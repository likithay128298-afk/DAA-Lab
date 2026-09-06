Aim
To implement the Making Change Problem using Dynamic Programming and determine the minimum number of coins required to make a given amount of money.

Objectives
To understand the Coin Change/Making Change Problem.
To learn how Dynamic Programming can be used for optimization problems.
To find the minimum number of coins needed for a given amount.
To avoid repeated calculations using a DP table.
To implement the solution using Python.
To analyze the time and space complexity of the algorithm.

Algorithm
Start.
Read the available coin denominations.
Read the target amount.
Create a DP array dp of size amount + 1.
Initialize all values of dp to infinity.
Set dp[0] = 0, because zero coins are required to make amount 0.
For every amount from 1 to the target amount:
Consider every available coin.

If the coin value is less than or equal to the current amount, calculate:

$$ dp[i] = \min(dp[i], dp[i-coin] + 1) $$
After filling the DP table, dp[amount] contains the minimum number of coins.
If the value is still infinity, the amount cannot be formed using the given coins.
Display the result.
Stop.
Pseudocode
Algorithm MakingChange(coins, amount)

Input:
    coins = list of available coin denominations
    amount = target amount

Output:
    Minimum number of coins required

1. Create array dp[0...amount]

2. Set all dp values to infinity

3. Set dp[0] = 0

4. For i = 1 to amount:
       For each coin in coins:

           If coin <= i:
               dp[i] = min(dp[i],
                            dp[i - coin] + 1)

5. If dp[amount] is infinity:
       Print "Change cannot be made"

   Else:
       Print dp[amount]

6. Stop
   
# Main program
coins = list(map(int, input("Enter coin denominations: ").split()))
amount = int(input("Enter the amount: "))

result = making_change(coins, amount)

if result == -1:
    print("Change cannot be made using the given coins.")
else:
    print("Minimum number of coins required:", result)
    
Example
Input:
Enter coin denominations: 1 2 5
Enter the amount: 11

Output:
Minimum number of coins required: 3
Because:
11 = 5 + 5 + 1
Therefore, the minimum number of coins is 3.

Advantages
Efficient: Avoids solving the same subproblem repeatedly.
Optimal solution: Finds the minimum number of coins required.
Easy to implement: The DP table provides a systematic approach.
Works with arbitrary denominations: It is not limited to standard currency denominations.
Handles overlapping subproblems efficiently.

Disadvantages
Memory usage: Requires additional space for the DP array.
Time complexity: Can become expensive for very large target amounts.
Not always the simplest approach: For some standard coin systems, a greedy approach may be faster.
Requires integer denominations in the basic implementation.
If the target amount is very large, the DP table can require significant memory.

Conclusion
The Making Change Problem using Dynamic Programming successfully finds the minimum number of coins required to make a given amount. By storing solutions to previously solved smaller amounts, the algorithm avoids redundant calculations and produces an optimal solution. The approach has a time complexity of O(n × A) and a space complexity of O(A), making it suitable for many coin-change optimization problems.
