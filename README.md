# 🛸 Alien Shooter Game (Space Invaders)

A retro-style Space Invaders arcade game written in **C++** utilizing the **Win32 Console Graphics API (GDI)** for direct console-based rendering. 

---

## 🎮 Game Controls

### 🏠 Start Menu
- **`1`** — Start a New Game
- **`2`** — Load a Saved Game
- **`3`** — Quit the Game

### 🚀 Gameplay Controls
- **`↑ / ↓ / ← / →`** — Move the Space Jet
- **`Spacebar`** — Fire Bullets
- **`Esc`** — Pause Menu

### ⏸️ Pause Menu Options
- **`R`** — Resume the Game
- **`S`** — Save Game State (saves current score, lives, and positions)
- **`Q`** — Quit to Menu

### 🏆 Game Over Options
- **`H`** — View Local High Scores
- **`Q`** — Quit to Menu

---

## ✨ Features
- **Win32 GDI Graphics:** Custom UI elements, alien shapes, and particle bullets drawn directly onto the console window.
- **Save & Load System:** Save your progress, score, lives, and alien waves locally to `savedgame.txt` and resume anytime.
- **Local Leaderboard:** Saves the top 5 high scores to `highscores.txt`.
- **Intelligent Alien AI:** Wave of 50 aliens that moves in a challenging zig-zag pattern towards the player.
- **Smooth Game Loop:** Optimized frame rates with sleep calls to prevent high CPU usage.

---

## 🛠️ How to Compile & Run (Windows)

This game is designed specifically for **Windows operating systems** because it relies on `<windows.h>` and console window handles.

### Step 1: File Setup
For cleaner compilation, rename the project files:
1. Rename `L24-0505 L24-0523 (BINARY DUO) .txt` to `main.cpp`.
2. Rename `help (3).txt` to `help.h`.
3. In `main.cpp`, ensure you have `#include "help.h"` (if it's not already linked).

### Step 2: Build & Run
You can compile the files using **Microsoft Visual Studio** or from the command line using `MSVC (cl.exe)` or `MinGW (g++)`:

**Using MinGW (g++):**
```bash
g++ main.cpp -o AlienShooter.exe -lgdi32
AlienShooter.exe
```

---

## 📁 File Structure
- `main.cpp` — Main game loop, state handling, collision detection, and menu logic.
- `help.h` — Win32 utility wrapper containing console drawing methods (`myRect`, `myLine`, `drawText`).
- `highscores.txt` — Automated local database for leaderboard scores.
- `savedgame.txt` — Automated state preservation file.
