# Kaed Esposo

## Description

My static project looked at what is related to academic growth in Chicago public
schools. For the interactive project, I want readers to explore this (and other possible reasons)
on their own.

The main piece is an interactive map of Chicago. It starts zoomed out, with all
of CPS split into regions of the city (North, Northwest, Central, Far South, and
so on). The map starts out plain white, and the reader picks what to color it
by: academic growth, school climate (5Essentials), share of low-income students,
or other measures. Readers can click a region to zoom into its community areas/networks/schools and filter 
by things like school level.
They can also "pin" a few areas or groups and keep them open next to the map to
compare them directly.

## Technical Plan

**Option:** Large interactive

**Tools:** D3.js for the map and charts, and Python (numpy+pandas) to clean the data first.

**Inspiration**
- The interactive maps in the prior year examples that lets you pick what metrics shades the maps (Interactive CPD Stop Analysis Map and State-Level Health Insurance Enrollment Rates
by Demographic Characteristics and Insurance Type)
- *270toWin simulation map* (https://www.270towin.com/2024-simulation/): you click
  areas on a map to build something and see the result change. I want that same
  click-to-build feel for choosing groups of schools to compare.
- *Google Public Data Explorer* (https://www.google.com/publicdata/explore): Similar to the above, you get
  pick the metrics that shades the map, along with what we're comparing (county, city, census tract, etc).

## Mockup
AI was (unfortunately) used to generate this mockup. I gave it the map that I made myself for the static and told it to add the selection box parts as well as the pinned part where you can compare area/schools/regions/etc
![Alt text](milestones/interactive-mockup.png)

## Data Sources
All of the below listed data was used for my static project, so the same exploration as stated in my static proposal has been done!

### Data Source 1: CPS student growth (Academic Progress Indicator)

URL: https://www.cps.edu/about/district-data/metrics/

Size: 42,131 rows, 12 columns

Growth scores for 600 schools in reading (ELA) and math. This is the main
measure I'm mapping.

### Data Source 2: CPS school demographics

URL: https://www.cps.edu/about/district-data/demographics/

Size: 998 rows, 13 columns

One row per school, with its network, community area, enrollment, and the share
of low-income students. I use this to group schools. There are other metrics in this map that can also be
used to shade the map (english learners and students with disabilities).

### Data Source 3: Chicago community area boundaries

URL: https://data.cityofchicago.org/Facilities-Geographic-Boundaries/Boundaries-City-Map/ewy2-6yfk

Size: 77 areas

The shapes used to draw the map. I'll group the 77 community areas into regions
myself. I will have to look for a shape file for networks and how to map specific school.

**Extra "color by" options from my static project:** 5Essentials school climate
scores (UChicago Impact), and chronic absence rates and ISBE school ratings
(Illinois State Board of Education).


