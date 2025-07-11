# Nim Game

A classic mathematical strategy game where you play against an unbeatable AI opponent using the Minimax algorithm.

![Nim Game Screenshot](Nim-Game.png)

## How to Run the Game

1. **Download the files**: Ensure you have all the game files in the correct folder structure:
   - `index.html` (main file)
   - `style.css` (styling)
   - `script.js` (game logic and AI implementation)

2. **Open the HTML file**: Double-click on index.html to open it in your web browser

3. **Start playing**: The game will load automatically and you can start playing immediately

## Prerequisites

No installation required! This game runs entirely in your web browser using:

- HTML5 for the structure
- CSS3 for styling and animations
- Vanilla JavaScript for game logic and AI

### Browser Requirements:

- Any modern web browser (Chrome, Firefox, Safari, Edge)
- JavaScript enabled (enabled by default in most browsers)

## How to Play

- **Make Your Move**: Choose how many objects (1, 2, or 3) to take from the pile by clicking the corresponding button
- **AI Response**: The computer will automatically make its move after you
- **Win Condition**: The player who takes the last object from the pile wins
- **Restart**: Click the Restart button at any time to start a new game

### Controls:
- **Button Click**: Click on the "Take 1", "Take 2", or "Take 3" buttons to make moves
- **Restart Button**: Start a new game at any time

## Algorithms Used

This game implements several important algorithms and programming concepts:

### Minimax Algorithm:
- **Purpose**: Ensures the AI makes optimal moves
- **How it works**: Recursively evaluates all possible future game states
- **Result**: The AI is unbeatable when playing from a winning position
- **Time Complexity**: O(3^n) where n is the pile size

### Game Tree Search:
- **Depth-First Search**: Explores game states recursively
- **Backtracking**: Evaluates different move options
- **Scoring System**: Evaluates game states with positive scores for AI wins, negative scores for human wins

### Game State Management:
- **State Representation**: Single variable tracking the pile size
- **Win Detection**: Checks if pile is empty after a move
- **Turn Management**: Alternates between human and AI players

### Event-Driven Programming:
- **DOM Event Handling**: Responds to user button clicks
- **Dynamic Rendering**: Updates UI based on game state changes
- **Async Operations**: Simulates "thinking time" for the AI

## Key Features

- **Clean Interface**: Simple, intuitive design with clear visual feedback
- **Unbeatable AI**: Perfect play from the AI using the minimax algorithm
- **Interactive Buttons**: Responsive controls that adapt to game state
- **Game Status**: Real-time feedback on game state and turn information
- **Modern Styling**: Attractive visual design with gradient background and depth effects

## Implementation Details

The game is built with three main components:

- **HTML Structure**: Provides the basic layout of the game
- **CSS Styling**: Creates an attractive, responsive interface
- **JavaScript Logic**:
  - Game state management
  - Player move handling and validation
  - AI move calculation using minimax
  - Win detection

## Minimax Algorithm Explained

The AI uses the minimax algorithm to determine the best move. Here's a simplified explanation:

1. The AI simulates all possible moves it can make (taking 1, 2, or 3 objects)
2. For each move, it simulates all possible player responses
3. This continues recursively until reaching terminal states (win or loss)
4. Terminal states are assigned scores: +1 for AI win, -1 for player loss
5. The AI chooses the move that leads to the highest score, assuming the player will make optimal moves

This approach makes the AI unbeatable when starting from a winning position. In Nim with a pile of 15 and taking 1-3 objects per turn, the winning strategy is to leave multiples of 4 objects for the opponent.

For detailed implementation guide and code explanations, see [Detailed_Guide.md](Detailed_Guide.md)

## Why the AI is Unbeatable

The minimax algorithm explores all possible future moves and outcomes, essentially "looking ahead" to the end of the game. For Nim, this means the AI can always choose the optimal move that leads to a winning position.

In this specific version of Nim (starting with 15 objects, taking 1-3 per turn), the player who goes first actually has a disadvantage if both players play optimally. The winning strategy is to leave your opponent with a multiple of 4 objects (4, 8, 12).

## Taking It Further

To better understand the code or modify the game, try:

- Changing the initial pile size (currently 15)
- Adding difficulty levels by introducing randomness to the AI's moves
- Implementing a visual representation of the pile
- Adding animations when objects are removed
- Creating a multi-pile version of Nim
- Implementing an undo feature
- Adding sound effects
