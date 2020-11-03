---
title: Syncing With the Exchange
summary: "Syncing with the exchange involves calculating the actual size, the actual rate, the percentage filled, the fees paid, and the size filled, to update the trading engine data structure so that it matches with the actual situation of the order at the exchange."
sidebar: suite_sidebar
permalink: suite-low-frequency-syncing-with-the-exchange.html
---

The process of synchronizing the data in the trading engine with what actually happens at the exchange is crucial to monitoring and controlling a live trading operation from within Superalgos. It is this process that allows users to access the information at the exchange throughout the life cycle of each order, on the fly.

This is when all calculations involving the actual size, actual rate, actual fees, and so on are made. We will closely look into each of the calculations.

Once the synchronization is done, the bot does the accounting (see [Accounting](suite-low-frequency-accounting.html)), to keep the rest of the variables&mdash;like balances and the stage size&mdash;up to date with the reality of orders.

## Actual Size Calculation

While users may define the target size of the stage in either the base asset or the quoted asset, the size of orders is always denominated in the base asset, as per the CCXT Library API, and&mdash;likely&mdash;most exchange’s APIs.

{% include note.html content='It is a common occurrence that exchanges change the size slightly, for whatever reason, including issues with the precision of decimal places, for example. This is why the size of the order as defined by the user may need to be updated, synchronizing it with the actual size determined by the exchange.' %}

When the actual size of the order as reported by the exchange is different than the size defined by the user, the trading bot makes the adjustments described below.

### Recalculate Actual Size

The actual size of the base asset is updated with the size reported by the exchange:

```
tradingEngineOrder.orderBaseAsset.actualSize.value = order.amount
```

Then it’s time to calculate the actual size in the quoted asset. At this stage, the actual rate of the order hasn’t been established yet, so the existing rate is used temporarily.

```
tradingEngineOrder.orderQuotedAsset.actualSize.value = 
tradingEngineOrder.orderBaseAsset.actualSize.value * 
tradingEngineOrder.rate.value
```

### Recalculate Size Placed

The open stage and close stage sections of the trading engine hierarchy keep track of the accumulated size of the orders that have been placed so that the stage size may be compared to the target size defined in the trading system. 

{% include note.html content='Remember that the target size defined acts as a size cap, thus, the system must not place orders in excess of the defined target size.' %}

If the size of the order as determined by the exchange is different from the original size of the order, the current stage size must be recalculated.

What the trading bot does in this case is subtracting the original size from the stage size placed, and then add the actual size, as obtained from the exchange. As usual, this is done both for the base asset and the quoted asset.

For clarity, each operation is done in two steps.

```
tradingEngineStage.stageBaseAsset.sizePlaced.value =
tradingEngineStage.stageBaseAsset.sizePlaced.value -
tradingEngineOrder.orderBaseAsset.size.value

tradingEngineStage.stageBaseAsset.sizePlaced.value =
tradingEngineStage.stageBaseAsset.sizePlaced.value +
tradingEngineOrder.orderBaseAsset.actualSize.value

tradingEngineStage.stageQuotedAsset.sizePlaced.value =
tradingEngineStage.stageQuotedAsset.sizePlaced.value -
tradingEngineOrder.orderQuotedAsset.size.value

tradingEngineStage.stageQuotedAsset.sizePlaced.value =
tradingEngineStage.stageQuotedAsset.sizePlaced.value +
tradingEngineOrder.orderQuotedAsset.actualSize.value
```

## Actual Rate Calculation

Market orders are placed without a definition in terms of the rate they will be executed at, as, by definition, a market rate is filled at whatever rate the order book allows. 

In the case of limit orders&mdash;although the user defines a rate&mdash;the exchange may change it slightly, for multiple reasons. For example, due to issues related to decimals precision, or because the order may match existing orders in the order book with a better rate.

For those reasons, the trading bot gets the actual rate from the exchange and &mdash;in case it differs from the defined rate&mdash;makes the updates described below.

First of all, the actual rate under the order statistics node is updated with the actual rate provided by the exchange:

```
tradingEngineOrder.orderStatistics.actualRate.value = order.price
```

If the actual rate is the same as the rate of the order as originally defined, then that’s all. Otherwise, the bot goes back and recalculates the size of the order for the quoted asset and the size placed in the quoted asset for the corresponding stage&mdash;again.

{% include callout.html type='success' content='Let’s do a little recap in case the above is not crystal clear. When the order size in the quoted asset was calculated earlier, the calculation was made by multiplying the actual size in the base asset as reported by the exchange, by the rate as was originally defined. However, if the rate used earlier is not the actual rate at which the order was filled at the exchange, the trading bot needs to go back and calculate the size in the quoted asset again. The same goes for the size placed in the quoted asset.' %}

Both calculations are virtually the same as described earlier, so we are not going to go over the details again. Suffice to say that the only difference is that the actual rate is used instead of the original rate as defined in the trading system.

And remember, the size in the base asset does not need to be recalculated, as it is not affected by the differences in rates.

## Percentage Filled Calculation

This is a simple calculation to determine what percentage of the order has been filled, which is relevant later on to calculate fees and balances:

```
tradingEngineOrder.orderStatistics.percentageFilled.value = 
order.filled * 100 / 
tradingEngineOrder.orderBaseAsset.actualSize.value
```

