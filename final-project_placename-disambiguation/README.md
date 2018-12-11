## Component of natural language processing final course project. 

- Task is to disambiguate a list of location names in a document by considering the presence of other locations names in the document.

- For example, if the name "London" is detected in a text we must predict whether the author is referring to London, Ontario or London, UK by examining the context of the paper, where in this this case, context corresponds to the other locations mentioned in the paper.

- We design a heuristic that assigns a (longitude, latitude) pair to each place name by finding the set of (longitude, latitude) pairs that minimize a minimum spanning tree where distance is defined by the [great-circle distance](https://en.wikipedia.org/wiki/Great-circle_distance) between two (longitude, latitude) pairs computed by the [haversine formula](https://en.wikipedia.org/wiki/Haversine_formula). 

- [Prim's algorithm](https://en.wikipedia.org/wiki/Prim%27s_algorithm) was used to compute the minimum spanning tree. 

- An exhaustive search of all possible map combinations is not feasible. Therefore, we propose a greedy approach that iteratively adds (longitude, latitude) nodes from a list of options that minimizes the cost of the overall minimum spanning tree.  
