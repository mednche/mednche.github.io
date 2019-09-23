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
- [Historical calls for service data for Detroit](https://data.detroitmi.gov/Public-Safety/DPD-911-Calls-for-Service-September-20-2016-Presen/wgv9-drfc)
- [Location of Detroit police stations](https://data.detroitmi.gov/Public-Safety/DPD-911-Calls-for-Service-September-20-2016-Presen/wgv9-drfc)
- Open Street Map data (accessed using the [OSMNX python library](https://osmnx.readthedocs.io/en/stable/)). This data contains information on:
  * Infrastructure of the road network (road type, length and number of lanes)
  * Location of traffic lights
  * Speed limit on street segment

For analysis:
- [Boundaries of police districts](https://data.detroitmi.gov/Government/City-Council-Districts/4vse-9zps)

### Methods

In OSMNX, 
- A NetworkX graph (edges are road segments, nodes are intersections)
- 2 geodataframes associated with the networkx (one for nodes and one for edges)

The geodataframes contain information on the edges and nodes as well as a 'geometry' field containing:
- Geometry of a node is a Shapely POINT()
- Geometry of edges is a Shapely LINESTRING()
This is how information on 

In summary, OSMNX uses:
- NetworkX library for manipulating the graph
- Shapely library for geometric objects 

In the first basic ABM implementation, police vehicles move along the road retwork of Detroit to respond to calls for service. They head back to the station when the incident is sorted.

#### 1. Basic movement of agent (node jumping)

The position of agents is recorded as node ID. At ever step, they move along their route (list of nodes) towards a target node (the closest node to the incident's location).

This method presents disadvantages. For example if a road segment (edge) is particularily long (motorway between 2 exits)

#### 2. Improved movement of agents

Coming soon

### Demo for 50 steps
![](/images/project/abm-detroit.gif)

Legend: 
- Green: police stations
- Blue: police vehicles
- Yellow: incident not yet targeted by an agent
- Red: incident currently targeted by an agent


### Value of the Research

Coming soon

### Link to the project code

Coming soon
