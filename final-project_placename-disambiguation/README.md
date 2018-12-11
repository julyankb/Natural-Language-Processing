## Component of Natural language processing course final project. 

- Task is to disambiguate a list of locations by considering its distance to other locations in the paper. 

- We design a heuristic that assigns a (longitude, latitude) pair to each place name by finding the set of (longitude, latitude) pairs that minimize a minimum spanning tree where distance is defined by the haversine distance (1) between two (longitude, latitude) pairs. 

- Prim's algorithm was used to compute the minimum spanning tree. 

- An exhaustive search of all possible map combinations is not feasible. Therefore, we propose a greedy approach that iteratively adds (longitude, latitude) nodes from a list of options that minimizes the cost of the overall minimum spanning tree.  
