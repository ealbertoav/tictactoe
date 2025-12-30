# Tic-Tac-Toe with Minimax AI

A classic Tic-Tac-Toe game featuring an unbeatable AI opponent powered by the Minimax algorithm. Play against a computer that always makes optimal moves!

## Requirements

- Python 3.x
- Pygame library

Install pygame using pip:

```bash
pip install pygame
```

## How to Run

Start the game by running:

```bash
python runner.py
```

## How to Play

1. **Choose Your Side**: When the game starts, click "Play as X" or "Play as O" to select your symbol
   - X always moves first
2. **Make Your Move**: Click on any empty cell to place your symbol
3. **AI Response**: The computer will automatically calculate and make its optimal move
4. **Game End**: The game ends when someone wins (three in a row) or all cells are filled (tie)
5. **Play Again**: Click "Play Again" to start a new game

## Implementation Details

### The Minimax Algorithm

The AI uses the Minimax algorithm, a recursive decision-making algorithm for two-player zero-sum games. It works by:

- **Maximizing**: X tries to maximize the game score (aiming for +1)
- **Minimizing**: O tries to minimize the game score (aiming for -1)
- The algorithm explores all possible future game states to find the optimal move

### Core Functions

| Function | Description |
|----------|-------------|
| `player(board)` | Determines whose turn it is (X or O) based on the current board state |
| `actions(board)` | Returns all possible moves as a set of (row, column) tuples |
| `result(board, action)` | Returns a new board state after applying a move |
| `winner(board)` | Checks for a winner by examining rows, columns, and diagonals |
| `terminal(board)` | Returns True if the game is over (win or tie) |
| `utility(board)` | Returns the score: +1 (X wins), -1 (O wins), or 0 (tie) |
| `minimax(board)` | Calculates and returns the optimal move for the current player |

## Expected Behavior

With optimal play from the AI, **the game should always result in a tie** when both players play perfectly. You should never be able to beat the AI—the best possible outcome is a draw.

## File Structure

```
tictactoe/
├── runner.py          # Game interface using Pygame (handles graphics and user input)
├── tictactoe.py       # Game logic and AI implementation (Minimax algorithm)
├── OpenSans-Regular.ttf  # Font file for the game interface
└── README.md          # This file
```

