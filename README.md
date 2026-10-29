# The Risky Route to Class: Traffic Crashes Near Schools in New York

This notebook was built for a workshop at [GIJN's Investigative Journalism Week](https://gijn.org/stories/ij-week-full-program-release/). It shows how journalists with no coding experience can use ChatGPT or Claude to write Python code for a real data analysis, and how to check the results.

The analysis is based on [The Risky Route to Class](https://teodoracurcic.github.io/lede2025-risky-route-to-class/index.html), which found that two out of three traffic accidents in Belgrade happened within 250 meters of a school. Here the same method is applied to open data from New York City.

---

## How to use it

Every step has a prompt and an empty code cell. Copy the prompt into ChatGPT or Claude, paste the code you get into the cell, and run it. If something breaks, paste the error back into the chat.

Start with the opening prompt in part 1 and keep the whole workshop in one chat, so the AI remembers the names of tables and columns from earlier steps.

You can run the notebook in Jupyter, in VS Code (with the Python and Jupyter extensions) or in Google Colab.

---

## What's in the notebook

0. **Python basics**: cells, variables, lists, a first pandas table and how to read an error
1. **How to work with the AI**: four rules and the opening prompt
2. **Load the crash data**: Brooklyn crashes for 2023 to 2025, downloaded through the NYC Open Data API, one file per year, then combined
3. **Clean the crash data**: dates and times, missing and wrong coordinates, crashes involving pedestrians
4. **Load and clean the school data**: dropping and renaming columns, finding the borough hidden in the school code
5. **Crashes within 250 meters of a school**: coordinates in meters, circles around schools, a spatial join, and a check of whether the result is actually surprising
6. **Which schools are the most exposed**: crashes per school and per neighborhood
7. **Export for maps**: GeoJSON files for Datawrapper, Flourish, QGIS or Mapbox

---

## Data

- [Motor Vehicle Collisions - Crashes](https://data.cityofnewyork.us/Public-Safety/Motor-Vehicle-Collisions-Crashes/h9gi-nx95), NYPD via NYC Open Data
- [2019 - 2020 School Locations](https://data.cityofnewyork.us/Education/2019-2020-School-Locations/wg9x-4ke6), NYC Department of Education via NYC Open Data

---

## Requirements

```
pandas
geopandas>=1.0
```

---

Made by [Teodora Curcic](https://www.linkedin.com/in/teodora-curcic-27a93884/)
