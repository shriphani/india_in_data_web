---
title: "Indian Railway Network"
date: 2019-07-30T15:50:02-07:00
draft: true
---

This plot went viral on the [r/India subreddit](https://reddit.com/r/India). No base
map is used. The track LineStrings are plotted as-is and a map of India starts to appear.

The data is from Geofabrik's OSM extracts. We obtained the railway shapefiles and plotted
them as-is (source code in the observable notebooks below).

<figure>
    <img src="/img/railways_3_ig.png" />
    <caption>Railway Tracks of India</caption>
</figure>

The data seems complete but there are a few mis-annotations like the metro networks of 
Bangalore and Delhi which technically are different networks.

To identify underserved bits of the country, we can just plot this over raster tiles
of India. Here is the resulting map.

<figure>
    <img src="/img/railways_overlaid.png" />
    <caption>India Railway Network Overlaid on Raster</caption>
</figure>

The immediate next question is what are the least served bits of India. The sparsity
of a rail network in a region depends on the population density, the terrain (mountains
make things difficult), and geopolitical situations (terrorism). Here are some of the key 
sparse areas in the map.

<figure>
    <img src="/img/railways_sparse.png" />
    <caption>Areas of sparse rail coverage</caption>
</figure>

In clockwise order:

* Srinagar - The capital of India's northernmost state is not connected to the rail network.
* The North-East and Easternmost Parts - These are a new focus area for the railways and possibly within the next few years they will be linked.
* Rajasthan - Desert
* Himalayan Belt - Mountains
* Northern Telanga and Odisha - Forest and volatile political situation

## Data and Source Code

* Datasets: [GeoJSONs](https://github.com/india-in-data/infrastructure_renders)
* Source Code:

    * Rail Network Standalone: [Observable Notebook](https://observablehq.com/@shriphani/transportation-networks-india)
    * Overlaid Rail Network: [Observable Notebook](https://observablehq.com/@shriphani/overlaid-rail-map)