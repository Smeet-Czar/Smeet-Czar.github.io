---
name: Buliding usage analysis
tools: [Python, HTML, vega-lite, Altair]
image: assets/pngs/Buildings.png
description: This is a "showcase" project that uses vega-lite for interactive viz!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Example including vega-lite

Example comes from this [great blog post right here](https://blog.4dcu.be/programming/2021/05/03/Interactive-Visualizations.html) that was also used in [our test import script](https://github.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/blob/main/week01/test_imports_week01.ipynb).

We can use a vegachart HTML tag like so:

```
<vegachart schema-url="{{ site.baseurl }}/assets/json/1_usage_chart.json" style="width: 100%"></vegachart>
```

<vegachart schema-url="{{ site.baseurl }}/assets/json/1_usage_chart.json" style="width: 100%"></vegachart>

This bar chart shows the distribution of building usage categories (Usage Description) in a selected city. Users can select a city from a dropdown menu, and the chart dynamically updates to display the count of buildings in each category for the selected city.

## Encoding Types:
* X-axis: Encodes the Usage Description as a nominal variable. Categories are sorted in descending order of count.
* Y-axis: Encodes the count of buildings (count()) as a quantitative variable to show the number of buildings in each category.
* Color Scheme: Encodes each Usage Description with a unique color. This choice highlights differences between usage categories and makes the chart more visually appealing.

## Interactivity:
* The dropdown menu provides city-level filtering. Users can explore the distribution of building usage categories specific to their selected city, making the visualization tailored and insightful. This interactivity simplifies the analysis of city-specific data and makes the chart more engaging.


```
<vegachart schema-url="{{ site.baseurl }}/assets/json/2_interactive_chart.json" style="width: 100%"></vegachart>
```

<vegachart schema-url="{{ site.baseurl }}/assets/json/2_interactive_chart.json" style="width: 100%"></vegachart>

This bar chart dynamically displays the top 30 cities with the highest number of buildings. The chart updates based on the year selected using a slider, allowing users to explore trends in building counts for different time periods.

## Encoding Types:
* X-axis: Encodes City as a nominal variable, sorted by descending building counts.
* Y-axis: Encodes the count of buildings (BuildingCount) as a quantitative variable, showing the number of buildings in each city.
* Color Scheme: Encodes City with a unique color, ensuring clear differentiation between cities.

## Interactivity
* The slider allows users to select a year, dynamically updating the chart to show the top 30 cities with the most buildings constructed up to that year. This interactivity enhances user exploration and enables trend analysis over time, offering a more focused and dynamic view of the data.

## Search The Data & Methods

```
<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/Smeet-Czar/Smeet-Czar.github.io/blob/71c6bd47288b31e25756dd30317ee43e361a653e/python_notebooks/Workbook.ipynb" text="The Analysis" %}
</div>
```

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/Smeet-Czar/Smeet-Czar.github.io/blob/7730b9527e0740fcafa7276fb4856f00e0e5ae4f/python_notebooks/Workbook.ipynb" text="The Analysis" %}
</div>

