# Highways England Network Graph

A directed network graph of the Strategic Road Netowork (SRN) that is maintained by Highways England (now National Highways). 
The network is built with the published HATRIS link dataset (see our paper for full details) and models two highways (edges, i.e, one for each direction of travel) between each junction (nodes). 
It is assumed that a central crash barrier is always in place and therefore a pair of edges only ever meet at a node.

The network graph is free to use, however I ask that any further publications that use our graph cite the paper where it was published: [Patrol Regimes for Traffic Officers in Transportation Asset Monitoring](https://journals.sagepub.com/doi/full/10.1177/03611981221103243#:~:text=Within%20the%20simulation%2C%20TOs%20patrolled,across%20the%20entire%20highway%20network)

## Data
The file SRN_region_graph.csv contains the graph data, where each row describes a highway section (a directed edge).
StartLat, StartLon, StartX, StarY describe the position (X is Easting and Y is Northing) of the start junction (node) and similarly EndLat/Lon/X/Y describes the end junction position. StartCluster and EndCluster is the node id for the start and end nodes. 
The other columns provide extra detail, like the road and junction name, the straighline distance of each highway section, and the Highways England region where that highway section lies. 
