# Omni-Solver: AI Palette Puzzle 🎨

A highly optimized web-based recreation of the "Overflowing Palette" mechanic, enhanced with a custom-built AI engine. This project features a "God Mode" solver, a hybrid audio system, and a responsive mobile-first UI.

## 🎮 Play Online
**[Live Demo Link Here]**
https://omni-solver.onrender.com

## ✨ Features

### 🧠 Omni-Solver AI Engine
Unlike standard puzzle generators that use random noise, this game runs a **Beam Search Algorithm** in the background.
- **Real-time Solving:** Calculates the optimal path to solve any grid configuration from *any* starting point (not just top-left).
- **Dynamic Difficulty:** Ensures generated puzzles require a specific range of moves (6-14 moves).
- **Smart Hints:** The "Lightbulb" button queries the AI to show the exact next best move.

### 🔊 Hybrid Audio System
Built using the **Web Audio API** for zero-latency sound effects.
- **Sampler Mode:** Pre-loads and decodes MP3 assets into memory buffers for instant playback.
- **Dynamic Streaming:** Uses HTML5 Audio for BGM to save memory usage.
- **Smart Resuming:** Handles browser "Audio Context" suspension policies automatically.

### 📱 Core Gameplay
- **Mechanic:** Select a color and click any "island" on the grid to flood it.
- **Tools:** Undo (History Stack), Reset Level, and Add Moves.
- **Settings:** Independent volume controls for BGM and SFX.
- **Responsive:** Fully playable on Desktop and Mobile (touch-optimized).

## 🛠️ Installation & Setup

This is a **Static Web Application** (HTML/CSS/JS). It does not require a backend server, Node.js, or a database.

### Prerequisites
* A code editor (VS Code recommended).
* **VS Code Live Server Extension** (Required for Audio).

### Running Locally
1.  Clone the repository:
    ```bash
    git clone [https://github.com/aniketshaw748-hub/Omni-Solver](https://github.com/aniketshaw748-hub/Omni-Solver)
    ```
2.  Open the folder in VS Code.
3.  **Right-click** `index.html` and select **"Open with Live Server"**.

> **⚠️ Important:** Do not double-click `index.html` to open it directly from your file explorer. Browsers block the Web Audio API (CORS policy) when using the `file://` protocol. You must use a local server (localhost).

## 📂 Project Structure

```text
omni-solver/
├── index.html        # Complete game logic (HTML/CSS/JS)
└── assets/           # Audio files (Required)
    ├── bgm.mp3       # Background music
    ├── click.mp3     # Selection sound
    ├── flood.mp3     # Paint splash effect
    ├── win.mp3       # Level completion
    ├── lose.mp3      # Game over
    └── hint.mp3      # Hint activation
