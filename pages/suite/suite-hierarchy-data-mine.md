---
title:  Data Mine Hierarchy
summary: "A data mine provides the tools to build indicators, produce data visualization plotters, and process markets data, with minimal coding requirements."
sidebar: suite_sidebar
permalink: suite-hierarchy-data-mine.html
toc: false
---

{% include note.html content="Hover your mouse over a node for a tooltip definition, and click to get all the details." %}

<table class='hierarchyTable'><thead><tr><th><a href='#data-mine' data-toggle='tooltip' data-original-title='{{site.data.data_mine.data_mine}}'><img src='images/icons/nodes/png50/data-mine.png' /><br />Data Mine</a></th><th></th><th></th><th></th><th></th><th></th><th></th><th></th><th></th><th></th></tr></thead><tbody>
<tr><td><img src='images/icons/various/png/tree-connector-fork.png' /></td><td><a href='#indicator-bot' data-toggle='tooltip' data-original-title='{{site.data.data_mine.indicator_bot}}'><img src='images/icons/nodes/png50/indicator-bot.png' /><br />Indicator Bot</a></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-fork.png' /></td><td><a href='#process-definition' data-toggle='tooltip' data-original-title='{{site.data.data_mine.process_definition}}'><img src='images/icons/nodes/png50/process-definition.png' /><br />Process Definition</a></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-fork.png' /></td><td><a href='#process-output' data-toggle='tooltip' data-original-title='{{site.data.data_mine.process_output}}'><img src='images/icons/nodes/png50/process-output.png' /><br />Process Output</a></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#output-dataset' data-toggle='tooltip' data-original-title='{{site.data.data_mine.output_dataset}}'><img src='images/icons/nodes/png50/output-dataset.png' /><br />Output Dataset</a></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-fork.png' /></td><td><a href='#process-dependencies' data-toggle='tooltip' data-original-title='{{site.data.data_mine.process_dependencies}}'><img src='images/icons/nodes/png50/process-dependencies.png' /><br />Process Dependencies</a></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-fork.png' /></td><td><a href='#status-dependency' data-toggle='tooltip' data-original-title='{{site.data.data_mine.status_dependency}}'><img src='images/icons/nodes/png50/status-dependency.png' /><br />Status Dependency</a></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#data-dependency' data-toggle='tooltip' data-original-title='{{site.data.data_mine.data_dependency}}'><img src='images/icons/nodes/png50/data-dependency.png' /><br />Data Dependency</a></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-fork.png' /></td><td><a href='#status-report' data-toggle='tooltip' data-original-title='{{site.data.data_mine.status_report}}'><img src='images/icons/nodes/png50/status-report.png' /><br />Status Report</a></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-fork.png' /></td><td><a href='#execution-started-event' data-toggle='tooltip' data-original-title='{{site.data.data_mine.execution_started_event}}'><img src='images/icons/nodes/png50/execution-started-event.png' /><br />Execution Started Event</a></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#execution-finished-event' data-toggle='tooltip' data-original-title='{{site.data.data_mine.execution_finished_event}}'><img src='images/icons/nodes/png50/execution-finished-event.png' /><br />Execution Finished Event</a></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#product-definition' data-toggle='tooltip' data-original-title='{{site.data.data_mine.product_definition}}'><img src='images/icons/nodes/png50/product-definition.png' /><br />Product Definition</a></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td></td><td><img src='images/icons/various/png/tree-connector-fork.png' /></td><td><a href='#dataset-definition' data-toggle='tooltip' data-original-title='{{site.data.data_mine.dataset_definition}}'><img src='images/icons/nodes/png50/dataset-definition.png' /><br />Dataset Definition</a></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td></td><td><img src='images/icons/various/png/tree-connector-fork.png' /></td><td><a href='#record-definition' data-toggle='tooltip' data-original-title='{{site.data.data_mine.record_definition}}'><img src='images/icons/nodes/png50/record-definition.png' /><br />Record Definition</a></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#record-property' data-toggle='tooltip' data-original-title='{{site.data.data_mine.record_property}}'><img src='images/icons/nodes/png50/record-property.png' /><br />Record Property</a></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#formula' data-toggle='tooltip' data-original-title='{{site.data.data_mine.formula}}'><img src='images/icons/nodes/png50/formula.png' /><br />Formula</a></td><td></td><td></td><td></td><td></td></tr>
<tr><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td></td><td><img src='images/icons/various/png/tree-connector-fork.png' /></td><td><a href='#calculations-procedure' data-toggle='tooltip' data-original-title='{{site.data.data_mine.calculations_procedure}}'><img src='images/icons/nodes/png50/calculations-procedure.png' /><br />Calculations Procedure</a></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-fork.png' /></td><td><a href='#procedure-loop' data-toggle='tooltip' data-original-title='{{site.data.data_mine.procedure_loop}}'><img src='images/icons/nodes/png50/procedure-loop.png' /><br />Procedure Loop</a></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#javascript-code' data-toggle='tooltip' data-original-title='{{site.data.data_mine.javascript_code}}'><img src='images/icons/nodes/png50/javascript-code.png' /><br />JavaScript Code</a></td><td></td><td></td><td></td><td></td></tr>
<tr><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#procedure-initialization' data-toggle='tooltip' data-original-title='{{site.data.data_mine.procedure_initialization}}'><img src='images/icons/nodes/png50/procedure-initialization.png' /><br />Procedure Initialization</a></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#javascript-code' data-toggle='tooltip' data-original-title='{{site.data.data_mine.javascript_code}}'><img src='images/icons/nodes/png50/javascript-code.png' /><br />JavaScript Code</a></td><td></td><td></td><td></td><td></td></tr>
<tr><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#data-building-procedure' data-toggle='tooltip' data-original-title='{{site.data.data_mine.data_building_procedure}}'><img src='images/icons/nodes/png50/data-building-procedure.png' /><br />Data Building Procedure</a></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-fork.png' /></td><td><a href='#procedure-loop' data-toggle='tooltip' data-original-title='{{site.data.data_mine.procedure_loop}}'><img src='images/icons/nodes/png50/procedure-loop.png' /><br />Procedure Loop</a></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#javascript-code' data-toggle='tooltip' data-original-title='{{site.data.data_mine.javascript_code}}'><img src='images/icons/nodes/png50/javascript-code.png' /><br />JavaScript Code</a></td><td></td><td></td><td></td><td></td></tr>
<tr><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#procedure-initialization' data-toggle='tooltip' data-original-title='{{site.data.data_mine.procedure_initialization}}'><img src='images/icons/nodes/png50/procedure-initialization.png' /><br />Procedure Initialization</a></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#javascript-code' data-toggle='tooltip' data-original-title='{{site.data.data_mine.javascript_code}}'><img src='images/icons/nodes/png50/javascript-code.png' /><br />JavaScript Code</a></td><td></td><td></td><td></td><td></td></tr>
<tr><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#plotter' data-toggle='tooltip' data-original-title='{{site.data.data_mine.plotter}}'><img src='images/icons/nodes/png50/plotter.png' /><br />Plotter</a></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#plotter-module' data-toggle='tooltip' data-original-title='{{site.data.data_mine.plotter_module}}'><img src='images/icons/nodes/png50/plotter-module.png' /><br />Plotter Module</a></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td></td><td></td><td><img src='images/icons/various/png/tree-connector-fork.png' /></td><td><a href='#plotter-panel' data-toggle='tooltip' data-original-title='{{site.data.data_mine.plotter_panel}}'><img src='images/icons/nodes/png50/plotter-panel.png' /><br />Plotter Panel</a></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td></td><td></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#panel-data' data-toggle='tooltip' data-original-title='{{site.data.data_mine.panel_data}}'><img src='images/icons/nodes/png50/panel-data.png' /><br />Panel Data</a></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td></td><td></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#data-formula' data-toggle='tooltip' data-original-title='{{site.data.data_mine.data_formula}}'><img src='images/icons/nodes/png50/data-formula.png' /><br />Data Formula</a></td><td></td><td></td><td></td><td></td></tr>
<tr><td></td><td></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#shapes' data-toggle='tooltip' data-original-title='{{site.data.data_mine.shapes}}'><img src='images/icons/nodes/png50/shapes.png' /><br />Shapes</a></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-fork.png' /></td><td><a href='#chart-points' data-toggle='tooltip' data-original-title='{{site.data.data_mine.chart_points}}'><img src='images/icons/nodes/png50/chart-points.png' /><br />Chart Points</a></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#point' data-toggle='tooltip' data-original-title='{{site.data.data_mine.point}}'><img src='images/icons/nodes/png50/point.png' /><br />Point</a></td><td></td><td></td><td></td><td></td></tr>
<tr><td></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#point-formula' data-toggle='tooltip' data-original-title='{{site.data.data_mine.point_formula}}'><img src='images/icons/nodes/png50/point-formula.png' /><br />Point Formula</a></td><td></td><td></td><td></td></tr>
<tr><td></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-fork.png' /></td><td><a href='#polygon' data-toggle='tooltip' data-original-title='{{site.data.data_mine.polygon}}'><img src='images/icons/nodes/png50/polygon.png' /><br />Polygon</a></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-fork.png' /></td><td><a href='#polygon-condition' data-toggle='tooltip' data-original-title='{{site.data.data_mine.polygon_condition}}'><img src='images/icons/nodes/png50/polygon-condition.png' /><br />Polygon Condition</a></td><td></td><td></td><td></td><td></td></tr>
<tr><td></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-fork.png' /></td><td><a href='#polygon-vertex' data-toggle='tooltip' data-original-title='{{site.data.data_mine.polygon_vertex}}'><img src='images/icons/nodes/png50/polygon-vertex.png' /><br />Polygon Vertex</a></td><td></td><td></td><td></td><td></td></tr>
<tr><td></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-fork.png' /></td><td><a href='#polygon-border' data-toggle='tooltip' data-original-title='{{site.data.data_mine.polygon_border}}'><img src='images/icons/nodes/png50/polygon-border.png' /><br />Polygon Border</a></td><td></td><td></td><td></td><td></td></tr>
<tr><td></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-fork.png' /></td><td><a href='#style' data-toggle='tooltip' data-original-title='{{site.data.data_mine.style}}'><img src='images/icons/nodes/png50/style.png' /><br />Style</a></td><td></td><td></td><td></td></tr>
<tr><td></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#style-condition' data-toggle='tooltip' data-original-title='{{site.data.data_mine.style_condition}}'><img src='images/icons/nodes/png50/style-condition.png' /><br />Style Condition</a></td><td></td><td></td><td></td></tr>
<tr><td></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#style' data-toggle='tooltip' data-original-title='{{site.data.data_mine.style}}'><img src='images/icons/nodes/png50/style.png' /><br />Style</a></td><td></td><td></td></tr>
<tr><td></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#polygon-body' data-toggle='tooltip' data-original-title='{{site.data.data_mine.polygon_body}}'><img src='images/icons/nodes/png50/polygon-body.png' /><br />Polygon Body</a></td><td></td><td></td><td></td><td></td></tr>
<tr><td></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td></td><td><img src='images/icons/various/png/tree-connector-fork.png' /></td><td><a href='#style' data-toggle='tooltip' data-original-title='{{site.data.data_mine.style}}'><img src='images/icons/nodes/png50/style.png' /><br />Style</a></td><td></td><td></td><td></td></tr>
<tr><td></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#style-condition' data-toggle='tooltip' data-original-title='{{site.data.data_mine.style_condition}}'><img src='images/icons/nodes/png50/style-condition.png' /><br />Style Condition</a></td><td></td><td></td><td></td></tr>
<tr><td></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#style' data-toggle='tooltip' data-original-title='{{site.data.data_mine.style}}'><img src='images/icons/nodes/png50/style.png' /><br />Style</a></td><td></td><td></td></tr>
<tr><td></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-fork.png' /></td><td><a href='#image' data-toggle='tooltip' data-original-title='{{site.data.data_mine.image}}'><img src='images/icons/nodes/png50/image.png' /><br />Image</a></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-fork.png' /></td><td><a href='#image-condition' data-toggle='tooltip' data-original-title='{{site.data.data_mine.image_condition}}'><img src='images/icons/nodes/png50/image-condition.png' /><br />Image Condition</a></td><td></td><td></td><td></td><td></td></tr>
<tr><td></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-line.png' /></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#image-position' data-toggle='tooltip' data-original-title='{{site.data.data_mine.image_position}}'><img src='images/icons/nodes/png50/image-position.png' /><br />Image Position</a></td><td></td><td></td><td></td><td></td></tr>
<tr><td></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#text' data-toggle='tooltip' data-original-title='{{site.data.data_mine.text}}'><img src='images/icons/nodes/png50/text.png' /><br />Text</a></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td></td><td></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-fork.png' /></td><td><a href='#text-condition' data-toggle='tooltip' data-original-title='{{site.data.data_mine.text_condition}}'><img src='images/icons/nodes/png50/text-condition.png' /><br />Text Condition</a></td><td></td><td></td><td></td><td></td></tr>
<tr><td></td><td></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-fork.png' /></td><td><a href='#text-position' data-toggle='tooltip' data-original-title='{{site.data.data_mine.text_position}}'><img src='images/icons/nodes/png50/text-position.png' /><br />Text Position</a></td><td></td><td></td><td></td><td></td></tr>
<tr><td></td><td></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-fork.png' /></td><td><a href='#text-formula' data-toggle='tooltip' data-original-title='{{site.data.data_mine.text_formula}}'><img src='images/icons/nodes/png50/text-formula.png' /><br />Text Formula</a></td><td></td><td></td><td></td><td></td></tr>
<tr><td></td><td></td><td></td><td></td><td><img src='images/icons/various/png/tree-connector-elbow.png' /></td><td><a href='#text-style' data-toggle='tooltip' data-original-title='{{site.data.data_mine.text_style}}'><img src='images/icons/nodes/png50/text-style.png' /><br />Text Style</a></td><td></td><td></td><td></td><td></td></tr></tbody></table>




