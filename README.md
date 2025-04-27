# Game of Life

A C++ implementation of Conway's Game of Life, featuring various preset patterns and custom placements.

## Overview

The Game of Life is a cellular automaton devised by mathematician John Conway in 1970. It's a zero-player game where evolution is determined by the initial state. This implementation allows you to place different predefined patterns on a 50×50 grid and observe their evolution across multiple generations.

## Features

- 50×50 grid environment
- Seven predefined patterns:
  - Block (still life)
  - Boat (still life)
  - Tub (still life)
  - Blinker (oscillator)
  - Toad (oscillator)
  - Glider (spaceship)
  - LWSS (Lightweight Spaceship)
  - Gosper Glider Gun
- Custom placement of patterns on the grid
- Configurable number of generations to display

## Game Rules

The Game of Life follows these simple rules:
1. Any live cell with fewer than two live neighbors dies (underpopulation)
2. Any live cell with two or three live neighbors survives to the next generation
3. Any live cell with more than three live neighbors dies (overpopulation)
4. Any dead cell with exactly three live neighbors becomes alive (reproduction)

## How to Use

1. Compile the program using a C++ compiler:
   ```
   g++ game_of_life.cpp -o game_of_life
   ```

2. Run the executable:
   ```
   ./game_of_life
   ```

3. Follow the on-screen prompts to:
   - Select which patterns to add (y/n for each pattern)
   - Enter the grid coordinates (x y) for each pattern you want to place
   - Specify how many generations you want to observe

4. The program will display the evolution of the patterns through each generation.

## Classes

- **NeighbourCell**: Counts live neighbors for a cell
- **Updater**: Updates the grid according to Game of Life rules
- **LifePlacer**: Places predefined patterns on the grid
- **GenerationFinder**: Displays the grid and advances to next generation

## Patterns

### Still Lifes
- **Block**: A 2×2 square of live cells
- **Boat**: A still life pattern resembling a small boat
- **Tub**: A still life pattern with a diamond-like shape

### Oscillators
- **Blinker**: A 3-cell line that alternates between horizontal and vertical
- **Toad**: A 6-cell oscillator that shifts between two patterns

### Spaceships
- **Glider**: A small pattern that moves diagonally across the grid
- **LWSS**: Lightweight Spaceship, a pattern that travels horizontally

### Special Patterns
- **Gosper Glider Gun**: Creates a stream of gliders indefinitely

## Example

```
...Welcome to the Game of Life...
Want to add boat to grid(y/n) ? y
Enter the location to place on grid (x y) : 10 10
Want to add glider gun to grid(y/n) ? n
Want to add glider to grid(y/n) ? y
Enter the location to place on grid (x y) : 20 20
Want to add blinker to grid(y/n) ? n
Want to add toad to grid(y/n) ? n
Want to add tub to grid(y/n) ? n
Want to add light spaceship to grid(y/n) ? n
Enter the number of generations you want to display : 20
```

## Future Improvements

Possible enhancements for this implementation:
- Graphical user interface
- Save/load functionality for grid states
- Adjustable simulation speed
- Larger grid or infinite grid implementation
- Additional preset patterns
