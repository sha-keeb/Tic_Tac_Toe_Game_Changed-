# Tic-Tac_Toe game

A terminal game exploring C structures, arrays, input handling, game loops, and file I/O.

## Features

- Board sizes from 3 × 3 to 10 × 10.
- Player versus player, player versus computer, and three-player modes.
- Optional CPU players in three-player mode.
- A computer opponent that chooses a random available cell.
- Win detection across a complete row, column, or diagonal.
- A local game log, overwritten when a new game starts.

## Build and run

Install GCC or another C compiler. From the repository directory:

```sh
gcc -std=c11 -Wall -Wextra src/Tic-Tac-Toe.c -o tic-tac-toe
./tic-tac-toe
```

On Windows with GCC / MinGW:

```powershell
gcc -std=c11 -Wall -Wextra src/Tic-Tac-Toe.c -o tic-tac-toe.exe
.\tic-tac-toe.exe
```

Choose a board size and mode, then enter a move as `row column` using 1-based coordinates. During a turn, enter `M` for the menu or `E` to exit.

## Code map

| Component | Responsibility |
| --- | --- |
| `Board`, `Player` | Board state and player information |
| `main`, `main_menu` | Setup and menu flow |
| `run_game` | Turn order and game termination |
| `read_move`, `apply_move` | Input parsing and move validation |
| `computer_move` | Random legal computer moves |
| `check_win`, `board_full` | Win and draw detection |
| `open_log_file`, `log_message`, `close_log_file` | Local log output |

## Data and authentication

This is a local console program. It has no web requests, login system, passwords, sessions, or access tokens. Player names are display labels stored in memory; game events are written to `gamelog.txt`.

## Repository organization

Source code lives in `src/`; example logs live in `examples/`. Source code is tracked; compiled binaries, object files, and runtime logs are ignored.
An older sample log is preserved in `examples/legacy-gamelog.txt`. This repository is the primary project location.

## Known limitations

The computer opponent uses random moves rather than a strategy. End-of-input handling could be improved. This is a learning project.
