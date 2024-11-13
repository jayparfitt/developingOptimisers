# Developing Optimizers in Python

This project implements and evaluates two optimization algorithms: **Random Search (RS)** and **Simulated Annealing (SA)**. The aim is to approximate the optimal solution for a constrained optimization problem and compare the performance of these algorithms through statistical analysis and visualization.

---

## Table of Contents
1. [Overview](#overview)
2. [Implemented Algorithms](#implemented-algorithms)
3. [Tasks Breakdown](#tasks-breakdown)
4. [Dependencies](#dependencies)
5. [How to Run](#how-to-run)
6. [Results and Analysis](#results-and-analysis)
7. [Files in the Repository](#files-in-the-repository)

---

## Overview

The project focuses on solving a constrained optimization problem where the objective function is subject to multiple constraints. Random Search serves as a baseline algorithm, while Simulated Annealing employs a more sophisticated optimization strategy. The comparison evaluates performance, robustness, and statistical significance of the two methods.

---

## Implemented Algorithms

### Random Search (RS)
- **Type**: Stochastic optimization.
- **Purpose**: Randomly samples solutions within the defined constraints to find the optimal solution.
- **Advantages**:
  - Simple and easy to implement.
  - Provides a baseline for comparison with advanced optimization algorithms.
- **Limitations**:
  - Lack of systematic exploration often results in suboptimal solutions.
  - High variability in results.

### Simulated Annealing (SA)
- **Type**: Metaheuristic optimization inspired by the annealing process in metallurgy.
- **Purpose**: Iteratively improves solutions by accepting better neighbors and occasionally accepting worse ones based on a temperature schedule.
- **Advantages**:
  - Better exploration of the search space.
  - Escapes local minima due to its probabilistic acceptance criterion.
- **Limitations**:
  - Sensitive to parameter tuning (initial temperature, cooling rate, etc.).

---

## Tasks Breakdown

1. **Task 1: Define Functions and Constraints**
   - Implemented the objective function \( f(x) \).
   - Defined the constraints \( g1(x), g2(x), g3(x), g4(x) \).
   - Ensured feasibility through a dedicated `isFeasable` function.

2. **Task 2: Random Search Implementation**
   - Developed a simple stochastic search algorithm.
   - Validated solutions using `isFeasable`.
   - Recorded best solutions and objective values.

3. **Task 3: Simulated Annealing Implementation**
   - Implemented SA with:
     - Feasible initial solution.
     - Neighbor generation with controlled bounds.
     - Cooling schedule for systematic exploration.
   - Tracked the best solution and value across iterations.

4. **Task 4: Performance Evaluation**
   - Ran RS and SA over 21 repetitions each.
   - Visualized results using box plots.
   - Performed a T-Test to assess statistical significance of performance differences.

---

## Dependencies

Ensure the following libraries are installed:
- **Python**: >= 3.8
- **NumPy**: For numerical computations.
- **Matplotlib**: For visualizations.
- **SciPy**: For statistical analysis.

Install dependencies with:
```bash
pip install numpy matplotlib scipy
