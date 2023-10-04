# Highways England Network Graph

A directed network graph of the Strategic Road Netowork (SRN) that is maintained by Highways England (now National Highways). 
The network is built with the published HATRIS link dataset (see our paper for full details) and models two highways (edges, i.e, one for each direction of travel) between each junction (nodes). 
It is assumed that a central crash barrier is always in place and therefore a pair of edges only ever meet at a node.

The network graph is free to use, however I ask that any further publications that use our graph cite the paper where it was published: [Patrol Regimes for Traffic Officers in Transportation Asset Monitoring](https://journals.sagepub.com/doi/full/10.1177/03611981221103243#:~:text=Within%20the%20simulation%2C%20TOs%20patrolled,across%20the%20entire%20highway%20network)

## Data

### SRN_region_graph.csv
The file SRN_region_graph.csv contains the graph data, where each row describes a highway section (a directed edge).
The columns StartLat, StartLon, StartX, and StartY describe the position (X is Easting and Y is Northing) of the start junction (node) and similarly EndLat/Lon/X/Y describes the end junction position. StartCluster and EndCluster are respectively the start and end node id.
The other columns provide extra detail, like the highway and junction name, the straighline distance of each highway section, and the Highways England region where that highway section lies. 

The graph contains a small number of self loops which are a result of the processing steps performed to turn the HATRIS links into a connected graph (namely merging junctions with the same name, but different positional coorindates). 
These loops can be simply removed - see the provided notebook. 

### SRN_graph_loading_example.ipynb
A notebook demonstrating how to create a directed graph in networkx, as well as a visualisation. 
