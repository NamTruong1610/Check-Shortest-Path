# C++ Graph Library and Algorithms

This repository contains a template-based Graph library implemented in C++ along with a suite of algorithms and test cases. The project demonstrates common graph operations such as checking subgraphs, verifying tree structures (with isolated vertices), computing path lengths from a given root, and testing edge relaxation conditions.

## Project Structure

- **graph.hpp**  
  Contains the implementation of the `Graph` class template and several related functions:
  - **Graph Class:** Provides a representation of a directed graph using an adjacency list.
  - **Edge Operations:** Adding, removing, and querying edges.
  - **Graph Algorithms:**  
    - `isSubgraph`: Checks if one graph is a subgraph of another.
    - `isTreePlusIsolated`: Determines whether the graph forms a tree (from a given root) plus any isolated vertices.
    - `pathLengthsFromRoot`: Computes shortest path distances from a root vertex using a breadth-first style approach.
    - `allEdgesRelaxed`: Validates if a given distance vector satisfies the edge relaxation condition.

- **main.cpp**  
  Contains a comprehensive suite of test cases written using the [Google Test framework](https://github.com/google/googletest). These tests verify the correctness of graph operations and algorithms under various conditions, including:
  - Verifying subgraph conditions.
  - Testing tree properties with or without isolated vertices.
  - Evaluating path length calculations.
  - Assessing the edge relaxation criteria in multiple scenarios.

## Getting Started

### Prerequisites

- A C++ compiler with C++17 support (e.g., `g++` or `clang++`).
- [Google Test](https://github.com/google/googletest) framework installed on your system for running the test cases.

### Compilation

You can compile the project from the terminal. For example, if you are using `g++` and have Google Test properly set up, you might compile with a command similar to:

```bash
g++ -std=c++17 -I/path/to/googletest/include -L/path/to/googletest/lib main.cpp -lgtest -lgtest_main -pthread -o runTests
