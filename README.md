## Hex Game AI

This repository contains an implementation of the Hex board game, featuring a Monte Carlo Tree Search (MCTS) based AI for playing against a human opponent.

### Features

1. **Board Representation**:
   - The board is represented as a 2D vector of characters, where 'B' represents black pieces, 'W' represents white pieces, and '+' represents empty cells.
   - The board is dynamically sized, and its appearance is enhanced for better readability.

2. **Player Enumeration**:
   - Players are represented as an enumeration with two possible values: `Player::WHITE` and `Player::BLACK`.

3. **Move Validation**:
   - The game checks if a move is within the board boundaries and if the cell is empty before placing a piece.

4. **Win Condition**:
   - The game uses a breadth-first search (BFS) to check if a player has formed a connected path from one side of the board to the other.

5. **AI Implementation**:
   - The AI uses Monte Carlo simulations to evaluate possible moves and selects the move with the highest win rate.

6. **Game Play**:
   - The game allows the human player to choose their side and board size.
   - The AI makes optimal moves based on the Monte Carlo simulations.

### Usage

1. **Clone the repository**:
    ```bash
    git clone https://github.com/yourusername/hex-game-ai.git
    cd hex-game-ai
    ```

2. **Compile the code**:
    ```bash
    g++ -o hex_game main.cpp
    ```

3. **Run the game**:
    ```bash
    ./hex_game
    ```

### Game Flow

1. **Setup**:
   - The player is prompted to choose the size of the board.
   - The player selects their side (Black or White).

2. **Gameplay**:
   - Players take turns placing their pieces on the board.
   - The AI calculates and makes its move using the MCTS algorithm.
   - The game checks for a win after each move.

3. **Win Condition**:
   - The first player to connect their pieces from one side of the board to the opposite side wins.

### Example

```bash
You wish to challenge a computer in Hex? Very well, Let's play!

How big of a board do you want to play on? (5 - 11 recommended): 7
Good! The board is set!
  0 w 1 w 2 w 3 w 4 w 5 w 6
0 +---+---+---+---+---+---+
  b \ / \ / \ / \ / \ / \ / \
    b 1 +---+---+---+---+---+
      b \ / \ / \ / \ / \ / \
        b 2 +---+---+---+---+
          b \ / \ / \ / \ / \
            b 3 +---+---+---+
              b \ / \ / \ / \
                b 4 +---+---+
                  b \ / \ / \
                    b 5 +---+
                      b \ / \
                        b 6 +
Now we need to pick sides. I'll let you pick. (b/w): b

Your turn!
Where are you putting your piece? (x y =) 0 0

My turn! I move: 6 6
```


### Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

---
