Longest Increasing Path in a Matrix
🧩 Problem Statement

Given an m x n integer matrix, return the length of the longest increasing path in the matrix.

From each cell, you can move in four directions:

Up

Down

Left

Right

You may not move diagonally or outside the matrix boundaries.

The next cell in the path must contain a strictly greater value than the current cell.

💡 Approach

This problem can be solved efficiently using Depth First Search (DFS) + Memoization (Dynamic Programming).

🔹 Key Idea

Treat each cell as a starting point.

From each cell, explore all 4 directions.

Move only if the next cell value is greater than the current value.

Store already computed results in a dp table to avoid recomputation.

Since values must be strictly increasing, cycles are impossible.
This makes the matrix behave like a Directed Acyclic Graph (DAG).

🧠 How the Algorithm Works

Create a dp matrix initialized with 0.

For each cell (i, j):

Run DFS to calculate the longest increasing path starting from that cell.

Store the result in dp[i][j].

Keep track of the global maximum length.

Return the maximum value found.

Each cell is computed only once, ensuring efficiency.

⏱️ Complexity Analysis

Time Complexity: O(m × n)
Each cell is processed once and explores at most 4 directions.

Space Complexity: O(m × n)
For the DP table and recursion stack.

✅ Key Takeaways

Model the matrix as a graph.

Use DFS to explore increasing paths.

Use memoization to avoid recomputation.

Strictly increasing condition guarantees no cycles.

Efficient solution runs in linear time relative to the number of cells
