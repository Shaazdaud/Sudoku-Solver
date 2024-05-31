# Sudoku Solver README

## Introduction

This Sudoku Solver is a C program designed to solve 9x9 Sudoku puzzles using a backtracking algorithm. It reads a Sudoku grid from the user, solves it if possible, and then prints the solved grid.

## Features

- Reads a 9x9 Sudoku grid from the user.
- Uses a backtracking algorithm to find a solution.
- Checks the safety of placing numbers in the grid using Sudoku rules.
- Prints the solved Sudoku grid or notifies if no solution exists.

## Files

- `sudoku_solver.c`: Contains the implementation of the Sudoku solver.

## Functions

### `void print(int arr[N][N])`
Prints the Sudoku grid.

- `arr`: 2D array representing the Sudoku grid.

### `int isSafe(int grid[N][N], int row, int col, int num)`
Checks if placing `num` in `grid[row][col]` is safe according to Sudoku rules.

- `grid`: 2D array representing the Sudoku grid.
- `row`: Row index.
- `col`: Column index.
- `num`: Number to place in the grid.
- Returns `1` if it's safe to place `num`, otherwise returns `0`.

### `int solveSudoku(int grid[N][N], int row, int col)`
Recursively attempts to solve the Sudoku puzzle using backtracking.

- `grid`: 2D array representing the Sudoku grid.
- `row`: Row index to start solving.
- `col`: Column index to start solving.
- Returns `1` if the Sudoku is solved, otherwise returns `0`.

## Usage

1. Compile the program using a C compiler, for example:
   ```bash
   gcc sudoku_solver.c -o sudoku_solver
   ```

2. Run the compiled program:
   ```bash
   ./sudoku_solver
   ```

3. Enter the Sudoku grid values row by row, using `0` for empty cells. For example:
   ```
   Enter the sudoku grid (0 for empty cell):
   5 3 0 0 7 0 0 0 0
   6 0 0 1 9 5 0 0 0
   0 9 8 0 0 0 0 6 0
   8 0 0 0 6 0 0 0 3
   4 0 0 8 0 3 0 0 1
   7 0 0 0 2 0 0 0 6
   0 6 0 0 0 0 2 8 0
   0 0 0 4 1 9 0 0 5
   0 0 0 0 8 0 0 7 9
   ```

4. The program will print the solved Sudoku grid if a solution exists. If no solution exists, it will notify you.

## Example

### Input
```
5 3 0 0 7 0 0 0 0
6 0 0 1 9 5 0 0 0
0 9 8 0 0 0 0 6 0
8 0 0 0 6 0 0 0 3
4 0 0 8 0 3 0 0 1
7 0 0 0 2 0 0 0 6
0 6 0 0 0 0 2 8 0
0 0 0 4 1 9 0 0 5
0 0 0 0 8 0 0 7 9
```

### Output
```
5 3 4 6 7 8 9 1 2
6 7 2 1 9 5 3 4 8
1 9 8 3 4 2 5 6 7
8 5 9 7 6 1 4 2 3
4 2 6 8 5 3 7 9 1
7 1 3 9 2 4 8 5 6
9 6 1 5 3 7 2 8 4
2 8 7 4 1 9 6 3 5
3 4 5 2 8 6 1 7 9
```

## Notes

- Ensure that the input grid contains valid Sudoku values (1-9) and 0 for empty cells.
- The program does not validate the initial grid for consistency according to Sudoku rules; it assumes the input is a valid puzzle that can be solved.

## License

This project is open source and available under the [MIT License](https://opensource.org/licenses/MIT).