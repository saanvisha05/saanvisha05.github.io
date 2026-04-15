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

This visualization shows the distribution of the selected variable using a histogram. The X-axis uses a quantitative encoding with binning applied to group values into ranges, while the Y-axis represents the count of records. Color is used to distinguish categorical groupings, allowing comparison across different categories. The dataset was preprocessed by selecting relevant columns and removing missing values using dropna().

## Visualization 2: Interactive Dropdown Filter

<vegachart schema-url="{{ site.baseurl }}/assets/json/licenses_chart2.json" style="width: 100%"></vegachart>

This chart displays how values change over time, with an interactive dropdown that allows users to filter the data by category. The X-axis uses a quantitative encoding for time, while the Y-axis shows counts. The dropdown interactivity allows users to isolate specific categories, making it easier to explore patterns without visual clutter. This improves clarity compared to displaying all categories simultaneously.

## Search The Data & Methods

<div class="left">
{% include elements/button.html link="https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/licenses_fall2022.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/saanvisha05/saanvisha05.github.io/blob/main/python_notebooks/YOUR_NOTEBOOK_NAME.ipynb" text="The Analysis" %}
</div>
