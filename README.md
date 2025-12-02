# Biquadris – CS246 Final Project

This repository is a demonstration only.

Due to University of Waterloo course policies, the full source code is not included.

---

## Project Overview

Biquadris is a two-player, turn-based interpretation of the classic arcade game Tetris.  
Unlike traditional real-time gameplay, Biquadris gives each player unlimited time per turn to strategically manipulate and place tetrominoes on their own 11×15 grid.

Each turn, a player may:
- Move the falling block (left, right, down)
- Rotate the block clockwise or counterclockwise
- Soft-drop the block
- Hard-drop the block (ending the turn)
- Clear rows to score points and trigger special actions

The objective is to survive longer than the opponent by preventing your board from overflowing while leveraging strategy and special effects.

---

## UML

<img width="2226" height="1746" alt="image" src="https://github.com/user-attachments/assets/c7728333-2c49-4cc7-8eca-304452089518" />

---

## Images

<img width="2734" height="1548" alt="image" src="https://github.com/user-attachments/assets/fc3b7a64-2c00-41a3-a0ba-d635f63d8276" />

<img width="2734" height="1548" alt="image" src="https://github.com/user-attachments/assets/b405e490-a415-48d3-b779-a163359e876d" />


---


## Gameplay Mechanics

### Board
Each player manages an 11-column by 15-row board.  
Blocks fall one per turn, and a turn ends when a block is dropped.

### Player Actions
Players may:
- Move the block horizontally
- Rotate the block
- Drop the block instantly
- Clear rows strategically

Since the game is turn-based, players can think for as long as needed.

### Special Actions (Triggered on 2+ row clears)
Clearing two or more rows activates a special action affecting the opponent:
- **Blind:** Covers a region of the opponent’s board
- **Heavy:** Applies extra gravity to opponent’s falling blocks
- **Force:** Forces the opponent’s next block to be a specific tetromino

These mechanics add strategic depth beyond simple block placement.

---

## Difficulty Levels

Players can choose between several difficulty tiers (Levels 0–4).  
Each level modifies rules such as:
- Block generation behavior  
- Gravity effects  
- Special conditions on falling blocks  

---

## Technical Implementation

Biquadris is implemented in C++ using:
- Object-oriented design principles  
- Design patterns, including Observer and Strategy  
- Memory-safe ownership via `std::unique_ptr`  
- Modular components separating Board, Player, Block, Level, and Display  
- Both text-based and graphical user interfaces  

The architecture emphasizes reliability, maintainability, and clean separation of responsibilities.
