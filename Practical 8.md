Aim
To implement a Graph data structure and perform Depth First Search (DFS) and Breadth First Search (BFS) traversals using Python.

Objectives
To understand the concept of a Graph data structure.
To represent a graph using an adjacency list.
To implement Depth First Search (DFS).
To implement Breadth First Search (BFS).
To compare DFS and BFS traversal techniques.
To understand the applications of graph traversal algorithms.

Introduction
A Graph is a non-linear data structure consisting of vertices (nodes) and edges connecting them.

Two common graph traversal techniques are:
DFS: Explores as far as possible along one branch before backtracking.
BFS: Explores all neighboring vertices before moving to the next level.

Algorithm

DFS Algorithm
Start from a selected vertex.
Mark the vertex as visited.
Print the vertex.
Visit each unvisited adjacent vertex recursively.
Continue until all reachable vertices are visited.

BFS Algorithm
Start from a selected vertex.
Mark the vertex as visited.
Insert it into a queue.
Remove a vertex from the queue.
Visit all its unvisited adjacent vertices.
Add the newly visited vertices to the queue.
Repeat until the queue is empty.

Pseudocode
DFS
DFS(graph, vertex, visited)

1. Mark vertex as visited
2. Print vertex

3. For each adjacent vertex:
       If adjacent vertex is not visited:
           DFS(graph, adjacent vertex, visited)
4. Stop
   
BFS
BFS(graph, start)

1. Create an empty queue
2. Mark start as visited
3. Add start to queue

4. While queue is not empty:
       vertex = remove from queue
       Print vertex

       For each adjacent vertex:
           If adjacent vertex is not visited:
               Mark it as visited
               Add it to queue

5. Stop

The exact DFS order can vary depending on the order in which adjacent vertices are stored.

Difference Between DFS and BFS

Feature	DFS	BFS
Full Form	Depth First Search	Breadth First Search
Data Structure	Stack / Recursion	Queue
Approach	Goes deep first	Goes level by level
Memory	Generally less for some graph structures	Can require more memory
Shortest path in unweighted graph	Not guaranteed	Guaranteed
Common Applications	Backtracking, cycle detection	Shortest path, level-order traversal

Advantages
DFS
Simple to implement using recursion.
Requires less memory in many cases than BFS.
Useful for cycle detection and backtracking.
Useful for finding connected components.
BFS
Finds the shortest path in an unweighted graph.
Easy to implement using a queue.
Useful for level-by-level traversal.
Useful in network and social-network searches.

Disadvantages
DFS
Does not necessarily find the shortest path.
Recursive implementation can cause stack overflow for very deep graphs.
Can spend a long time exploring one branch before checking others.
BFS
Can require significant memory for graphs with many vertices.
Queue management requires additional space.
Not always efficient for very large or highly connected graphs.

Conclusion
The Graph data structure was successfully implemented using an adjacency list, and both DFS and BFS traversal algorithms were performed. DFS explores a graph deeply before backtracking, while BFS explores the graph level by level. Both algorithms are fundamental graph-search techniques with a time complexity of O(V + E) and are widely used in computer science applications such as path finding, networking, web crawling, and connected-component analysis.
