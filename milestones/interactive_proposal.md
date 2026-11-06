# Kaed Esposo

## Description

My static project looked at what is related to academic growth in Chicago public
schools. For the interactive project, I want readers to explore this (and other possible reasons)
on their own.

The main piece is an interactive map of Chicago. It starts zoomed out, with all
of CPS split into regions of the city (North, Northwest, Central, Far South, and
so on). The map starts out plain white, and the reader picks what to color it
by: academic growth, school climate (5Essentials), share of low-income students,
or other measures. Readers can click a region to zoom into its community areas/networks and filter 
by things like school level.
They can also "pin" a few areas or groups and keep them open next to the map to
compare them directly.

I know this is a big plan, so I expect to cut and simplify as I go. The must-haves
are the region map, the "color by" choice, zooming into community areas, and
pinning groups to compare. Things like showing individual schools, comparing by
CPS network, and extra measures are extras I'll add if there's time.

## Plan

**Option:** A (one big interactive), because the map is the centerpiece.

**Tools:** D3.js for the map and charts, and Python to clean the data first.

**Inspiration**
- *270toWin simulation map* (https://www.270towin.com/2024-simulation/): you click
  areas on a map to build something and see the result change. I want that same
  click-to-build feel for choosing groups of schools to compare.
- *Google Public Data Explorer* (https://www.google.com/publicdata/explore): you
  pick several things, compare them side by side, and switch what is being
  measured. That is the idea for my "pin to compare" panel and "color by" menu.

## Mockup

![Mockup](interactive-mockup.png)

*(Image to be added: `milestones/interactive-mockup.png`.)*

A big map on the left, plain white at first, with a "Color by" menu above it. A
panel on the right holds the groups the reader has pinned, so they can see them
side by side. A short note at the bottom explains what the measures mean.

## Data Sources

### Data Source 1: CPS student growth (Academic Progress Indicator)

URL: https://www.cps.edu/about/district-data/metrics/

Size: 42,131 rows, 12 columns

Growth scores for about 600 schools in reading (ELA) and math. This is the main
measure I'm mapping.

### Data Source 2: CPS school demographics

URL: https://www.cps.edu/about/district-data/demographics/

Size: 998 rows, 13 columns

One row per school, with its network, community area, enrollment, and the share
of low-income students. I use this to group schools.

### Data Source 3: Chicago community area boundaries

URL: https://data.cityofchicago.org/Facilities-Geographic-Boundaries/Boundaries-City-Map/ewy2-6yfk

Size: 77 areas

The shapes used to draw the map. I'll group the 77 community areas into regions
myself, since that isn't in the file.

**Extra "color by" options from my static project:** 5Essentials school climate
scores (UChicago Impact), and chronic absence rates and ISBE school ratings
(Illinois State Board of Education).

## Questions

1. The assignment notes say changes are coming this year. Would a map with a
   "color by" menu, zooming in, and pinned comparisons still count as Option A?
2. I need to create a few groupings that aren't in my data, such as regions of
   the city and elementary vs. high school. Is that okay?
3. Does the pinned comparison panel count as enough interactivity, or should I
   add something more?
4. What hosting options will we have for the public site?
