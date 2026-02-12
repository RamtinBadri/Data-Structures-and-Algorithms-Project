# Comparative Analysis of Range Minimum Query (RMQ) Algorithms

A comprehensive benchmarking project analyzing five different data structures and algorithms for solving the **Static Range Minimum Query (RMQ)** problem. This project compares theoretical time complexities against actual runtime performance using Python.

**Repository:** [Data-Structures-and-Algorithms-Project](https://github.com/RamtinBadri/Data-Structures-and-Algorithms-Project)

## Overview

The **Range Minimum Query (RMQ)** problem asks: *Given an array $A$ and two indices $L$ and $R$, what is the minimum value in the subarray $A[L \dots R]$?*

This project implements and benchmarks the following approaches to understand the trade-offs between preprocessing time (Build) and retrieval speed (Query):

1.  **Simple (Brute Force):** Linear scan.
2.  **Sparse Table:** Precomputed power-of-2 intervals (Dynamic Programming).
3.  **Segment Tree:** Binary tree structure for range operations.
4.  **Block Decomposition:** Square root decomposition technique.
5.  **Creative:** A custom optimization mixing Block Decomposition with Sparse Tables.

## Complexity Analysis

| Algorithm | Build Time | Query Time | Space Complexity | Best Use Case |
| :--- | :---: | :---: | :---: | :--- |
| **Simple (Naive)** | $O(1)$ | $O(N)$ | $O(N)$ | Small arrays, one-off queries |
| **Sparse Table** | $O(N \log N)$ | $O(1)$ | $O(N \log N)$ | **Static** data, massive query volume |
| **Segment Tree** | $O(N)$ | $O(\log N)$ | $O(N)$ | **Dynamic** data (updates allowed) |
| **Block Decomp.** | $O(N)$ | $O(\sqrt{N})$ | $O(N)$ | Memory constrained systems |
| **Creative** | $O(N)$ | $O(\sqrt{N})$ | $O(N)$ | Optimized block approach |

> **Note:** While Sparse Table offers the fastest query time ($O(1)$), it requires significantly more preprocessing time and memory. Segment Trees offer the best balance if the array values needed to change (Dynamic RMQ).

## Getting Started

### Prerequisites
*   Python 3.x
*   `matplotlib` (for generating performance charts)

### Installation

1.  Clone the repository:
```bash
git clone https://github.com/RamtinBadri/Data-Structures-and-Algorithms-Project.git
cd Data-Structures-and-Algorithms-Project
