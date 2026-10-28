1. Aim
To implement the Travelling Salesman Problem (TSP) to find the minimum-cost tour that visits every city exactly once and returns to the starting city.

2. Objective
To find the minimum-cost travelling route.
To understand the brute-force approach.
To calculate the total cost of a tour.

3. Algorithm
Start.
Initialize the distance matrix.
Generate all possible routes between cities.
Calculate the cost of each route.
Select the route with the minimum cost.
Display the optimal route and its cost.
Stop.

4. Pseudocode
TSP(graph, start):
    min_cost = infinity

    Generate all permutations of cities
    excluding the starting city

    for each route:
        cost = distance from start to first city

        Add distances between consecutive cities
        Add distance from last city to start

        if cost < min_cost:
            min_cost = cost
            best_route = route

    Display best_route and min_cost

5. Advantages
Finds the optimal route for small numbers of cities.
Simple to understand and implement.
Useful in route planning and logistics.

6. Disadvantages
Requires a large amount of computation for many cities.
Time complexity increases factorially.
Not suitable for large problems using brute force.

7. Conclusion
The Travelling Salesman Problem was successfully implemented using the brute-force approach to find the minimum-cost tour.
