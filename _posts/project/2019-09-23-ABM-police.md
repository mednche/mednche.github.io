---
layout: posts
small-title: ABM police dispatch
big-title: ABM of police dispatch
feature-img: "/images/project/route-explained.jpg"
thumbnail: "/images/project/thumbs/route-explained.jpg"
tags: [python, ABM, policing]
teaser: An ABM of police dispatch in Detroit
---



### Project Background



### Data 

In this simulation, 
- [historical calls for service data for Detroit](https://data.detroitmi.gov/Public-Safety/DPD-911-Calls-for-Service-September-20-2016-Presen/wgv9-drfc)
- [location of Detroit police stations](https://data.detroitmi.gov/Public-Safety/DPD-911-Calls-for-Service-September-20-2016-Presen/wgv9-drfc)
- Open Street Map data (accessed using the [OSMNX python library](https://osmnx.readthedocs.io/en/stable/)). This data contains information on:
  * infrastructure of the road network (road type, length and number of lanes)
  * location of traffic lights
  * speed limit on street segment

For analysis:
- [Boundaries of police districts]https://data.detroitmi.gov/Government/City-Council-Districts/4vse-9zps)

### Methods


In the first basic ABM implementation, police vehicles move along the road retwork of Detroit to respond to calls for service. They head back to the station when the incident is sorted.

#### Basic movement of agent (node jumping)


#### Improved movement of agents




### Demo for 50 steps
![](./abm-detroit.gif)

Legend: 
- Green: police stations
- Blue: police vehicles
- Yellow: incident not yet targeted by an agent
- Red: incident currently targeted by an agent


### Value of the Research

### Link to the project code

Private repo for the moment
