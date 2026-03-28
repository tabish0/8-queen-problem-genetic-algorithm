# 8-Queens Problem using Genetic Algorithm (Python)

This project solves the classic **8-Queens problem** using a simple genetic algorithm approach.

The goal is to place 8 queens on an 8×8 chessboard such that no two queens attack each other.

---

## What it does

* Generates a random population of possible board configurations
* Evaluates each configuration based on number of conflicts (fitness)
* Uses crossover and mutation to create new solutions
* Repeats until a valid solution (0 conflicts) is found

---

## How it works

### Representation (Chromosome)

* Each solution is a list of 8 numbers
* Index = column
* Value = row of the queen

Example:

```
[3, 1, 7, 5, 0, 2, 4, 6]
```

---

### Fitness Function

* Counts how many queens are attacking each other
* Lower fitness is better
* `0` means a valid solution

---

### Genetic Operations

**Selection**

* Best solutions (lowest conflicts) are kept

**Crossover**

* Two-point crossover swaps parts of two solutions

**Mutation**

* Randomly changes a position in the chromosome

---

### Loop

* Evaluate fitness
* Sort population
* Select best candidates
* Apply crossover + mutation
* Replace weaker solutions
* Repeat until solution is found

---

## How to run

1. Make sure Python is installed

2. Run the script:

```bash
python your_file.py
```

---

## Output

* Shows fitness values for each generation
* Prints the best solution found
* Stops when a valid solution is reached

Example:

```
fitness [0, 2, 3, ...]
[3, 1, 7, 5, 0, 2, 4, 6]
Found
```

---

## Notes

* Population size is set to 10
* Board size is fixed at 8×8
* Uses simple genetic operations (not optimized)

---

## Limitations

* Mutation may create duplicate rows (invalid states)
* No guarantee of fastest convergence
* No randomness seed (results vary each run)

---

## Summary

A simple implementation to understand how genetic algorithms can be used to solve constraint problems like the 8-Queens puzzle.
