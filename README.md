# coin-change
Intuition
The Coin Change problem is a classic example of dynamic programming. The goal is to find the minimum number of coins that you need to make up a given amount of money, given an array of coin denominations. The problem has overlapping subproblems and optimal substructure, making it suitable for dynamic programming solutions.

Approach
Recursion: Start with the target amount and recursively try to reduce it by each coin denomination. If the amount becomes zero, a valid combination is found. If the amount becomes negative, the combination is invalid.

Memoization: To optimize the recursive solution, store the results of subproblems in a memoization table to avoid recomputing them.

Tabulation (Bottom-Up DP): Iteratively build up a solution for the entire problem using the solutions to smaller subproblems. This approach fills a DP table where each entry dp[i] represents the minimum number of coins needed to make the amount i.

Space Optimization: Further optimize the tabulation method by using a single-dimensional array, since the current state only depends on the previous state.

Space and Time Complexity
Recursion
Time Complexity: O(2^n), where n is the target amount. Each coin denomination can lead to a new recursive call.
Space Complexity: O(n), due to the recursion stack.
Memoization
Time Complexity: O(n*m), where n is the target amount and m is the number of coin denominations. Each subproblem is solved only once.
Space Complexity: O(n), for storing the results of subproblems.
Tabulation (Bottom-Up DP)
Time Complexity: O(n*m), similar to memoization.
Space Complexity: O(n), for the DP array.
Space Optimization
Time Complexity: O(n*m), remains the same as tabulation.
Space Complexity: O(n), only a single array is used regardless of the number of coins.
