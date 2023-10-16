# UCS-GBS-A

##Description
This repository contains Python implementations of various search algorithms to solve the classic 8-puzzle problem. The 8-puzzle problem is a sliding puzzle that consists of a 3x3 grid with eight numbered tiles and a blank space. The goal is to rearrange the tiles from their initial state to a goal state, typically in numerical order from 1 to 8, with the blank space in the bottom-right corner.

The implemented search algorithms include:

Breadth-First Search (BFS)
Uniform-Cost Search (UCS)

## Files
puzz.py: Contains the implementation of the EightPuzzleBoard class, which represents the state of the 8-puzzle board, and various search algorithms.
pdqpq.py: Contains a priority queue implementation used by the search algorithms.
test_puzz.py: Contains unit tests for the EightPuzzleBoard class and the search algorithms.
sample_puzzles.txt: Contains sample 8-puzzle instances for testing the algorithms.
README.md: This file, providing an overview of the repository.

## Usage
To solve an 8-puzzle instance using the implemented algorithms, you can run the test_puzz.py file with a specific puzzle instance and search algorithm. For example, to solve a puzzle with the BFS algorithm, use the following command:

python test_puzz.py 123405678 bfs
Replace 123405678 with the initial state of your puzzle. You can also specify different search algorithms (bfs or ucost) and multiple puzzle instances in the sample_puzzles.txt file.

# Implementation Details

EightPuzzleBoard Class
Represents the state of the 8-puzzle board.
Supports generating successor states, finding tile coordinates, and calculating heuristics.
Implements the required methods for hashing, equality comparison, and string representation.
Search Algorithms
Breadth-First Search (BFS):
Explores the search space level by level, ensuring the shortest path to the goal state is found.
Implemented using a queue to manage the frontier.
Uniform-Cost Search (UCS):
Explores the search space by considering the cost of each path from the start state.
Implemented using a priority queue to manage the frontier, where the priority is the total cost of the path.
Priority Queue (pdqpq.py)
Provides an efficient priority queue implementation based on a min-heap.
Supports operations like insertion, deletion, and peeking with logarithmic time complexity.

## Testing
Unit tests for the EightPuzzleBoard class and the search algorithms are available in the test_puzz.py file. You can run the tests using the following command:

python -m unittest test_puzz.py

## Sample Puzzles
The sample_puzzles.txt file contains sample 8-puzzle instances for testing the algorithms. You can add more puzzles to this file following the specified format.

## Note
The provided algorithms are generic and can be applied to any solvable 8-puzzle instance.
Additional search algorithms and heuristics can be added to the puzz.py file if needed.
Feel free to explore, modify, and use these implementations for educational purposes or as a basis for more complex applications involving puzzle-solving algorithms.
