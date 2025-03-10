# 8-Puzzle-Solver_202401100400192

8-Puzzle Solver using BFS
Problem Statement
The 8-Puzzle is a sliding puzzle that consists of a 3x3 grid with 8 numbered tiles and 1 blank space. The objective of the puzzle is to rearrange the tiles starting from an initial configuration to reach a goal configuration. In this problem, the goal configuration is defined as:
1 2 3
4 5 6
7 8 0
Where 0 represents the blank space.

The puzzle is solved by moving the blank space (represented by 0) to adjacent positions (up, down, left, right) and sliding the adjacent tiles into the blank space. The task is to implement a solution for this puzzle using a search algorithm to find the sequence of moves that will transform the initial state into the goal state.
Approach Taken
In this solution, we have implemented a Breadth-First Search (BFS) algorithm to find the shortest sequence of moves that solves the 8-puzzle problem.
Key Features:
Breadth-First Search (BFS): BFS is used to explore all possible states starting from the initial state. It ensures that the shortest solution (if one exists) is found.
State Representation: The state of the puzzle is represented as a tuple of tuples. This ensures immutability, which is necessary when using data structures like sets and queues for storing visited states and exploring possible moves.
Valid Moves: The possible moves for the blank space (0) are up, down, left, and right. Each move swaps the blank space with the adjacent tile, and the algorithm ensures that the resulting state is valid (within the bounds of the 3x3 grid).
Visited States: The program keeps track of the states it has already visited to avoid redundant calculations and infinite loops.
User Input: The user is prompted to input the initial configuration of the puzzle. This allows for dynamic testing with different puzzle configurations.
Steps to Solve:
Initial State: The program accepts an initial puzzle configuration from the user.
BFS Execution: The BFS algorithm explores all possible states by performing valid moves from the initial state. Each new state is added to a queue and processed. If the goal state is reached, the solution path is returned.
Solution Path: Once the BFS algorithm finds the goal state, it returns the sequence of states that leads to the solution. Each state in the solution path is printed in a human-readable format.