{% include note.html content='As you can see, the actual size in the base asset is used, as the size is always denominated in the base asset according to the exchange.' %}

## Fees Paid Calculation

Exchange fees are a crucial aspect of trading, as they may greatly affect the profitability of strategies. 

{% include callout.html type='success' content='Surprisingly, the exchange does not explicitly report how much is charged in fees on each order. This apparent contradiction must be resolved by Superalgos, so let’s dive into the details.' %}

There are a few fundamental workings that affect the calculations:

The fees are not explicitly reported by the exchange, hence the need to calculate them. 

{% include important.html content='To calculate fees, the user bears the ultimate responsibility in supplying the trading bot with the correct parameters defined in the fee structure session parameters. It is these values of maker and taker fees that the system uses to calculate fees. If the parameters are wrong, the calculated fees will be wrong as well. ' %}

The ```taker``` fee parameter is used to calculate the fees on market orders, while the ```maker``` fee parameter is used to calculate fees for limit orders.

The exchange charges fees denominated in the asset that the user is acquiring in the transaction. For example, in the BTC/USDT market, a sell order exchanges BTC for USDT, and the exchange charges fees in USDT, because that is the asset you are acquiring. On the contrary, a buy order in the BTC/USDT market exchanges USDT for BTC, thus fees are charged in BTC.

{% include callout.html type='success' content='Properly calculating fees is crucial to keeping an accurate accounting system, as they directly affect balances. This is why: The actual size reported by the exchange is not representative of the actual amount of the asset acquired in the transaction. This is because the exchange fills the order, determines the size filled, and then subtracts the fees from the size filled. That is, the size filled reported by the exchange is greater than the amount you receive. In fact, the amount you receive is the actual size filled minus the fees. That calculation is the one used to estimate the balances for both assets in Superalgos so that they match the balances at the exchange.' %}

Because orders (in particular limit orders) may be partially filled, the system uses the percentage filled calculated earlier to determine the fees to be paid for the portion filled, as the exchange charges fees for the amount filled only.

All of the above considerations are captured in the following calculations.

### Market buy orders

Because you are acquiring the base asset, fees paid are calculated using the base asset actual size. Because it’s a market order, the taker fees parameter is used.

```
tradingEngineOrder.orderBaseAsset.feesPaid.value =
tradingEngineOrder.orderBaseAsset.actualSize.value *
sessionParameters.feeStructure.config.taker / 100 *
tradingEngineOrder.orderStatistics.percentageFilled.value / 100
```

### Limit buy orders

Like with market buy orders, because you are acquiring the base asset, fees paid are calculated using the base asset actual size. Because it’s a limit order, the maker fees parameter is used.

```
tradingEngineOrder.orderBaseAsset.feesPaid.value =
tradingEngineOrder.orderBaseAsset.actualSize.value *
sessionParameters.feeStructure.config.maker / 100 *
tradingEngineOrder.orderStatistics.percentageFilled.value / 100
```

### Market sell orders

Because you are acquiring the quoted asset, fees paid are calculated using the base asset actual size. Because it’s a market order, the taker fees parameter is used.

```
tradingEngineOrder.orderQuotedAsset.feesPaid.value =
tradingEngineOrder.orderQuotedAsset.actualSize.value *
sessionParameters.feeStructure.config.taker / 100 *
tradingEngineOrder.orderStatistics.percentageFilled.value / 100
```

### Limit sell orders

Like with market sell orders, because you are acquiring the quoted asset, fees paid are calculated using the quoted asset actual size. Because it’s a limit order, the maker fees parameter is used.

```
tradingEngineOrder.orderQuotedAsset.feesPaid.value =
tradingEngineOrder.orderQuotedAsset.actualSize.value *
sessionParameters.feeStructure.config.maker / 100 *
tradingEngineOrder.orderStatistics.percentageFilled.value / 100
```

## Size Filled Calculation

As mentioned earlier, and as may be inferred from the example orders presented earlier, the size filled is always reported by the exchange denominated in the base asset. That is:

```
tradingEngineOrder.orderBaseAsset.sizeFilled.value = order.filled
```

Therefore, the trading bot needs to calculate the size filled in the quoted asset:

```
tradingEngineOrder.orderQuotedAsset.sizeFilled.value =
tradingEngineOrder.orderQuotedAsset.actualSize.value * 
tradingEngineOrder.orderStatistics.percentageFilled.value / 100
```

## Amount Received Calculation

The amount received is a simple calculation to facilitate the comprehension of the trade, given that the exchange does not provide that basic information. Remember that only the size filled is reported and that fees are subtracted from the size filled.

### Market and limit buy orders

In these cases, the user receives the amount in the base asset.

```
tradingEngineOrder.orderBaseAsset.amountReceived.value =
tradingEngineOrder.orderBaseAsset.sizeFilled.value -
tradingEngineOrder.orderBaseAsset.feesPaid.value
```

### Market and limit sell orders

In these cases, the user receives the amount in the quoted asset.

```
tradingEngineOrder.orderQuotedAsset.amountReceived.value =
tradingEngineOrder.orderQuotedAsset.sizeFilled.value -
tradingEngineOrder.orderQuotedAsset.feesPaid.value
```
