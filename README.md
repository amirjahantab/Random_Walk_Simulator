# Random Walk Simulator

This repository contains a Python script for simulating a random walk within a 2D grid, along with analysis on the occurrence of dead ends in the walk.

## Random Walk

A random walk is a mathematical concept describing a path consisting of a succession of random steps. It is a fundamental concept in various fields, including physics, biology, economics, and computer science. In its simplest form, a random walk can be visualized as the movement of a point in a sequence of discrete steps, where each step is chosen randomly from a set of possible directions.

## Algorithm Explanation

The provided Python script (`random_walk.py`) simulates a random walk within a 2D grid. Here's how the algorithm works:

1. **Initialization**: The script takes two command-line arguments: `n` (size of the grid) and `trials` (number of trials to perform).

2. **Main Loop**: For each trial, the algorithm proceeds as follows:

   a. Initialize a 2D grid (`a`) of size `n x n`, where each cell represents a position in the grid. Initially, all cells are marked as unvisited (`False`).

   b. Set the starting position (`x`, `y`) to the center of the grid (`n // 2`, `n // 2`).

   c. While the current position is not at the edge of the grid:

      i. Check if the current position (`x`, `y`) is a dead end. If it is, increment the `dead_ends` counter and exit the loop for the current trial.

      ii. Mark the current position as visited by setting `a[x][y]` to `True`.

      iii. Generate a random number (`r`) between 0 and 1.

      iv. Based on the value of `r`, move the position to one of the adjacent cells (up, down, left, or right), if the destination cell is not already visited.

3. **Output**: After all trials are completed, the script prints the percentage of dead ends encountered during the random walks.

## Usage

To run the script, execute the following command in your terminal:

```
python random_walk.py <grid_size> <num_trials>
```

Replace `<grid_size>` with the desired size of the grid and `<num_trials>` with the number of trials to perform.

## Example

```
python random_walk.py 10 1000
```

This command will simulate 1000 random walks within a 10x10 grid and output the percentage of dead ends encountered.
