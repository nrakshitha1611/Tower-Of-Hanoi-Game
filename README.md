# Tower of Hanoi Game

A Python implementation of the classic **Tower of Hanoi** puzzle using object-oriented programming. This project simulates the game using custom `Node` and `Stack` classes, offering a command-line experience for solving the puzzle interactively.

## 🧠 About the Puzzle

The Tower of Hanoi is a mathematical game consisting of three rods and a number of disks of different sizes. The objective is to move the entire stack from one rod to another, obeying the following rules:

- Only one disk may be moved at a time.
- Each move consists of taking the top disk from one rod and placing it on another.
- No larger disk may be placed on top of a smaller disk.

[Learn more on Wikipedia](https://en.wikipedia.org/wiki/Tower_of_Hanoi)

---

## 📁 Project Structure
```text
Tower-Of-Hanoi-Game/
├── node.py     # Defines the Node class
├── stack.py    # Defines the Stack class
├── script.py   # Main script to run the game
└── README.md   # Project documentation
```

---

## 🚀 Getting Started

### Prerequisites

- Python 3.x installed

### Running the Game

1. Clone this repository:

```bash
git clone https://github.com/nrakshitha1611/Tower-Of-Hanoi-Game.git
cd Tower-Of-Hanoi-Game
```
2. Run the Script:
```bash
python script.py
```
3. Follow the on-screen prompts to play the game by moving disks between rods.

## 📦 Code Overview

### `node.py`

Defines a simple `Node` class that represents an element in a linked list. Each node stores:
- `value`: the data held by the node
- `next_node`: a reference to the next node in the stack

### `stack.py`

Implements a `Stack` class using linked nodes (via the `Node` class). Key methods:
- `__init__(self, name)`: initializes a stack with a name, size, and limit
- `push(value)`: adds a new node to the top of the stack
- `pop()`: removes and returns the top node’s value
- `peek()`: returns the value of the top node without removing it
- `has_space()`: checks if the stack has room for more elements
- `is_empty()`: returns `True` if the stack is empty
- `get_size()`, `get_name()`: utility methods
- `print_items()`: prints the current items in the stack from bottom to top

### `script.py`

Main script that drives the game:
- Prompts the user to enter the number of disks
- Initializes three stacks: left, middle, and right
- Calculates the minimum number of moves using the formula `2 ** num_disks - 1`
- Displays the stacks after each move
- Prompts the player to move disks between stacks while enforcing the Tower of Hanoi rules

This file ties together the logic from `node.py` and `stack.py` into an interactive terminal-based Tower of Hanoi game.

### 🎯 Objective
Move all the disks from the source rod to the destination rod with as few moves as possible, while following the rules of the Tower of Hanoi puzzle.
