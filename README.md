# Browser NES Tetris (HTML5 Canvas)

A faithful, web-based recreation of the classic 8-bit NES Tetris experience. Built with vanilla HTML5, CSS3, and JavaScript. Focuses on mechanical accuracy, retro aesthetics, and cross-platform playability (desktop and mobile).

## Play the Game
`[Play Here]: (https://sphor.github.io/tetris)`

## Features

* **NES-Accurate Mechanics & Scoring:** 
  * Replicates classic line clear multipliers (40, 100, 300, 1200), multiplied by `(Level + 1)`.
  * Proper 1/2G soft-drop speed with 1 point awarded per successfully dropped grid space.
  * Soft-drop input lockout to prevent accidental drops on the next spawned piece.
  * No modern mechanics (no T-spins, hard drops, or hold queues) to preserve the classic difficulty.
* **Dynamic Sprite Rendering:** Uses a custom 7x7 pixel sprite sheet mapping that dynamically updates block color palettes based on the current level (Levels 0-9+).
* **"Panic Mode" Audio:** Dynamic background music playback rate increases when blocks stack up to row 5, simulating the original game's tension.
* **Level Selection:** Custom pre-game selection screen to start at higher difficulties.
* **Responsive UI & Controls:**
  * Clean, retro CRT-style canvas box shadows and overlays.
  * Dedicated on-screen D-Pad and NES-style action buttons for mobile touch screens.
  * Local Storage integration to save and persist High Scores.
  * Built-in changelog modal, pause functionality, and music toggle.

## Controls

**Desktop:**
* **Move Left / Right:** `A` / `D`
* **Soft Drop:** `S`
* **Rotate Counter-Clockwise:** `Left Mouse Click`
* **Rotate Clockwise:** `Right Mouse Click`
* **Pause / Start:** `Enter` or `P`

**Mobile (Touch):**
* **Movement:** On-screen D-Pad
* **Rotate Counter-Clockwise:** `B` Button
* **Rotate Clockwise:** `A` Button

## Tech Stack
* **HTML5 Canvas:** For rendering the playfield, piece matrices, and UI panels.
* **Vanilla JavaScript (ES6+):** Handling game loops (requestAnimationFrame), matrix rotation, collision detection, and audio manipulation.
* **CSS3:** For responsive layouts, media queries, and classic pixel-font typography.

## File Structure & Assets

To run this project locally, ensure all assets are placed in the root directory alongside `index.html`:

* `index.html` - The core game engine and UI.
* `home.png` - Title screen background asset.
* `NES - Tetris - Miscellaneous - Tetrominoes.png` - The 7x7 block sprite sheet.
* **Audio Files:**
  * `theme.MP3` - Main background music.
  * `move-block.MP3`, `block-land.MP3`, `rotate.MP3` - Block manipulation SFX.
  * `line.MP3`, `tetris.MP3` - Clear SFX.
  * `pause.MP3`, `resume.MP3`, `gameover.MP3` - Game state SFX.

## Running Locally

No build tools or package managers are required. Since the game uses the HTML5 Canvas `drawImage` and local audio API, you will need to serve it over a local web server to avoid CORS restrictions on local file loading.

1. Clone the repository: `git clone https://github.com/sphor/browser-tetris.git`
2. Open the directory in your terminal.
3. Start a local server (e.g., using Python or Node):
   * Python: `python -m http.server 8000`
   * Node/npx: `npx serve`
4. Open `http://localhost:8000` in your browser.

## 📝 Changelog Highlight
* **v1.0.14:** Ignored mouse rotation triggers when interacting with UI buttons.
* **v1.0.13:** Implemented soft-drop input lockout between pieces.
* **v1.0.12:** Added Level Select screen and integrated exact 7x7 custom sprite mapping.
* **v1.0.11:** Added accurate 1-point-per-cell soft-drop scoring.

---
*Disclaimer: This is a fan-made project created for educational and portfolio purposes.*
