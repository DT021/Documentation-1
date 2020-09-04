---
title:  Production Environment
summary: "The production environment within the network hierarchy organizes your strategy-deployment resources, grouping tasks, and associated forward testing and live trading sessions."
sidebar: suite_sidebar
permalink: suite-production-environment.html
toc: false
---

{% include /network/production-environment.md heading="" icon="150" adding="" configuring="" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include tip.html content="If you are familiar with the testing environment, the production environment works in the exact same way, only that it features forward testing and live trading sessions instead of backtesting and paper trading sessions. **Live sessions require the setup of a key instance and a live data feed, meaning that the sensor bot, along with all indicators used by the trading system, must be up and running**." %}

<table class='hierarchyTable'><thead><tr><th><a href='#production-environment' data-toggle='tooltip' data-original-title='{{site.data.network.production_environment}}'><img src='images/icons/nodes/png50/production-environment.png' /><br />Production Environment</a></th><th></th><th></th><th></th><th></th><th></th><th></th><th></th><th></th><th></th></tr></thead><tbody>
<tr><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#task-manager' data-toggle='tooltip' data-original-title='{{site.data.network.task_manager}}'><img src='images/icons/nodes/png50/task-manager.png' /><br />Task Manager</a></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#task' data-toggle='tooltip' data-original-title='{{site.data.network.task}}'><img src='images/icons/nodes/png50/task.png' /><br />Task</a></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td></td><td></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#trading-bot-instance' data-toggle='tooltip' data-original-title='{{site.data.network.trading_bot_instance}}'><img src='images/icons/nodes/png50/trading-bot-instance.png' /><br />Trading Bot Instance</a></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#trading-process-instance' data-toggle='tooltip' data-original-title='{{site.data.network.trading_process_instance}}'><img src='images/icons/nodes/png50/trading-process-instance.png' /><br />Trading Process Instance</a></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td></td><td></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-fork.png' /></td><td><a href='#forward-testing-session' data-toggle='tooltip' data-original-title='{{site.data.network.forward_testing_session}}'><img src='images/icons/nodes/png50/forward-testing-session.png' /><br />Forward Testing Session</a></td><td>&mdash;or&mdash;</td><td><a href='#live-trading-session' data-toggle='tooltip' data-original-title='{{site.data.network.live_trading_session}}'><img src='images/icons/nodes/png50/live-trading-session.png' /><br />Live Trading Session</a></td><td></td><td></td></tr>
<tr><td></td><td></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#parameters' data-toggle='tooltip' data-original-title='{{site.data.trading_system.parameters}}'><img src='images/icons/nodes/png50/parameters.png' /><br />Parameters</a></td><td></td><td></td><td></td></tr>
<tr><td></td><td></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-fork.png' /></td><td><a href='#market-reference' data-toggle='tooltip' data-original-title='{{site.data.network.market_reference}}'><img src='images/icons/nodes/png50/market-reference.png' /><br />Market Reference</a></td><td></td><td></td><td></td><td></td></tr>
<tr><td></td><td></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#key-instance' data-toggle='tooltip' data-original-title='{{site.data.trading_system.key_instance}}'><img src='images/icons/nodes/png50/key-instance.png' /><br />Key Instance</a></td><td></td><td></td><td></td></tr>
<tr><td></td><td></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#execution-started-event' data-toggle='tooltip' data-original-title='{{site.data.network.execution_started_event}}'><img src='images/icons/nodes/png50/execution-started-event.png' /><br />Execution Started Event</a></td><td></td><td></td><td></td><td></td></tr></tbody></table>




{% include /network/task-manager.md heading="##" icon="150" adding="####" configuring="" starting="####" content="yes" definition="bold" table="yes" more="yes"%}

{% include /network/task.md heading="##" icon="150" adding="####" configuring="" starting="####" content="yes" definition="bold" table="yes" more="yes"%}

{% include note.html content="In the context of the testing environment structure of nodes, tasks control trading bot instances." %}

{% include /network/trading-bot-instance.md heading="#####" icon="50" adding="#####" configuring="" starting="#####" content="yes" definition="yes" table="yes" more="yes"%}

{% include /network/trading-process-instance.md heading="######" icon="50" adding="######" configuring="" starting="######" content="yes" definition="yes" table="yes" more="yes"%}

{% include /network/market-reference.md heading="######" icon="50" adding="######" configuring="" starting="" content="yes" definition="yes" table="yes" more="yes"%}

{% include /network/key-instance.md heading="######" icon="50" adding="######" configuring="" starting="" content="yes" definition="yes" table="yes" more="yes"%}

{% include note.html content="Notice how live sessions do require a key instance, as these sessions do connect with the exchange." %}

{% include /data_mine/execution-started-event.md heading="######" icon="50" adding="######" configuring="" starting="" content="yes" definition="yes" table="yes" more="yes"%}

{% include /network/forward-testing-session.md heading="#####" icon="50" adding="#####" configuring="#####" starting="#####" content="yes" definition="yes" table="yes" more="yes"%}

{% include /network/live-trading-session.md heading="#####" icon="50" adding="#####" configuring="#####" starting="#####" content="yes" definition="yes" table="yes" more="yes"%}

{% include /network/parameters.md heading="######" icon="50" adding="######" configuring="" starting="" content="yes" definition="yes" table="yes" more="yes"%}

{% include note.html content="To learn about parameters, please see the <a href='suite-parameters.html'>parameters</a> page." %}
