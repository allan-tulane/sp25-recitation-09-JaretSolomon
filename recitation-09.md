Jaret Solomon

2) 
If the graph has K nodes and E edges, and is made up of k connected components, then the worst-case work of the modified Prim's algorithm is O(E + K log K).

Each edge is considered at most once when it's added to the priority queue, contributing O(E) work.
Each node is processed once, and priority queue operations (insertions and updates) cost log K, giving O(K log K) total work.
Since we're running Prim's separately on each component, the cost is still bounded by the total number of edges and nodes.


4) 
The overall work is O(n² log n), where n is the number of cities.

We start by constructing a complete graph where each of the n cities is connected to every other city. This results in O(n²) edges.
For each of these n² edges, we compute the Euclidean distance, and then apply Prim's algorithm.
Since Prim’s uses a priority queue and touches each node with log n operations, the total work is O(n² log n).
