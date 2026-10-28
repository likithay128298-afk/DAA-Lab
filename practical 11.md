1. Aim
To implement the Floyd–Warshall algorithm to find the shortest paths between all pairs of vertices in a weighted graph.

2. Objective
To calculate the shortest distances between all pairs of vertices.
To understand the concept of dynamic programming.
To update distances using intermediate vertices.

3. Algorithm
Start.
Initialize the distance matrix with edge weights.
Consider each vertex as an intermediate vertex.

Update the distance using the formula:

$$ D[i][j] = \min(D[i][j], D[i][k] + D[k][j]) $$
Repeat for all vertices.
Display the shortest distance matrix.
Stop.

4. Pseudocode
FLOYD_WARSHALL(D, V):
    for k = 0 to V-1:
        for i = 0 to V-1:
            for j = 0 to V-1:
                D[i][j] = min(D[i][j],
                              D[i][k] + D[k][j])

    return D

6. Advantages
Finds shortest paths between all pairs of vertices.
Simple to implement.
Works with negative edge weights if there are no negative-weight cycles.

8. Disadvantages
Requires \(O(V^3)\) time.
Requires \(O(V^2)\) space.
Can be inefficient for large graphs.

10. Conclusion
the Floyd–Warshall algorithm was successfully implemented to find the shortest distances between all pairs of vertices using dynamic programming.
Time Complexity: \(O(V^3)\)
Space Complexity: O(V^2)
