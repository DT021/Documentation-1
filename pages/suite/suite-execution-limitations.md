---
title:  Execution Limitations
summary: "Orders may not be fragmented and all orders are market orders."
sidebar: suite_sidebar
permalink: suite-execution-limitations.html
---

At the current stage of development, users have no control whatsoever over the execution of orders.

{% include tip.html content="All of the limitations detailed below will be lifted with the upcoming release of Superalgos Beta 6 featuring a brand new iteration of the trading engine. Superalgos Beta 6 gives you absolute control over trading execution." %}

**The way order execution works at this stage is quite basic: once conditions are met for taking a position, or once a take profit or stop target is hit, one single market order is placed at the exchange**.

When taking a position, the Take Position price shown in simulations is defined by the formula you use in your ```Open Stage > Initial Definition > Position Rate > Formula```. 

[![Live-Trading-Execution-Position-Rate](https://user-images.githubusercontent.com/13994516/63421629-3980c180-c409-11e9-837e-212e69588ebb.gif)](https://user-images.githubusercontent.com/13994516/63421629-3980c180-c409-11e9-837e-212e69588ebb.gif)

However, this is overridden during live-trading, and replaced with a market order.

When taking profit or hitting a stop, that is, when attempting to close a position, the price in simulations is determined by the intersection of the corresponding candle with the values resulting from the active take profit and stop phases formulas.

However, during live-trading, once a take profit or stop target is hit, the order to close the trade is placed as a market order.

An additional limitation is that there currently is no feature to fragment orders, therefore, the size of your orders and the likelihood of them getting filled depend on the liquidity of the market/exchange.

{% include important.html content="It is important that you fully understand the implications of these limitations if you are considering to trade live with the system at this stage, as you will need to adapt to the current state of affairs." %}
