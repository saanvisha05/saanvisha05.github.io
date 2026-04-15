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

This visualization displays the distribution of square footage values using a histogram. The x-axis uses a **quantitative encoding** with binning applied to group values into ranges, while the y-axis represents the **count of records**. Color is used as a **nominal encoding** to distinguish between different usage categories, allowing for comparison across groups. A categorical color scheme was chosen since the usage variable is discrete and unordered.

The dataset was preprocessed by selecting relevant columns and removing missing values using `dropna()`. Binning was applied to reduce clutter and improve readability, especially given the wide range of square footage values.

## Visualization 2: Interactive Dropdown Filter

<vegachart schema-url="{{ site.baseurl }}/assets/json/licenses_chart2.json" style="width: 100%"></vegachart>

This visualization shows how building counts change over time using an interactive dropdown filter. The x-axis uses a **quantitative encoding** for year, while the y-axis represents the **count of buildings**. Instead of displaying all categories at once, a dropdown selection allows the user to filter by usage type.

This interactivity improves clarity by reducing visual clutter and enabling focused analysis of individual categories. It allows users to explore trends over time for specific building types without distraction from overlapping data.

## Search The Data & Methods

<div class="left">
{% include elements/button.html link="https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/licenses_fall2022.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/saanvisha05/saanvisha05.github.io/blob/main/python_notebooks/445Proj.ipynb" text="The Analysis" %}
</div>