{% include /data_mine/data-mine.md heading="##" icon="150" adding="####" configuring="####" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/indicator-bot.md heading="##" icon="150" adding="####" configuring="####" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/process-definition.md heading="##" icon="150" adding="####" configuring="####" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/process-output.md heading="##" icon="150" adding="####" configuring="" starting="" content="no" definition="bold" table="yes" more="no"%}

{% include /data_mine/output-dataset.md heading="##" icon="150" adding="####" configuring="" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/process-dependencies.md heading="##" icon="150" adding="####" configuring="" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/status-dependency.md heading="##" icon="150" adding="####" configuring="####" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/data-dependency.md heading="##" icon="150" adding="####" configuring="" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/status-report.md heading="##" icon="150" adding="####" configuring="" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/execution-started-event.md heading="##" icon="150" adding="####" configuring="" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/execution-finished-event.md heading="##" icon="150" adding="####" configuring="" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/product-definition.md heading="##" icon="150" adding="####" configuring="####" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/dataset-definition.md heading="##" icon="150" adding="####" configuring="####" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/record-definition.md heading="##" icon="150" adding="####" configuring="" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/record-property.md heading="##" icon="150" adding="####" configuring="####" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/formula.md heading="##" icon="150" adding="####" configuring="" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/calculations-procedure.md heading="##" icon="150" adding="####" configuring="" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/procedure-loop.md heading="##" icon="150" adding="####" configuring="" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/javascript-code.md heading="##" icon="150" adding="####" configuring="" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/procedure-initialization.md heading="##" icon="150" adding="####" configuring="" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/data-building-procedure.md heading="##" icon="150" adding="####" configuring="" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/plotter.md heading="##" icon="150" adding="####" configuring="####" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/plotter-module.md heading="##" icon="150" adding="####" configuring="####" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/plotter-panel.md heading="##" icon="150" adding="####" configuring="" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/panel-data.md heading="##" icon="150" adding="####" configuring="####" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/data-formula.md heading="##" icon="150" adding="####" configuring="" starting="" content="no" definition="bold" table="yes" more="no"%}

