# 8-Puzzle Solver

## Project Description
This Python project implements a solution to the 8-puzzle problem, a classic sliding puzzle that consists of a 3x3 grid with 8 numbered tiles and one empty space. The goal is to rearrange the tiles to achieve a specific goal state by sliding tiles into the empty space. The code is designed to solve the puzzle using an informed search algorithm A*, where the cost function is a combination of the actual cost to reach the current state and the estimated cost to reach the goal from the current state. This solver uses two heuristic functions to aid the search:
1. **Manhattan Distance**: The sum of the distances of each tile from its goal position.
2. **Misplaced Tiles**: The count of tiles that are not in their goal position.

## How it works:
- **Libraries**: we used necessary libraries such as `copy`, `numpy`, and `time`.

- **bestsolution Function**: This function traces back the best solution from the goal state to the initial state by keeping track of the moves and states.

- **all Function**: It checks if a state has already been visited to avoid repetition.

- **manhattan Function**: It calculates the Manhattan distance, which is the sum of the absolute values of the horizontal and the vertical distance of the tiles from their goal positions.

- **misplaced_tiles Function**: It counts the number of misplaced tiles compared to the goal state.

- **coordinates Function**: It identifies the coordinates of each tile in the puzzle.

- **evaluvate Function**: This is the main function that evaluates the puzzle using a heuristic method (like Manhattan distance) to find the best solution. It uses a priority queue to keep track of the next best move.

- **Heuristic Methods**: The code includes two heuristic methods to aid the search - Manhattan distance and misplaced tiles.

- **Priority Queue**: The code uses a priority queue to determine the next state to explore based on the lowest cost function.

- **Termination**: The code has a condition to terminate if it takes too long to solve the puzzle, indicating it might be unsolvable.
