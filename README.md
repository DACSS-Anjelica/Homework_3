# Homework 3 – Diet Optimization with Linear Programming

This project solves a diet optimization problem using linear programming. The goal is to meet minimum daily vitamin and mineral requirements while minimizing total cost.

The problem is modeled and solved using **PuLP** in Python.

---

## Problem Overview

Two vitamin supplements are available:

- **SuperVit**
- **NewHealth**

Each supplement provides different amounts of Vitamin C, Calcium, Iron, Niacin, and Magnesium at different costs. The task is to determine how many tablets of each supplement to take per day in order to meet all minimum nutrient requirements at the lowest possible cost.

---

## Modeling Approach

The decision variables represent the number of tablets taken per day:

- `super_vit`
- `new_health`

The objective function minimizes total daily cost.

Constraints ensure that the minimum daily requirements for each nutrient are met.

---

## Solutions Reported

Two versions of the model are considered:

### 1. Continuous Linear Programming (LP)
- Tablets are allowed to be fractional.
- Optimal solution:
  - SuperVit ≈ 1.30
  - NewHealth ≈ 3.13
  - Minimum cost = **$1.20/day**

### 2. Integer Linear Programming (ILP)
- Tablets must be whole numbers.
- Optimal solution:
  - SuperVit = 3
  - NewHealth = 2
  - Minimum cost = **$1.20/day**

Both approaches achieve the same minimum cost, but the integer solution reflects a more realistic, real-world scenario.

---

## Tools Used

- Python
- PuLP
- CBC Solver
- Jupyter Notebook (via VS Code)

---

## Files

- `homework_3.ipynb` – Contains the full model setup, solution, and results.

---

## Notes

The continuous LP solution is useful for understanding the theoretical optimum, while the integer solution enforces realistic constraints on tablet quantities. Both are included for completeness.
