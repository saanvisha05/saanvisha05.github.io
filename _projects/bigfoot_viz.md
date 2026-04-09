---
name: Bigfoot Sightings Visualization
tools: [Python, HTML, vega-lite]
image: assets/pngs/cars.png
description: Exploring Bigfoot sightings across the US using Altair and vega-lite!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

# Bigfoot Sightings Across the US

## Visualization 1: Sightings by State

<vegachart schema-url="{{ site.baseurl }}/assets/json/bigfoot_by_state.json" style="width: 100%"></vegachart>

This bar chart displays the total number of Bigfoot sightings reported in each US state, colored by season. The X axis uses a nominal encoding for state, sorted in descending order by count, and the Y axis uses a quantitative encoding for the count of records. Color encodes the season variable using a nominal encoding, allowing viewers to see which seasons dominate sightings in each state. Altair's default categorical color scheme was used since season is a discrete, unordered variable with no natural progression. A data transformation was performed to subset the dataframe to only the columns needed (state, season, date) and rows with missing state values were dropped using dropna().

## Visualization 2: Interactive Season Filter

<vegachart schema-url="{{ site.baseurl }}/assets/json/bigfoot_interactive.json" style="width: 100%"></vegachart>

This visualization consists of two linked bar charts. The right chart shows total sightings broken down by season, using nominal encoding on the X axis and quantitative count on the Y axis, colored by season. The left chart shows sightings by state, also colored by season. Both charts use the same subset dataframe with the same transformations described above. The interactivity allows the user to click on a season bar in the right chart to filter the left chart to only show sightings from that season. This makes it much easier to explore geographic patterns within a specific season rather than viewing all seasons stacked together at once.

## Search The Data & Methods

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/bfro_reports_fall2022.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/saanvisha05/saanvisha05.github.io/blob/main/python_notebooks/bigfoot_viz.ipynb" text="The Analysis" %}
</div>
