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

Coming soon

### Data 

In order to make the simulation more realistic, the following data was incorporated:
- [Historical calls for service data for Detroit](https://data.detroitmi.gov/datasets/911-calls-for-service?geometry=-86.058%2C42.028%2C-80.785%2C42.738)
- [Location of Detroit police stations](https://data.detroitmi.gov/Public-Safety/DPD-911-Calls-for-Service-September-20-2016-Presen/wgv9-drfc)
- Open Street Map data (accessed using the [OSMNX python library](https://osmnx.readthedocs.io/en/stable/)). This data contains information on:
  * Infrastructure of the road network (road type, length and number of lanes)
  * Location of traffic lights
  * Speed limit on street segment

For analysis:
- [Boundaries of police precincts](https://data.detroitmi.gov/datasets/dpd-precincts?geometry=-83.758%2C42.264%2C-82.440%2C42.442)
- [Boundaries of council districts](https://data.detroitmi.gov/Government/City-Council-Districts/4vse-9zps)

### Methods

When using OSMNX for a given city, the structure of the data consists in: 
- A NetworkX graph (edges are road segments, nodes are intersections)
- 2 geodataframes associated with the networkx (one for nodes and one for edges)

The geodataframes contain information on the edges and nodes as well as a 'geometry' field containing:
- Geometry of a node is a Shapely POINT()
- Geometry of edges is a Shapely LINESTRING()

In summary, OSMNX uses:
- NetworkX library for manipulating the graph
- Shapely library for geometric objects 



#### Agent movement

The position of a given police vehicle is recorded as **node ID**. At ever step, they move along the road network following a **route** (list of nodes) towards a target node (the closest node to the incident's location).

This method presents disadvantages. For example if a road segment (edge) is particularily long (motorway between 2 exits).


#### Idle strategy

Before running the simulation, an idle strategy is chosen that will apply to all agents. When idle they can:
- remain stationnary
- return to their station
- patrol nearby hot streets


### Demo for 50 steps
![](/images/project/abm-detroit2.gif)

Purple segments represent *hot streets* based on historical CFS/crime data.


### Value of the Research

Coming soon

### Link to the project code

Coming soon
