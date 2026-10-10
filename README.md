# 🐍 Retro Pixel Snake Game

A sleek, modern arcade-style Snake game built with **React 18**, **Vite**, **Tailwind CSS**, and the **HTML5 Canvas 2D API**. Featuring smooth pixel rendering, glowing neon visuals, responsive keyboard & touch controls, and persistent high scores.

![React](https://img.shields.io/badge/React-18.3-61DAFB?logo=react&logoColor=black)
![Vite](https://img.shields.io/badge/Vite-5.4-646CFF?logo=vite&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-3.4-38B2AC?logo=tailwind-css&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-emerald)

---

## ✨ Features

- **🎮 Crisp Pixel Canvas Engine**: Rendered on a 400×400 canvas with a retro 10px tile grid, dynamic neon glow on the snake head and food, and subtle CRT scanline overlays.
- **⚡ Responsive Input & Buffered Turns**: Dual-buffer direction queue prevents instant 180° self-collisions during rapid key taps.
- **🏆 Persistent High Score**: Best scores are automatically synced to the browser's `localStorage` so your record remains intact across page reloads. Includes a one-click score reset.
- **📱 Hybrid Controls**: Fully playable on desktop and mobile:
  - **Keyboard**: Arrow keys and WASD.
  - **On-Screen D-Pad**: Touch/click directional buttons designed for mobile screens.
- **⏸️ Pause & Restart System**: Pause/resume mid-game via Spacebar or the UI; restart seamlessly upon collision.
- **🧩 Clean & Modular Architecture**: Game state, collision detection, and interval timers are encapsulated inside a custom `useSnakeGame` hook, separating logic from presentation.

---

## 🎮 Controls & Gameplay

| Action | Keyboard Keys | On-Screen Controls |
| :--- | :--- | :--- |
| **Move Up** | <kbd>↑</kbd> or <kbd>W</kbd> | ▲ button |
| **Move Down** | <kbd>↓</kbd> or <kbd>S</kbd> | ▼ button |
| **Move Left** | <kbd>←</kbd> or <kbd>A</kbd> | ◀ button |
| **Move Right** | <kbd>→</kbd> or <kbd>D</kbd> | ▶ button |
| **Pause / Resume** | <kbd>Space</kbd> | Pause / Resume button |
| **Start / Restart** | <kbd>Space</kbd> / <kbd>Enter</kbd> / Any Arrow | Play Again button |

### Rules
1. Guide the snake to eat the glowing pink pixel food.
2. Each food eaten increases your score by **1** and lengthens the snake.
3. Avoid hitting the outer walls or colliding with the snake's own body.

---

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (version 18 or newer recommended)
- `npm` or `yarn` / `pnpm`

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/snake-game.git
   cd snake-game
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Start the local development server**:
   ```bash
   npm run dev
   ```

4. **Open in browser**:
   Navigate to the URL displayed in your terminal (typically `http://localhost:5173`).

### Production Build

To build the project for production deployment:
```bash
npm run build
```

To preview the production build locally:
```bash
npm run preview
```

---

## 📁 Project Structure

```text
snake-game/
├── public/                 # Static assets & favicons
├── src/
│   ├── components/
│   │   ├── Controls.jsx      # Directional D-pad & action bar
│   │   ├── GameBoard.jsx     # HTML5 Canvas renderer & scanline HUD
│   │   ├── GameOverModal.jsx # Ready, Game Over, and Pause overlays
│   │   └── ScoreBoard.jsx    # Current score & persistent high-score badge
│   ├── constants/
│   │   └── gameConfig.js     # Board dimensions, speed, and grid constants
│   ├── hooks/
│   │   └── useSnakeGame.js   # Game loop, state, key listeners, & storage
│   ├── utils/
│   │   └── gameUtils.js      # Collision detection & random food generation
│   ├── App.jsx               # Main application container
│   ├── index.css             # Tailwind CSS entry point
│   └── main.jsx              # Application bootstrap
├── index.html              # HTML shell
├── tailwind.config.js      # Tailwind styling configuration
├── vite.config.js          # Vite bundler configuration
└── package.json            # Project dependencies & scripts
```

---

## ⚙️ Customization

Game parameters can be easily tweaked in [`src/constants/gameConfig.js`](src/constants/gameConfig.js):

- `INITIAL_SPEED` (default `70`ms): Decrease for faster, more challenging gameplay; increase for a relaxed pace.
- `BOARD_WIDTH` & `BOARD_HEIGHT` (default `400`px): Canvas size.
- `PIXEL_SIZE` (default `10`px): Tile dimensions for snake segments and food.
- `INITIAL_SNAKE`: Starting segment count and spawn coordinates.

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
