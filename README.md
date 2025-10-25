# ♟️ ChessBot: A Python Chess Engine

A fully functional chess engine implemented in Python, featuring both human vs. human and human vs. AI gameplay. The AI uses the Minimax algorithm with Alpha-Beta pruning to make strategic decisions.

## 🚀 Features

- **Complete Chess Implementation**: All standard chess rules including castling, en passant, pawn promotion, and check/checkmate detection
- **Dual Game Modes**: 
  - Player vs Player (PvP)
  - Player vs AI with adjustable difficulty levels
- **Intelligent AI**: Uses Minimax algorithm with Alpha-Beta pruning and move ordering heuristics
- **Flexible Board Representation**: Class-based internal representation with ASCII text interface
- **Comprehensive Move Generation**: Legal move validation with special move handling

## 🧠 AI Capabilities

### Search Algorithm
- **Minimax Algorithm** with configurable search depth
- **Alpha-Beta Pruning** for optimized performance
- **Move Ordering** heuristics to improve pruning efficiency

### Difficulty Levels
- **Easy**: Search depth 2
- **Medium**: Search depth 3  
- **Hard**: Search depth 4

### Evaluation Function
- Piece-value weighted scoring
- Position-based heat maps for strategic piece placement
- Material balance consideration
- Checkmate and stalemate detection

## 🏗️ Project Structure

### Core Components

#### Board Representation
- `Square`: Represents individual board squares
- `Piece`: Base class with subclasses for each piece type (Pawn, Knight, Bishop, Rook, Queen, King)
- `Move`: Encapsulates all move information including special moves
- `Board`: Main board class managing game state and piece positions

#### Move Generation
- Legal move validation with check detection
- Support for all special moves (castling, en passant, promotion)
- Pseudo-legal move generation with filtering

#### AI Engine
- `minmax_alphabeta()`: Main search function
- `order()`: Move ordering for optimal pruning
- `score()`: Position evaluation function

## 📊 Performance

### Time Complexity
- **Worst case**: O(bᵈ) - no move ordering
- **Best case**: O(bᵈ/²) - perfect move ordering  
- **Average case**: O(b³ᵈ/⁴) - with heuristic ordering

Where:
- `b` = average branching factor (~35 in chess)
- `d` = search depth

### Space Complexity
- O(d) due to recursive implementation

## 🎮 Usage

### Game Modes
1. **Player vs Player**: Two human players take turns
2. **Player vs AI**: Play against the computer at chosen difficulty

### Input Format
Moves are entered in coordinate notation:
- **Format**: `initial_squarefinal_square`
- **Example**: `e2e4` (move pawn from e2 to e4)

### Board Perspective
- Choose between White or Black perspective
- Board automatically rotates based on chosen side

## 🔧 Technical Details

### Internal Representation
- 8×8 grid of `Square` objects
- Class-based design for readability
- Comprehensive game state tracking

### Move Validation
- Legal move generation with check verification
- Special move handling (castling, en passant, promotion)
- Game state updates (checkmate, stalemate)

## 🛠️ Installation & Requirements

### Requirements
- Python 3.6+

### Running the Game
Import this file in a Google Colab environment. 
Run every cell and then the "main loop" to play.
