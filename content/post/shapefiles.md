---
title: "Plotting India: Challenges and Resources"
date: 2019-06-28T17:38:26-07:00
draft: true
tags: india, map, plotting, geojson, topojson
lastmod: 2019-07-05
---

_We discuss the challenges in visualizing Indian geographical datasets, and provide references to reliable maps and sample code using them with the latest version of d3._

The internal state-boundaries of India have changed several times
in the last 20 years thanks to five new states. In our experience, quite a few
Indian maps shipped with popular libraries are outdated.

Additional geopolitical issues make Indian cartography hard.
The Kashmir region in the north is broken up into three
territories administered by India, Pakistan, and China. China also claims
additional territory that is currently administered by India.

Maps of India encountered outside the country exclude (some of) the
disputed territories. However,
most Indians only know (and expect) a map that includes these regions in the mainland.
Not doing so can apparently carry [*significant* legal consequences](https://economictimes.indiatimes.com/news/politics-and-nation/7-year-jail-rs-100-crore-fine-soon-for-showing-pok-arunachal-as-disputed/articleshow/52117889.cms).

Thus, there are 2 map flavors you want - ones that include the disputed territories, and ones that
don't. For a userbase that is based in India (or includes an outsized number of Indians), you might
prefer the former. The latter should be fine for everything else (and is typically the default in many
libraries).

We next provide sample code and map geojson references. All the code used to render these plots
is available from this Observable notebook: [https://observablehq.com/@shriphani/india-map-examples](https://observablehq.com/@shriphani/india-map-examples).

## India With Disputed Areas

The Hindustan Times, a highly regarded national
daily newspaper maintains very high quality geojsons of India with the disputed territories included
in this git repository: [https://github.com/HindustanTimesLabs/shapefiles](https://github.com/HindustanTimesLabs/shapefiles). Here is this map rendered using d3:

<div style="text-align: center">
    <img src="/img/india-with-disputed.png" width="75%"/>
</div>

## India Without Disputed Areas

We are also releasing a set of geojsons obtained from the [GADM project](https://gadm.org/download_country_v3.html). These are highly accurate
and if you want a version of India without the disputed areas these will get the job done. The full
set of geojsons is available from this git repository: [https://github.com/india-in-data/india_maps](https://github.com/india-in-data/india_maps). When rendered with d3, the map of Indian states looks like this:

<div style="text-align: center">
    <img src="/img/india-without-disputed.png" width="75%"/>
</div>

## Centering World Map on India

In a visualization with India as the theme, it is highly advised to center the map around India
else it just looks weird. You can just plug in the longitude to d3's rotate method and it will
take care of the rest. Here is a country map from Natural Earth centered on India:

<div style="text-align: center">
    <img src="/img/india-map-examples-world.png" width="100%"/>
</div>

## Links:

* [Code and rendered map for all the examples shown](https://observablehq.com/@shriphani/india-map-examples)
* [Hindustan Times geojsons for India](https://github.com/HindustanTimesLabs/shapefiles/)
* [GADM sourced geojsons for India without disputed areas](https://github.com/india-in-data/india_maps)
