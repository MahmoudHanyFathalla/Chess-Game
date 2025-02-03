# Chess Game 

This is a simple Python-based chess game implementation with an interactive console interface. The game features classic chess rules, including the concept of "check" and "checkmate," and allows players to move pieces in algebraic notation (e.g., e2 e4). The game includes a variety of chess pieces, each with its unique movement logic, and supports the full set of chess moves.

## Features

- **Interactive Console Input:** Players enter their moves in standard algebraic notation (e.g., "e2 e4").
- **Piece Movement:** Each piece follows the rules of chess, including special movements like castling for the King and en passant for the Pawn.
- **Check and Checkmate Detection:** The game checks if a player's King is in check and verifies checkmate conditions.
- **Pawn Promotion:** Pawns can be promoted when reaching the opposite side of the board.
- **Board Representation:** The chessboard is represented in a row-column format, and each square can contain a chess piece or be empty.

## Setup

To run this chess game, ensure that you have Python installed on your system (Python 3.x). You can simply copy and run the code in a Python interpreter.

## Usage

1. Run the script.
2. The game will prompt you for moves in algebraic notation.
3. Enter a move, such as `e2 e4` (moves the pawn from e2 to e4).
4. The game will update the board and check for any "check" or "checkmate" situations after each move.

### Example Move Input

```
e2 e4
```

### Board Display

```
   1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 
--------------------------------  
a|♖ | ♙ |   |   |   |   | ♟ | ♜ | 
--------------------------------  
b|♘ | ♙ |   |   |   |   | ♟ | ♞ | 
--------------------------------  
c|♗ | ♙ |   |   |   |   | ♟ | ♝ | 
--------------------------------  
d|♕ | ♙ |   |   |   |   | ♟ | ♚ |
--------------------------------
e|♔ | ♙ |   |   |   |   | ♟ | ♛ |
--------------------------------
f|♗ | ♙ |   |   |   |   | ♟ | ♝ |
--------------------------------
g|♘ | ♙ |   |   |   |   | ♟ | ♞ |
--------------------------------
h|♖ | ♙ |   |   |   |   | ♟ | ♜ |
--------------------------------
```

## Code Overview

### Classes:

- **Game Class:** Manages the game loop, board, and player turns. It handles the main game logic including input parsing, move validation, and check/checkmate detection.
- **Piece Class:** A base class for all chess pieces. It defines basic behaviors such as checking if a move is valid and determining available moves.
- **Specific Piece Classes:** Derived classes for each chess piece (Pawn, Rook, Knight, Bishop, Queen, King). Each has its own logic for available moves.
  
### Methods:

- **`isValid()`**: Checks whether a move is valid for a specific piece.
- **`availableMoves()`**: Returns the list of available moves for a piece.
- **`parseInput()`**: Converts algebraic notation input into board coordinates.
- **`isCheck()`**: Checks if the player's King is in check.
- **`isCheckmate()`**: Checks if the player's King is in checkmate.

### Special Pieces Logic:

- **Pawn**: Moves one square forward but can capture diagonally. It has special rules for its first move and promotions.
- **Rook**: Moves horizontally or vertically any number of squares.
- **Knight**: Moves in an "L" shape (two squares in one direction and one in a perpendicular direction).
- **Bishop**: Moves diagonally any number of squares.
- **Queen**: Combines the movement abilities of both the Rook and the Bishop.
- **King**: Moves one square in any direction.

## Conventions

- The board is represented using row-column coordinates starting from the bottom left (0,0). The columns are labeled from 'a' to 'h', and the rows are labeled from 1 to 8.
- The game handles both white and black pieces, with different Unicode symbols for each piece.
