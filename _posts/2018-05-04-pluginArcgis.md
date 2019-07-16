---
layout: posts
title: Mapping burglary risk
feature-img: "images/BurglaryRisk.png"
thumbnail: "images/BurglaryRisk.png"
tags: [Python, ArcGIS, arcpy]
teaser: A Python addin for ArcGIS written with arcpy.
excerpt_separator: <!--more-->
---

A Python addin for ArcGIS written with arcpy.
<!--more-->


Manchester police, based on work by a variety of people, have found that in general, if somewhere is burgled, there is an increased risk of burglary for the houses within 400m of the burgled house for up to 4 weeks. This is known as the Trafford Model.

This addin buffers a burglary file and then list the houses in an area by chance of burglary. Those houses that fall inside the most buffers will have the largest burglary risk. As our area is a rather small corner of the East End of London, we've used 80m buffers.

This addin displays the houses with the highest risk as a choropleth map, coloured by risk, and an associated sorted table.

<p align="center">
  <img src="/images/BurglaryRisk.png">
</p>

More information can be found in the [**Github repository**](https://github.com/mednche/AdvancedProgrammingSkills/tree/master/AddinArcGIS)
