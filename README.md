# Hangman Jack Game

A console-based Hangman implementation with multiple difficulty levels, categories, single- and two-player modes, hint support, and a dynamic scoring system.

---

## Table of Contents

- [Features](#features)  
- [Prerequisites](#prerequisites)  
- [Installation](#installation)  
- [Usage](#usage)  
  - [Starting the Game](#starting-the-game)  
  - [Controls & Input](#controls--input)  
- [Scoring](#scoring)  
- [Project Structure](#project-structure)  
- [Contributing](#contributing)  
- [License](#license)  

---

## Features

- **Three Difficulty Levels:**  
  - Easy (E)  
  - Medium (M)  
  - Hard (H)  

- **Three Question Categories:**  
  1. Geography  
  2. General Knowledge  
  3. Technology  

- **Game Modes:**  
  - Single Player  
  - Two Player (each player gets up to 5 words)  

- **Hint System:**  
  - Reveal one letter per word by pressing `?`  
  - Hints reduce the score reward for that word  

- **Scoring System:**  
  - Rewards and penalties vary by difficulty and hint usage  
  - Cumulative scoring across rounds  

- **ASCII-Art Hangman Drawing**  
- **Randomized Feedback Messages** for correct/incorrect guesses  

---

## Prerequisites

- Nand2Tetris JackCompiler and VMEmulator
---

## Installation

```bash
git clone https://github.com/Aniruddhraam/hangman-jack.git
cd hangman-terminal-game
javac src/*.java
```

---

## Usage

### Starting the Game

```bash
JackCompiler hangman-jack
```

### Controls & Input

1. **Mode Selection**  
   - Press `1` for Single Player  
   - Press `2` for Two Player  

2. **Difficulty Selection**  
   - Press `E` for Easy  
   - Press `M` for Medium  
   - Press `H` for Hard  

3. **Category Selection**  
   - Press `1` for Geography  
   - Press `2` for General Knowledge  
   - Press `3` for Technology  

4. **Guessing Letters**  
   - Type any letter `A–Z` (case insensitive) and press Enter  
   - Press `?` to use your one hint for the current word  

5. **Replay Prompt**  
   - After each round, press `Y` to play again or any other key to exit  

---

## Scoring

| Difficulty | No Hint Reward | With Hint Reward |
| ---------- | -------------- | ----------------- |
| Easy       | +1             | +0                |
| Medium     | +3             | +1                |
| Hard       | +5             | +3                |

- In **Two Player** mode, each player’s score is tracked separately over 5 words.

---

## Project Structure

```plaintext
hangman-terminal-game/
├── src/
│   ├── HangmanDisplay.java
│   ├── Questions.java
│   ├── Keyboard.java
│   ├── Screen.java
│   ├── Output.java
│   ├── Random.java
│   └── Time.java
├── README.md
└── LICENSE
```

- **`HangmanDisplay.java`** – Main game logic  
- **`Questions.java`** – Provides word lists and corresponding clues per difficulty/category  
- **`Keyboard`, `Screen`, `Output`, `Random`, `Time`** – Utility classes for I/O and game mechanics  

---

## Contributing

1. Fork the repository  
2. Create your feature branch: `git checkout -b feature/MyFeature`  
3. Commit your changes: `git commit -m "Add MyFeature"`  
4. Push to the branch: `git push origin feature/MyFeature`  
5. Open a Pull Request  

Please follow the existing code style and include meaningful commit messages.

---
