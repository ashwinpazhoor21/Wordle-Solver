# Wordle Solver Implementation

## Description

This project involves implementing a solver for the popular word-guessing game Wordle, building upon a previous implementation of the game. The solver can operate in two modes: 

1. **Specified Word Mode**: The secret word is known and specified by the user, allowing the program to efficiently narrow down the possible words until it finds the secret word.
2. **Interactive Mode**: The solver iteratively suggests guesses to the user, helping them find the solution to a live Wordle puzzle.

### Features

- **Optimal Guess Selection**: The solver uses a heuristic approach, selecting words based on the frequency of unique letters in the remaining possible vocabulary.
- **Vocabulary Pruning**: The solver reduces the list of possible words after each guess based on the feedback received (gray, yellow, and green responses).

### Key Files

- **`solver.c`**: Main driver for the Wordle solver, managing user interaction and guessing logic.
- **`search_util.c`**: Contains core functions for the solver, including vocabulary management and heuristic calculations.
- **`search_util.h`**: Header file with function declarations.
- **`demo_functions.c`**: Space for testing and demonstrating the functions implemented in `search_util.c`.
- **`Makefile`**: Builds the project with appropriate compilation flags.

### Data Structures

The project uses dynamic data structures to manage the vocabulary and track potential solutions:

- **Arrays**: Used to store the list of possible words and track eliminated options.
- **Dynamic Memory Management**: Allocates and frees memory for strings and arrays as the solver progresses through the guessing process.

### Usage

To run the solver with a specified secret word:

```bash
$ ./solver motif