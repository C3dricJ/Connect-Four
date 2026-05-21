# Connect4 Crestron Based Project

A fully functional Connect Four game built for a **Crestron 3-Series control processor**, programmed in SIMPL Windows and SIMPL+.
<img width="795" height="646" alt="image" src="https://github.com/user-attachments/assets/a5fce3db-af9b-4a64-bf80-c3a77d1f951e" />

---

## Primary Project Files

| File | Description |
|---|---|
| `Connect4.smw` | Main SIMPL Windows program |
| `Connect4.vtp` | VTPro-e UI project (touch panel interface) |
| `ConnectionOfTheFour.usp` | SIMPL+ module containing the core game logic |
| `Connect4.lpz` | Compile SIMPL Windows program |
| `Connect4TSW760.vtz` | Compiled VTPro-E UI for a TSW-760 panel |

---

## Requirements

- Crestron 3-Series control processor (e.g., CP3, AV3, PRO3)
- [SIMPL Windows]([https://www.crestron.com](https://www.crestron.com/Products/Catalog/Control-and-Management/Software/Programming-Commissioning/SW-SIMPL)) (for editing/compiling `Connect4.smw`)
- [VTPro-e]([https://www.crestron.com](https://www.crestron.com/Products/Catalog/Control-and-Management/Software/Programming-Commissioning/SW-VTPRO-E)) (for editing/compiling `Connect4.vtp`)
- SIMPL+ compiler (included with SIMPL Windows)
- Crestron Toolbox (for loading programs to the processor and touch panel)
- Compatible Crestron touch panel
- XPanel software

---

## Getting Started

### 1. Compile the SIMPL+ Module
1. Open `ConnectionOfTheFour.usp` in the SIMPL+ editor.
2. Compile for Series 3 target.
3. Ensure no errors before proceeding.

### 2. Load the SIMPL Program
1. Open `Connect4.smw` in SIMPL Windows.
2. Verify the processor type matches your hardware.
3. Compile the program (`F12`).
4. Use Crestron Toolbox to load the compiled program to your 3-Series processor.

### 3. Load the UI
1. Open `Connect4.vtp` in VTPro-e.
2. Compile the project.
3. Transfer the compiled UI to your touch panel via Crestron Toolbox or directly through the panel's IP address.

---

## How to Play

1. The game is displayed on the connected Crestron touch panel.
2. Player 1 and Player 2 take turns.
3. On your turn, tap a column button on the touch panel to drop your piece into that column.
4. Pieces fall to the lowest available row in the selected column.
5. You win by being the first player to connect four pieces in a row horizontally, vertically, or diagonally!
6. If all columns are filled with no winner, the game ends in a draw.
7. A Reset button is available on the UI to start a new game at any time.

<img width="799" height="647" alt="image" src="https://github.com/user-attachments/assets/82edc808-399d-4f74-843d-662c71fdc38a" />

---

## Notes

- The bulk of the game logic (win detection, board state, turn management) lives in `ConnectionOfTheFour.usp`.
- The `.smw` file handles signal routing between the SIMPL+ module and the touch panel joins.
- Ensure the IP ID of the touch panel in the SIMPL program matches the panel's configured IP ID.

---
