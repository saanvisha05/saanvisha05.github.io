---
name: License Data Visualization
tools: [Python, HTML, vega-lite]
image: assets/pngs/cars.png
description: Exploring license data using Altair and vega-lite!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

# License Data Analysis

## Visualization 1: Distribution of Values

<vegachart schema-url="{{ site.baseurl }}/assets/json/licenses_chart1.json" style="width: 100%"></vegachart>

This chart shows how square footage is distributed across buildings using a histogram. The x axis represents square footage and is grouped into bins so the values are easier to read, and the y axis shows the number of buildings in each range. Color is used to separate different usage types, which makes it easier to compare how building sizes vary across categories.

Before creating the chart, I filtered the dataset to only include the columns I needed and removed missing values using dropna(). I also used binning because the raw square footage values were very spread out and difficult to interpret without grouping them into ranges.

## Visualization 2: Interactive Legend Filter

<vegachart schema-url="{{ site.baseurl }}/assets/json/licenses_chart2.json" style="width: 100%"></vegachart>

This chart shows how the number of buildings changes over time and allows the user to filter by usage type by clicking on the legend. The x axis represents the year and the y axis shows the count of buildings. Each color corresponds to a different usage category, so the chart can display multiple categories at once.

This interaction makes the chart easier to read because the user can click on a category in the legend to isolate it and focus on its trend over time. This reduces clutter and makes it easier to compare patterns without being overwhelmed by all the data at once.

## Search The Data & Methods

<div class="left">
{% include elements/button.html link="https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/licenses_fall2022.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/saanvisha05/saanvisha05.github.io/blob/main/python_notebooks/445Proj.ipynb" text="The Analysis" %}
</div>
