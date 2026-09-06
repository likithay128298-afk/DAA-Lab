Implementation of Chain Matrix Multiplication Using Dynamic Programming
Aim
To implement the Chain Matrix Multiplication problem using Dynamic Programming and determine the optimal order of multiplying a sequence of matrices with the minimum number of scalar multiplications.

Objectives
To understand the concept of Matrix Chain Multiplication.
To study the Dynamic Programming approach.
To find the optimal parenthesization of a matrix chain.
To minimize the number of scalar multiplications.
To implement the solution using Python.
To analyze the time and space complexity of the algorithm.

Algorithm
Start.
Read the number of matrices.
Store the dimensions of all matrices in an array p.
Create a DP table dp[i][j] to store the minimum cost of multiplying matrices from i to j.
Initialize the diagonal elements dp[i][i] = 0 because multiplying a single matrix requires no multiplication.
Consider chains of length 2, 3, ..., n.
For each chain, try every possible splitting position k.

Calculate the multiplication cost using:

$$ Cost = dp[i][k] + dp[k+1][j] + p[i-1]\times p[k]\times p[j] $$
Store the minimum cost in dp[i][j].
The final answer is stored in dp[1][n].
Display the minimum number of scalar multiplications.
Stop.

Pseudocode
Algorithm MatrixChainMultiplication(p, n)

Input:
    Array p containing matrix dimensions
    n = number of matrices

Output:
    Minimum number of scalar multiplications

1. Create a table dp[1...n][1...n]

2. For i = 1 to n:
       dp[i][i] = 0

3. For length = 2 to n:
       For i = 1 to n - length + 1:

           j = i + length - 1
           dp[i][j] = infinity

           For k = i to j - 1:

               cost = dp[i][k]
                     + dp[k+1][j]
                     + p[i-1] * p[k] * p[j]

               If cost < dp[i][j]:
                   dp[i][j] = cost

4. Return dp[1][n]

5. Stop
   
Advantages
Efficient: Avoids repeated calculations by storing previously calculated results.
Optimal solution: Finds the minimum number of scalar multiplications.
Simple implementation: The DP table makes the solution systematic and easy to understand.
Avoids redundant subproblems: Each subproblem is solved only once.
Useful in optimization: The technique can be applied to other problems having overlapping subproblems and optimal substructure.

Disadvantages
High time complexity: The time complexity is O(n³).
High space requirement: The DP table requires O(n²) memory.
Does not perform actual matrix multiplication: It only determines the optimal multiplication order.
Less suitable for very large numbers of matrices because the cubic time complexity can become expensive.
Parenthesization requires additional storage if the actual optimal multiplication sequence is also required.

Conclusion
The Chain Matrix Multiplication using Dynamic Programming successfully determines the optimal order of multiplying a sequence of matrices while minimizing the number of scalar multiplications. By storing the results of overlapping subproblems in a DP table, the algorithm avoids unnecessary repeated calculations. Although it requires O(n³) time and O(n²) space, it provides an efficient and systematic solution compared with a brute-force approach.
