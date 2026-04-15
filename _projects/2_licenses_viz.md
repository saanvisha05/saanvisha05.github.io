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

This chart shows how square footage is distributed across buildings using a histogram. The x axis represents square footage and is grouped into bins so the values are easier to read. The y axis shows how many buildings fall into each range. Color is used to separate the different usage categories so it is easier to compare how building sizes vary across them.

Before making the chart, I filtered the dataset to only include the columns I needed and removed missing values using dropna(). I also used binning because the raw values were too spread out and hard to interpret without grouping them.

## Visualization 2: Interactive Dropdown Filter

<vegachart schema-url="{{ site.baseurl }}/assets/json/licenses_chart2.json" style="width: 100%"></vegachart>

This chart shows how the number of buildings changes over time and includes a dropdown that lets the user filter by usage type. The x axis represents the year and the y axis shows the count of buildings. Instead of displaying all categories at once, the dropdown lets the user focus on one category at a time.

This makes the chart easier to understand because it removes clutter and helps highlight trends for specific types of buildings. The interactivity allows users to explore the data in a more focused way instead of looking at everything at once.

## Search The Data & Methods

<div class="left">
{% include elements/button.html link="https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/licenses_fall2022.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/saanvisha05/saanvisha05.github.io/blob/main/python_notebooks/445Proj.ipynb" text="The Analysis" %}
</div>
