# Artificial Intelligence Foundations and Applications

## Overview

This repository contains homework assignments from an AI course, focused on fundamental techniques including deterministic and heuristic search, logical inference, and decision-making under uncertainty. Each assignment emphasizes practical implementation and reasoning in structured problem settings:

1. **Deterministic Search (HW1):** Implementing search algorithms to control multiple agents in a grid world.
2. **Logical Inference (HW2):** Using logical inference to reason and act in partially observable environments.
3. **Stochastic Decision Making (HW3):** Handling stochastic dynamics and optimizing decisions under uncertainty.

---

## HW1 — Deterministic Search

A deterministic search problem in a Harry Potter–themed environment.

- **Goal:** Control wizards (including Harry Potter) to find and destroy all horcruxes, then defeat Voldemort.
- **Implemented:** A search formulation (e.g. A*) with valid actions: move, wait, destroy horcrux, and kill Voldemort.
- **Challenges:** Death Eaters move along fixed paths; wizards must avoid them when they have one life. The solution uses an admissible heuristic (Manhattan distance, depth penalty) and oscillating death-eater path handling.
- **Main file:** `HW1/ex1.py` — `HarryPotterProblem` class with `actions`, `result`, `goal_test`, and heuristic `h`.

**Challenge:** Designing an accurate heuristic for A* so that optimal solutions are found within a limited number of turns.

---

## HW2 — Logical Inference

Logical reasoning in a partially observable setting (Gringotts Bank).

- **Goal:** Guide Harry through the bank using partial observations (e.g. sulfur, dragons, vaults) to find a target vault while avoiding traps and dragons.
- **Implemented:** A `GringottsController` that maintains a knowledge base (safe, suspicious, dragon, and vault cells) and updates it from observations. Actions include move, collect, and wait.
- **Main file:** `HW2/ex2.py` — `GringottsController` with `get_next_action` and internal inference over observed and inferred cell states.

**Challenge:** Reasoning under uncertainty with limited visibility and avoiding fatal cells (traps, dragons) using logical inference.

---

## HW3 — Stochastic Decision Making

Decision-making under uncertainty with stochastic dynamics.

- **Goal:** Maximize cumulative reward in an environment where death eaters and horcruxes can move probabilistically. Actions include move, destroy horcrux, reset, and terminate.
- **Implemented:** BFS-based and related agents that consider collision probability, horcrux locations, and reward/penalty structure (e.g. destroy horcrux, reset, death-eater catch).
- **Main file:** `HW3/ex3.py` — agents such as `BFSWizard` that combine short-horizon reasoning with the given reward model.

**Challenge:** Designing strategies that adapt to probabilistic movement and maximize expected score (e.g. when to reset or terminate).

---

## Repository Structure

```
AI-Course/
├── HW1/          # Deterministic search (wizards, horcruxes, Voldemort)
├── HW2/          # Logical inference (Gringotts Bank)
├── HW3/          # Stochastic decision making
│   └── Other_Tests/   # Additional test inputs and utilities
└── README.md
```

Each homework folder typically contains:

- Main solution file (`ex1.py`, `ex2.py`, `ex3.py`)
- Utilities and problem definitions (`utils.py`, `problems.py` or similar)
- Checker/validation script (`check.py` or `checker.py`)
- PDF with assignment instructions

---

## Key AI Techniques Covered

- Systematic Search
- Heuristic (Informed) Search
- STRIPS Planning
- Logical Inference and Resolution
- Markov Decision Processes (MDPs)
- Adversarial Planning
- Learning from Feedback

---

## Conclusion

This repository illustrates core AI methods through three assignments: deterministic search with A*, logical inference in partial observability, and stochastic decision-making. Together they give practical experience in search, reasoning, and optimization under uncertainty.
