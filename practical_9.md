Aim
To implement Prim’s Algorithm to find the Minimum Spanning Tree (MST) of a connected, weighted, undirected graph.

 Objective
* To understand Prim’s Algorithm.
* To find the Minimum Spanning Tree of a graph.
* To select edges with minimum weight without forming a cycle.
* To calculate the minimum total cost of connecting all vertices.

Algorithm
   
*Start.
*Read the number of vertices and the adjacency matrix.
*Select the starting vertex.
*Mark the starting vertex as visited.
*Find the minimum-weight edge connecting a visited vertex to an unvisited vertex.
*Add the selected edge to the Minimum Spanning Tree.
*Mark the new vertex as visited.
*Repeat steps 5–7 until all vertices are visited.
*Display the edges of the Minimum Spanning Tree and their total cost.
*Stop.

Pseudocode
START

Read number of vertices V
Read adjacency matrix graph[V][V]

Initialize visited[V] = false
Set visited[0] = true
Set totalCost = 0

Repeat V-1 times:
    min = INFINITY

    For i = 0 to V-1:
        If visited[i] is true:
            For j = 0 to V-1:
                If visited[j] is false AND
                   graph[i][j] != 0 AND
                   graph[i][j] < min:

                    min = graph[i][j]
                    u = i
                    v = j

    If min is INFINITY:
        Print "Graph is disconnected"
        STOP

    Print edge u-v and its weight
    visited[v] = true
    totalCost = totalCost + min

Print totalCost

STOP
Note: This program uses 0 to represent the absence of an edge, so it is intended for graphs with positive edge weights. The value 9999 represents infinity for this implementation.


 Advantages
Finds the Minimum Spanning Tree efficiently.
Avoids cycles while selecting edges.
Works well for connected, weighted, undirected graphs.
Can be implemented using adjacency matrices or priority queues.

 Disadvantages
The basic adjacency-matrix implementation takes O(V²) time.
It requires a connected graph to produce a spanning tree.
It may be less efficient for sparse graphs than suitable priority-queue implementations.
The basic implementation is not suitable for directed graphs.

 Conclusion
Thus, Prim’s Algorithm was successfully implemented in C++ to find the Minimum Spanning Tree of a connected, weighted, undirected graph. The algorithm selects minimum-weight edges to connect all vertices without forming cycles and calculates the minimum total cost.