{% include /data_mine/shapes.md heading="##" icon="150" adding="####" configuring="" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/chart-points.md heading="##" icon="150" adding="####" configuring="" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/point.md heading="##" icon="150" adding="####" configuring="" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/point-formula.md heading="##" icon="150" adding="####" configuring="" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/polygon.md heading="##" icon="150" adding="####" configuring="" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/polygon-condition.md heading="##" icon="150" adding="####" configuring="####" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/polygon-vertex.md heading="##" icon="150" adding="####" configuring="" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/polygon-border.md heading="##" icon="150" adding="####" configuring="" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/style.md heading="##" icon="150" adding="####" configuring="####" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/style-condition.md heading="##" icon="150" adding="####" configuring="####" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/polygon-body.md heading="##" icon="150" adding="####" configuring="" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/image.md heading="##" icon="150" adding="####" configuring="####" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/image-condition.md heading="##" icon="150" adding="#####" configuring="" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/image-position.md heading="##" icon="150" adding="#####" configuring="#####" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/text.md heading="##" icon="150" adding="####" configuring="" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/text-condition.md heading="##" icon="150" adding="#####" configuring="" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/text-position.md heading="##" icon="150" adding="#####" configuring="#####" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/text-formula.md heading="##" icon="150" adding="#####" configuring="" starting="" content="yes" definition="bold" table="yes" more="no"%}

{% include /data_mine/text-style.md heading="##" icon="150" adding="#####" configuring="#####" starting="" content="yes" definition="bold" table="yes" more="no"%}
