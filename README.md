# Longest-increasing-path
Difficulty: Hard
Topics: DFS, Dynamic Programming, Graph, Memoization

🧩 Problem Statement

Given an m x n integer matrix, return the length of the longest increasing path in the matrix.

From each cell, you can move in four directions:

Up

Down

Left

Right

You cannot move diagonally or go outside the matrix boundaries.

🚀 Approach

This problem can be solved efficiently using DFS + Memoization (Top-Down DP).

Key Idea:

From each cell, explore all 4 possible directions.

Move only to a neighbor with a strictly greater value.

Use a dp matrix to store the longest increasing path starting from each cell.

This avoids recomputation and ensures optimal performance.

Since the path must be strictly increasing, cycles are impossible. This makes the matrix behave like a Directed Acyclic Graph (DAG).

🧠 Algorithm Steps

Initialize a dp matrix with all values set to 0.

For each cell (i, j):

Run DFS if it hasn’t been computed.

Store the result in dp[i][j].

Keep track of the global maximum path length.

⏱️ Complexity Analysis

Time Complexity: O(m × n)
Each cell is computed once and explores at most 4 directions.

Space Complexity: O(m × n)
For the DP table and recursion stack. 

✅ Key Takeaways

Treat the matrix as a graph.

Use DFS with memoization to avoid repeated work.

Strictly increasing condition guarantees no cycles.

Efficient solution runs in linear time relative to the number of cells.
