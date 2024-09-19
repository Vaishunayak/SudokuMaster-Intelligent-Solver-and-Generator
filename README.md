# SudokuMaster: Intelligent Solver and Generator

**SudokuMaster** is an intelligent Sudoku solver and generator written in Java. This application can generate random Sudoku puzzles and solve them using backtracking. It's designed to fill Sudoku grids while ensuring that the solutions are valid according to Sudoku rules.

## Features

- **Sudoku Puzzle Generator**: Generates a random, valid Sudoku puzzle by filling diagonal blocks and then backtracking to fill the rest of the grid.
- **Sudoku Solver**: Solves any valid Sudoku puzzle using a backtracking algorithm.
- **Adjustable Difficulty**: You can control the number of cells removed to customize the puzzle's difficulty.
- **User-friendly Output**: Prints the generated puzzle and the solution in a grid format.

## Project Structure

The project contains a single class, `SudokuSolver`, which is responsible for generating and solving Sudoku puzzles. Below is a brief overview of its core methods:

### Methods

- **`solveSudoku(int[][] board)`**: Solves the given Sudoku puzzle using backtracking.
- **`isSafe(int[][] board, int row, int col, int num)`**: Checks if placing a number in the given position is valid.
- **`generateSudokuPuzzle()`**: Generates a Sudoku puzzle by filling a grid and removing numbers.
- **`fillDiagonalBlocks(int[][] board)`**: Fills the diagonal 3x3 blocks of the grid with random numbers.
- **`fillBlock(int[][] board, int row, int col)`**: Fills a 3x3 block with random unique numbers.
- **`fillRemaining(int[][] board, int row, int col)`**: Recursively fills the remaining cells of the Sudoku grid using backtracking.
- **`removeNumbers(int[][] board)`**: Removes numbers from the generated grid to create a playable puzzle.
- **`printBoard(int[][] board)`**: Prints the Sudoku grid in a readable format.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/SudokuMaster.git
   cd SudokuMaster
   ```

2. Compile the code:
   ```bash
   javac SudokuSolver.java
   ```

3. Run the application:
   ```bash
   java SudokuSolver
   ```

## Usage

Once you run the application, it will:

1. Generate a Sudoku puzzle.
2. Print the generated puzzle in the console.
3. Solve the puzzle and print the solution.

### Example Output:

```
Generated Sudoku Puzzle:
5 3 0 0 7 0 0 0 0 
6 0 0 1 9 5 0 0 0 
0 9 8 0 0 0 0 6 0 
8 0 0 0 6 0 0 0 3 
4 0 0 8 0 3 0 0 1 
7 0 0 0 2 0 0 0 6 
0 6 0 0 0 0 2 8 0 
0 0 0 4 1 9 0 0 5 
0 0 0 0 8 0 0 7 9 

Solved Sudoku:
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

## Customization

### Difficulty Level
You can adjust the difficulty level by modifying the `DIFFICULTY` constant in the `SudokuSolver` class:
```java
private static final int DIFFICULTY = 40;
```
Increasing this value will remove more numbers from the puzzle, making it harder to solve.

## Contributing

Contributions are welcome! If you'd like to enhance the functionality or improve the code, feel free to fork the repository and submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

