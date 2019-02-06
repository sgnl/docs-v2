---
title: Visualization types
description: >
  InfluxDB dashboards support multiple visualization types including line graphs,
  gauges, tables, and more.
menu:
  v2_0:
    name: Visualization types
    parent: Visualize data
weight: 101
---

The InfluxDB's user interface's (UI) dashboard views support the following visualization types,
which can be selected in the **Visualization Type** selection view of the
[Data Explorer](/v2.0/visualize-data/explore-metrices).

[Visualization Type selector](/img/chrono-viz-types-selector.png)

Each of the available visualization types and available user controls are described below.

* [Line Graph](#line-graph)
* [Stacked Graph](#stacked-graph)
* [Step-Plot Graph](#step-plot-graph)
* [Single Stat](#single-stat)
* [Line Graph + Single Stat](#line-graph-single-stat)
* [Bar Graph](#bar-graph)
* [Gauge](#gauge)
* [Table](#table)


### Graphs

There are several types of graphs you can create.

#### Line Graph

The **Line Graph** view displays a time series in a line graph.

![Line Graph selector](/img/chrono-viz-line-graph-selector.png)

##### Line Graph Controls

![Line Graph Controls](/img/chrono-viz-line-graph-controls.png)

Use the **Line Graph Controls** to specify the following:

* **Title**: y-axis title. Enter title, if using a custom title.
  - **auto**: Enable or disable auto-setting.
* **Min**: Minimum y-axis value.
  - **auto**: Enable or disable auto-setting.
* **Max**: Maximum y-axis value.  
  - **auto**: Enable or disable auto-setting.
* **Y-Value's Prefix**: Prefix to be added to y-value.
* **Y-Value's Suffix**: Suffix to be added to y-value.
* **Y-Value's Format**: Toggle between **K/M/B** (Thousand/Million/Billion) and **K/M/G** (Kilo/Mega/Giga).
* **Scale**: Toggle between **Linear** and **Logarithmic**.
* **Static Legend**: Toggle between **Show** and **Hide**.


##### Line Graph example

![Line Graph example](/img/chrono-viz-line-graph-example.png)


#### Stacked Graph

The **Stacked Graph** view displays multiple time series bars as segments stacked on top of each other.

![Stacked Graph selector](/img/chrono-viz-stacked-graph-selector.png)

##### Stacked Graph Controls

![Stacked Graph Controls](/img/chrono-viz-stacked-graph-controls.png)

Use the **Stacked Graph Controls** to specify the following:

* **Title**: y-axis title. Enter title, if using a custom title.
  - **auto**: Enable or disable auto-setting.
* **Min**: Minimum y-axis value.
  - **auto**: Enable or disable auto-setting.
* **Max**: Maximum y-axis value.
  - **auto**: Enable or disable auto-setting.
* **Y-Value's Prefix**: Prefix to be added to y-value.
* **Y-Value's Suffix**: Suffix to be added to y-value.
* **Y-Value's Format**: Toggle between **K/M/B** (Thousand/Million/Billion) and **K/M/G** (Kilo/Mega/Giga).
* **Scale**: Toggle between **Linear** and **Logarithmic**.
* **Static Legend**: Toggle between **Show** and **Hide**.


##### Stacked Graph example

![Stacked Graph example](/img/chrono-viz-stacked-graph-example.png)


### Step Graph

The **Step-Plot Graph** view displays a time series in a staircase graph.

![Step-Plot Graph selector](/img/chrono-viz-step-plot-graph-selector.png)

#### Step Graph Controls

![Step-Plot Graph Controls](/img/chrono-viz-step-plot-graph-controls.png)

Use the **Step-Plot Graph Controls** to specify the following:

* **Title**: y-axis title. Enter title, if using a custom title.
  - **auto**: Enable or disable auto-setting.
* **Min**: Minimum y-axis value.
  - **auto**: Enable or disable auto-setting.
* **Max**: Maximum y-axis value.
  - **auto**: Enable or disable auto-setting.
* **Y-Value's Prefix**: Prefix to be added to y-value.
* **Y-Value's Suffix**: Suffix to be added to y-value.
* **Y-Value's Format**: Toggle between **K/M/B** (Thousand/Million/Billion) and **K/M/G** (Kilo/Mega/Giga).
* **Scale**: Toggle between **Linear** and **Logarithmic**.

#### Step-Plot Graph example

![Step-Plot Graph example](/img/chrono-viz-step-plot-graph-example.png)


### Bar Graph

The **Bar Graph** view displays the specified time series using a bar chart.

To select this view, click the Bar Graph selector icon.

![Bar Graph selector](/img/chrono-viz-bar-graph-selector.png)

#### Bar Graph Controls

![Bar Graph Controls](/img/chrono-viz-bar-graph-controls.png)

Use the **Bar Graph Controls** to specify the following:

* **Title**: y-axis title. Enter title, if using a custom title.
  - **auto**: Enable or disable auto-setting.
* **Min**: Minimum y-axis value.
  - **auto**: Enable or disable auto-setting.
* **Max**: Maximum y-axis value.
  - **auto**: Enable or disable auto-setting.
* **Y-Value's Prefix**: Prefix to be added to y-value.
* **Y-Value's Suffix**: Suffix to be added to y-value.
* **Y-Value's Format**: Toggle between **K/M/B** (Thousand/Million/Billion) and **K/M/G** (Kilo/Mega/Giga).
* **Scale**: Toggle between **Linear** and **Logarithmic**.

#### Bar Graph example

![Bar Graph example](/img/chrono-viz-bar-graph-example.png)


### Line Graph + Single Stat

The **Line Graph + Single Stat** view displays the specified time series in a line graph and overlays the single most recent value as a large numeric value.

To select this view, click the **Line Graph + Single Stat** view option.

![Line Graph + Single Stat selector](/img/chrono-viz-line-graph-single-stat-selector.png)

#### Line Graph + Single Stat Controls

![Line Graph + Single Stat Controls](/img/chrono-viz-line-graph-single-stat-controls.png)

Use the **Line Graph + Single Stat Controls** to specify the following:

* **Title**: y-axis title. Enter title, if using a custom title.
  - **auto**: Enable or disable auto-setting.
* **Min**: Minimum y-axis value.
  - **auto**: Enable or disable auto-setting.
* **Max**: Maximum y-axis value.
  - **auto**: Enable or disable auto-setting.
* **Y-Value's Prefix**: Prefix to be added to y-value.
* **Y-Value's Suffix**: Suffix to be added to y-value.
* **Y-Value's Format**: Toggle between **K/M/B** (Thousand/Million/Billion) and **K/M/G** (Kilo/Mega/Giga).
* **Scale**: Toggle between **Linear** and **Logarithmic**.

#### Line Graph + Single Stat example

![Line Graph + Single Stat example](/img/chrono-viz-line-graph-single-stat-example.png)

### Single Stat

The **Single Stat** view displays the most recent value of the specified time series as a numerical value.

![Single Stat view](/img/chrono-viz-single-stat-selector.png)

If a cell's query includes a [`GROUP BY` tag](/influxdb/latest/query_language/data_exploration/#group-by-tags) clause, the user interface sorts the different [series](/influxdb/latest/concepts/glossary/#series) lexicographically and shows the most recent [field value](/influxdb/latest/concepts/glossary/#field-value) associated with the first series.
For example, if a query groups by the `name` [tag key](/influxdb/latest/concepts/glossary/#tag-key) and `name` has two [tag values](/influxdb/latest/concepts/glossary/#tag-value) (`chronelda` and `chronz`), the user interface shows the most recent field value associated with the `chronelda` series.

If a cell's query includes more than one [field key](/influxdb/latest/concepts/glossary/#field-key) in the [`SELECT` clause](/influxdb/latest/query_language/data_exploration/#select-clause), the user interface returns the most recent field value associated with the first field key in the `SELECT` clause.
For example, if a query's `SELECT` clause is `SELECT "chronogiraffe","chronelda"`, the user interface shows the most recent field value associated with the `chronogiraffe` field key.

#### Single Stat Controls

Use the **Single Stat Controls** panel to specify one or more thresholds:

* **Add Threshold**: Button to add a new threshold.
* **Base Color**: Select a base, or background, color from the selection list.
  * Color options: Ruby, Fire, Curacao, Tiger, Pineapple, Thunder, Honeydew, Rainforest, Viridian, Ocean, Pool, Laser (default), Planet, Star, Comet, Pepper, Graphite, White, and Castle.
* **Prefix**: Prefix. For example, `%`, `MPH`, etc.
* **Suffix**: Suffix.  For example, `%`, `MPH`, etc.
* Threshold Coloring: Toggle between **Background** and **Text**


### Gauge

The **Gauge** view displays the single value most recent value for a time series in a gauge view.

To select this view, click the Gauge selector icon.

![Gauge selector](/img/chrono-viz-gauge-selector.png)

#### Gauge Controls

![Gauge Controls](/img/chrono-viz-gauge-controls.png)

Use the **Gauge Controls** to specify the following:

* **Add Threshold**: Click button to add a threshold.
* **Min**: Minimum value for the threshold.
  - Select color to display. Selection list options include: Laser (default), Ruby, Fire, Curacao, Tiger, Pineapple, Thunder, and Honeydew.
* **Max**: Maximum value for the threshold.
  - Select color to display. Selection list options include: Laser (default), Ruby, Fire, Curacao, Tiger, Pineapple, Thunder, and Honeydew.
* **Prefix**: Prefix. For example, `%`, `MPH`, etc.
* **Suffix**: Suffix.  For example, `%`, `MPH`, etc.

#### Gauge example

![Gauge example](/img/chrono-viz-gauge-example.png)

### Table

The **Table** panel displays the results of queries in a tabular view, which is sometimes easier to analyze than graph views of data.

![Table selector](/img/chrono-viz-table-selector.png)

#### Table Controls

![Table Controls](/img/chrono-viz-table-controls.png)

Use the **Table Controls** to specify the following:

* **Default Sort Field**: Select the default sort field. Default is **time**.
* **Decimal Places**: Enter the number of decimal places. Default (empty field) is **unlimited**.
* **Time Axis**: Select **Vertical** or **Horizontal**.
* **Time Format**: Select the time format.
    - Options include: `MM/DD/YYYY HH:mm:ss` (default), `MM/DD/YYYY HH:mm:ss.SSS`, `YYYY-MM-DD HH:mm:ss`, `HH:mm:ss`, `HH:mm:ss.SSS`, `MMMM D, YYYY HH:mm:ss`, `dddd, MMMM D, YYYY HH:mm:ss`, or `Custom`.
* **Lock First Column**: Lock the first column so that the listings are always visible. Threshold settings do not apply in the first column when locked.
* **Customize Field**:
  - **time**: Enter a new name to rename.
  - [additional]: Enter name for each additional column.
  - Change the order of the column by dragging to the desired position.
* **Thresholds**

{{% note %}}
Threshold settings apply to any cells with values, except when they appear in the first column and **Lock First Column** is enabled.
{{% /note %}}

  - **Add Threshold** (button): Click to add a threshold.
  - **Base Color**: Select a base, or background, color from the selection list.
    * Color options: Ruby, Fire, Curacao, Tiger, Pineapple, Thunder, Honeydew, Rainforest, Viridian, Ocean, Pool, Laser (default), Planet, Star, Comet, Pepper, Graphite, White, and Castle.

#### Table view example

![Table example](/img/chrono-viz-table-example.png)