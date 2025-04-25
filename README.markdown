# Connect Four Game with AI

## Overview

This project implements a **Connect Four** game using Python, featuring a graphical user interface (GUI) built with Pygame. The game allows a human player to compete against an AI opponent, which uses different strategies to make moves:

- **Minimax with Alpha-Beta Pruning**: An optimized AI algorithm that evaluates game states to select the best move, with configurable difficulty levels (Easy, Medium, Hard).
- **Minimax without Alpha-Beta Pruning**: A less efficient version of the Minimax algorithm, also with configurable difficulty levels.
- **Heuristic-based AI**: A simpler AI that selects moves based on a heuristic evaluation of the board, prioritizing immediate opportunities and threats.

The game includes a user-friendly interface with a main menu, color selection for pieces (red or yellow), and difficulty selection for the Minimax-based AIs.

## Features

- **Interactive GUI**: Built with Pygame, featuring a main menu, color selection, and difficulty selection screens.
- **AI Opponents**:
  - Minimax with Alpha-Beta Pruning (optimized for faster performance).
  - Minimax without Alpha-Beta Pruning (slower but simpler).
  - Heuristic-based AI for quick, less computationally intensive gameplay.
- **Customizable Gameplay**:
  - Choose piece colors (Red or Yellow) for the human player and AI.
  - Select difficulty levels (Easy, Medium, Hard) for Minimax-based AIs.
- **Game Mechanics**:
  - Standard Connect Four rules: Players take turns dropping pieces into a 6x7 grid, aiming to connect four pieces horizontally, vertically, or diagonally.
  - Supports win detection, draw detection, and game-over states.
- **Visual Feedback**:
  - Displays the game board with colored pieces.
  - Shows win/draw messages and transitions back to the main menu after a game ends.

## Requirements

- **Python 3.x**
- **Pygame**: For rendering the GUI and handling user input.
- **NumPy**: For efficient board representation and manipulation.

Install the required dependencies using:

```bash
pip install pygame numpy
```

## File Structure

- `main.py`: The main game script containing the game logic, AI algorithms, and GUI implementation.
- `button1.py`: A custom Button class for handling interactive buttons in the GUI.
- `pics/`: Directory containing assets:
  - `Background.png`: Background image for the menu screens.
  - `Play Rect.png`: Button image for "Play" and other options.
  - `Quit Rect.png`: Button image for the "Quit" option.
  - `font.ttf`: Custom font for text rendering.
- `README.md`: This file, providing an overview and instructions for the project.

## How to Run

1. Clone the repository:

   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```
2. Ensure the required dependencies are installed (see Requirements).
3. Place the `pics/` directory with all assets in the same directory as `main.py` and `button1.py`.
4. Run the game:

   ```bash
   python main.py
   ```
5. Follow the on-screen instructions:
   - Navigate the main menu to choose between playing with Minimax (with/without Alpha-Beta) or Heuristic AI.
   - Select a color (Red or Yellow) for your pieces.
   - For Minimax modes, choose a difficulty level (Easy, Medium, Hard).
   - Click on a column to drop your piece during your turn.

## Gameplay Instructions

- **Main Menu**:
  - **Play Minimax**: Choose between Minimax with or without Alpha-Beta Pruning.
  - **Play Heuristic**: Play against the Heuristic-based AI.
  - **Quit**: Exit the game.
- **Color Selection**: Choose Red or Yellow for your pieces (the AI gets the opposite color).
- **Difficulty Selection** (Minimax modes only):
  - **Easy**: Depth 1 (faster, less strategic).
  - **Medium**: Depth 3 (balanced).
  - **Hard**: Depth 5 (slower, more strategic).
- **Gameplay**:
  - Click on a column to drop your piece.
  - The AI responds automatically during its turn.
  - The game ends when a player wins (four pieces connected) or the board is full (draw).
  - After the game ends, the result is displayed, and the game returns to the main menu after a short delay.

## AI Algorithms

- **Minimax with Alpha-Beta Pruning**:
  - Uses a depth-limited search to evaluate future game states.
  - Alpha-Beta pruning reduces the number of nodes evaluated, improving performance.
  - Scores positions based on winning moves, potential threats, and board control (e.g., center column preference).
- **Minimax without Alpha-Beta Pruning**:
  - Similar to the above but evaluates all possible nodes, making it slower.
  - Useful for educational purposes to compare with Alpha-Beta pruning.
- **Heuristic-based AI**:
  - Evaluates immediate board states without deep search.
  - Prioritizes moves that create winning opportunities, block opponent wins, or control the center.
  - Faster but less strategic than Minimax.

## Limitations

- The game relies on local assets (`pics/` directory), which must be present for the GUI to function correctly.
- The Minimax algorithms (especially without Alpha-Beta) can be slow at higher difficulty levels due to the large number of possible game states.
- No multiplayer mode; the game is strictly human vs. AI.
- The Heuristic AI may make suboptimal moves compared to Minimax, as it lacks deep foresight.

## Future Improvements

- Add a two-player mode for local multiplayer.
- Optimize the Minimax algorithm further (e.g., transposition tables).
- Enhance the GUI with animations for piece drops and win celebrations.
- Add sound effects and background music.
- Implement a save/load game feature.
- Provide an option to undo moves.

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Submit a pull request with a clear description of your changes.

Please ensure your code follows the existing style and includes appropriate comments.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Acknowledgments

- Built using **Pygame** for the GUI and game loop.
- Inspired by classic Connect Four implementations and AI tutorials.
- Thanks to the open-source community for providing resources and documentation.