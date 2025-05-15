# Mancala Game with AI

A Python implementation of the Mancala board game featuring multiple AI players using minimax algorithm with alpha-beta pruning.

## Features

- Multiple player types:
  - Human Player: Interactive command-line interface
  - Random Computer Player: Makes random valid moves
  - Smart Computer Player: Uses minimax algorithm with alpha-beta pruning
- PIE rule implementation for balanced gameplay
- Time-limited AI move computation
- Command-line interface

## Game Rules

The game follows standard Mancala rules:
- Each player has 6 pits and 1 store
- Initial setup: 4 stones in each pit
- Players take turns moving stones counter-clockwise
- Special rules:
  - Extra turn when last stone lands in player's store
  - Capture opponent's stones when last stone lands in empty pit
  - Game ends when one player's side is empty

## Getting Started

### Prerequisites
- Python 3.x

### Running the Game
```bash
python main.py
```

## Input Format

The game accepts input in the following format:
```
STATE <N> <p1_pits> <p2_pits> <p1_store> <p2_store> <turn> <player>
```
Where:
- N: Number of pits per player (always 6)
- p1_pits: 6 numbers representing Player 1's pits
- p2_pits: 6 numbers representing Player 2's pits
- p1_store: Player 1's store count
- p2_store: Player 2's store count
- turn: Current turn number
- player: Current player (1 or 2)

## Classes

- `MancalaGame`: Main game logic and state management
- `MancalaBoard`: Board representation and move mechanics
- `Player`: Base class for all player types
  - `HumanPlayer`: Interactive player
  - `RandomComputerPlayer`: Random move AI
  - `SmartComputerPlayer`: Minimax AI with alpha-beta pruning

## AI Implementation

The Smart Computer Player uses:
- Minimax algorithm with alpha-beta pruning
- Depth-limited search (default: 5 levels)
- Time-limited move computation (1 second)
- Simple heuristic based on store difference
