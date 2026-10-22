# Tic-Tac-Toe in C

A console game built to practice C programming, board logic, input handling, and file I/O.

## Features

- Configurable square boards from 3 × 3 to 10 × 10
- Player versus player and player versus computer
- Three-player mode with human or computer participants
- Row, column, and diagonal win detection
- Move logging to `gamelog.txt`

The computer selects a random available cell. A win requires filling an entire row, column, or diagonal.

## Repository structure

```text
src/
  Tic-Tac-Toe.c       # Application source
examples/
  gamelog.txt        # Sample game output
README.md
.gitignore
```

## Build and run

Install a C compiler such as GCC. Run these commands from the repository root.

### Windows PowerShell

```powershell
New-Item -ItemType Directory -Force build
gcc -std=c11 -Wall -Wextra src/Tic-Tac-Toe.c -o build/tic-tac-toe.exe
.\build\tic-tac-toe.exe
```

### Linux / macOS

```sh
mkdir -p build
gcc -std=c11 -Wall -Wextra src/Tic-Tac-Toe.c -o build/tic-tac-toe
./build/tic-tac-toe
```

## Play

Choose **Start Game**, a board size, and a game mode. Enter moves as `row column`, for example `2 3`. During a human turn, enter `M` to return to the menu or `E` to exit.

The program writes `gamelog.txt` in the current working directory and overwrites it when a new game starts. Generated logs and build files are ignored by Git.

## Project status

A learning project. Input validation and computer strategy are areas for future improvement.
