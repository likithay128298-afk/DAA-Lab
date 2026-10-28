1. Aim
To implement Kruskal’s algorithm to find the Minimum Spanning Tree (MST) of a connected, weighted, undirected graph.

2. Objective
To understand the concept of a Minimum Spanning Tree.
To select edges with minimum weights.
To avoid cycles while selecting edges.
To minimize the total cost of connecting all vertices.

4. Algorithm
Start.
Sort all edges in ascending order of their weights.
Initialize an empty Minimum Spanning Tree.
Select the edge with the minimum weight.
Check whether adding the edge creates a cycle.
If no cycle is formed, add the edge to the MST.
Repeat until the MST contains V − 1 edges, where V is the number of vertices.
Display the selected edges and their total weight.
Stop.

6. Pseudocode
KRUSKAL(Graph):
    MST = empty set
    Sort all edges by increasing weight

    for each edge (u, v, weight):
        if u and v belong to different sets:
            Add edge (u, v) to MST
            Merge the sets of u and v

        if MST contains V - 1 edges:
            break

    Return MST

7. Advantages
Simple and easy to implement.
Efficient for sparse graphs.
Produces a Minimum Spanning Tree with minimum total weight.
The Disjoint Set data structure helps detect cycles efficiently.

9. Disadvantages
Sorting edges requires additional time.
Less efficient for some dense graphs compared with Prim’s algorithm.
A disconnected graph does not produce a single spanning tree.

10. Conclusion
Kruskal’s algorithm was successfully implemented to find the Minimum Spanning Tree of a weighted graph. It selects minimum-weight edges while avoiding cycles and produces a minimum total cost of 19 for the given graph.
Time Complexity: \(O(E \log E)\), where \(E\) is the number of edges.
