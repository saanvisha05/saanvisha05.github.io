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

## Visualization 1: Distribution

<vegachart schema-url="{{ site.baseurl }}/assets/json/licenses_chart1.json" style="width: 100%"></vegachart>

This visualization shows the distribution of values using a histogram with binned quantitative encoding on the x-axis and count on the y-axis. Data was cleaned by selecting relevant columns and removing missing values using dropna().

## Visualization 2: Interactive Dropdown Filter

<vegachart schema-url="{{ site.baseurl }}/assets/json/licenses_chart2.json" style="width: 100%"></vegachart>

This visualization uses a dropdown filter to allow users to select categories dynamically. The x-axis encodes time while the y-axis shows counts. This interactivity makes it easier to isolate patterns without clutter.

## Search The Data & Methods

<div class="left">
{% include elements/button.html link="https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/licenses_fall2022.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/saanvisha05/saanvisha05.github.io/blob/main/python_notebooks/445Proj.ipynb" text="The Analysis" %}
</div>
