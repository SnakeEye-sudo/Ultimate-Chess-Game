# 🎮 Ultimate Chess Game

<div align="center">

![Java](https://img.shields.io/badge/Java-17+-orange?style=for-the-badge&logo=java)
![JavaFX](https://img.shields.io/badge/JavaFX-20+-blue?style=for-the-badge&logo=java)
![OpenGL](https://img.shields.io/badge/OpenGL-JOGL-green?style=for-the-badge&logo=opengl)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

### 🏆 Ultimate Chess Game with Stunning 3D Graphics, AI Opponent & Multiplayer Mode

*Built with Java + JavaFX/OpenGL | Developed by **Er. Sangam Krishna***

</div>

---

## 📖 Table of Contents
- [✨ Features](#-features)
- [🎯 Game Modes](#-game-modes)
- [🖼️ Screenshots](#️-screenshots)
- [🛠️ Tech Stack](#️-tech-stack)
- [📦 Installation](#-installation)
- [🚀 How to Run](#-how-to-run)
- [🎮 How to Play](#-how-to-play)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)
- [👨‍💻 Author](#-author)

---

## ✨ Features

### 🎨 Graphics & UI
- **Stunning 3D Chess Board** with JOGL (OpenGL wrapper for Java)
- **Multiple Board Themes** - Choose from 10+ beautiful board designs
- **High-Quality Chess Pieces** - Photorealistic 3D models with smooth animations
- **Customizable Piece Skins** - 20+ SVG/PNG piece sets (Classic, Modern, Wooden, Crystal, etc.)
- **Smooth Animations** - Piece movement, capture effects, particle engine
- **Camera Controls** - Zoom, rotate, pan the 3D chessboard
- **Lighting Effects** - Dynamic shadows and ambient lighting
- **Sound Effects** - Move, capture, check, checkmate sounds

### 🧠 Game Logic
- **Complete Chess Rules Implementation**
  - All piece movements (Pawn, Rook, Knight, Bishop, Queen, King)
  - Castling (Kingside & Queenside)
  - En Passant
  - Pawn Promotion (Queen, Rook, Bishop, Knight)
  - Check & Checkmate detection
  - Stalemate & Draw conditions
  - Threefold repetition
  - Fifty-move rule

### 🎮 Game Modes

#### 1️⃣ Single Player (vs AI)
- **Stockfish AI Engine Integration** - World's strongest open-source chess engine
- **Multiple Difficulty Levels** (Beginner to Grandmaster)
- **AI Strength Settings** (ELO 800 - 3500+)
- **Move Suggestions** - Hints and best move recommendations
- **Position Analysis** - Real-time evaluation bar

#### 2️⃣ Multiplayer Mode
- **Local Multiplayer** - Play on the same computer (Hot Seat)
- **Online Multiplayer** - Play with friends over the internet
  - Java Sockets implementation
  - Room creation & joining
  - Real-time move synchronization
  - Chat functionality

### 📊 Additional Features
- **Undo/Redo Moves** - Take back or replay moves
- **Move History Panel** - See all moves in PGN notation
- **Timer/Clock** - Configurable time controls (Blitz, Rapid, Classical)
- **Move Highlights** - Visual indicators for legal moves
- **Last Move Indicator** - Highlight previous move
- **Save/Load Games** - Save progress and resume later (PGN format)
- **Export Games** - Share your games in PGN format
- **Game Statistics** - Track wins, losses, draws
- **Puzzle Mode** - Solve chess puzzles (Coming Soon)

---

## 🎯 Game Modes

### 🤖 Single Player (vs AI)
Play against the powerful Stockfish chess engine with adjustable difficulty.

```
Difficulty Levels:
🟢 Beginner    (ELO 800-1200)
🟡 Intermediate (ELO 1200-1800)
🟠 Advanced     (ELO 1800-2400)
🔴 Expert       (ELO 2400-3000)
⚫ Grandmaster  (ELO 3000-3500+)
```

### 👥 Multiplayer
- **Local**: Play with a friend on the same device
- **Online**: Connect via IP address or create/join rooms

---

## 🖼️ Screenshots

> *Screenshots will be added soon after implementation*

---

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|----------|
| **Java 17+** | Core programming language |
| **JavaFX 20+** | Modern UI framework |
| **JOGL (OpenGL)** | 3D graphics rendering |
| **Stockfish Engine** | Chess AI opponent |
| **Maven/Gradle** | Build & dependency management |
| **Java Sockets** | Online multiplayer networking |
| **PGN Parser** | Game save/load functionality |

---

## 📦 Installation

### Prerequisites
- **Java Development Kit (JDK) 17 or higher**
- **JavaFX SDK 20+**
- **Maven or Gradle** (for dependency management)
- **Stockfish Engine** (for AI mode)

### Step 1: Clone the Repository
```bash
git clone https://github.com/SnakeEye-sudo/Ultimate-Chess-Game.git
cd Ultimate-Chess-Game
```

### Step 2: Install Dependencies

#### Using Maven:
```bash
mvn clean install
```

#### Using Gradle:
```bash
gradle build
```

### Step 3: Download Stockfish Engine
1. Download Stockfish from [official website](https://stockfishchess.org/download/)
2. Extract the executable
3. Place it in the `resources/engines/` directory
4. Update the path in `config.properties`

---

## 🚀 How to Run

### Using Maven:
```bash
mvn javafx:run
```

### Using Gradle:
```bash
gradle run
```

### Using JAR:
```bash
java --module-path /path/to/javafx-sdk/lib --add-modules javafx.controls,javafx.fxml -jar Ultimate-Chess-Game.jar
```

---

## 🎮 How to Play

### Basic Controls
- **Mouse**: Click and drag pieces to move
- **Right Click**: Show legal moves for a piece
- **Spacebar**: Undo last move
- **Ctrl+Z**: Redo move
- **Ctrl+S**: Save game
- **Ctrl+O**: Load game
- **Arrow Keys**: Rotate camera (3D mode)
- **Mouse Wheel**: Zoom in/out

### Starting a Game
1. Launch the application
2. Select game mode:
   - **Single Player**: Choose AI difficulty
   - **Multiplayer (Local)**: Pass and play
   - **Multiplayer (Online)**: Create or join a room
3. Choose your color (White/Black)
4. Set time controls (optional)
5. Start playing!

---

## 🏗️ Project Structure

```
Ultimate-Chess-Game/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   ├── com/sangamkrishna/chess/
│   │   │   │   ├── model/          # Chess pieces, board, game logic
│   │   │   │   ├── view/           # JavaFX UI components
│   │   │   │   ├── controller/     # Game flow controllers
│   │   │   │   ├── engine/         # Stockfish integration
│   │   │   │   ├── network/        # Multiplayer networking
│   │   │   │   ├── graphics/       # 3D rendering (JOGL)
│   │   │   │   └── utils/          # Helper classes
│   │   └── resources/
│   │       ├── images/             # Chess piece images
│   │       ├── models/             # 3D piece models
│   │       ├── sounds/             # Sound effects
│   │       ├── themes/             # Board themes
│   │       └── engines/            # Stockfish executable
│   └── test/                       # Unit tests
├── docs/                           # Documentation
├── screenshots/                    # Game screenshots
├── pom.xml / build.gradle          # Build configuration
├── LICENSE                         # MIT License
└── README.md                       # This file
```

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/AmazingFeature
   ```
3. **Commit your changes**
   ```bash
   git commit -m 'Add some AmazingFeature'
   ```
4. **Push to the branch**
   ```bash
   git push origin feature/AmazingFeature
   ```
5. **Open a Pull Request**

### Ideas for Contribution
- 🎨 Add more board themes
- 🎭 Create new piece designs
- 🧩 Implement puzzle mode
- 📱 Mobile version (Android/iOS)
- 🌐 Web version (GWT)
- 🤖 Improve AI integration
- 🔊 Add more sound effects
- 🌍 Add internationalization (i18n)

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

### Open Source Attributions
This project uses the following open-source resources:
- **Stockfish Chess Engine** - [GPL v3](https://github.com/official-stockfish/Stockfish)
- **JOGL (Java OpenGL)** - [BSD License](https://jogamp.org/)
- **Chess Piece Graphics** - [Wikimedia Commons](https://commons.wikimedia.org/) (Various CC licenses)

---

## 👨‍💻 Author

<div align="center">

### **Er. Sangam Krishna**

*Full Stack Developer | Java Enthusiast | Chess Lover*

[![GitHub](https://img.shields.io/badge/GitHub-SnakeEye--sudo-black?style=for-the-badge&logo=github)](https://github.com/SnakeEye-sudo)
[![Profile](https://img.shields.io/badge/Coder%20|%20AI/ML%20|%20Security-Never%20blinking%2C%20always%20building-green?style=for-the-badge)](#)

**📧 Contact:** Open for collaborations and suggestions!

</div>

---

## 🎉 Acknowledgments

- **Stockfish Team** - For the amazing chess engine
- **JOGL Community** - For OpenGL bindings
- **JavaFX Community** - For the modern UI framework
- **Chess.com & Lichess** - For inspiration
- **Wikimedia Commons** - For open-source chess piece graphics
- **All Contributors** - Thank you for your support!

---

## 🌟 Star This Repository!

If you like this project, please give it a ⭐ on GitHub!

---

<div align="center">

### 🚧 **Work in Progress** 🚧

*This project is actively under development. New features are being added regularly!*

**Current Status:** `Alpha v0.1.0`

**Roadmap:**
- [x] Repository setup
- [ ] Core chess engine implementation
- [ ] 3D graphics integration (JOGL)
- [ ] Stockfish AI integration
- [ ] Multiplayer networking
- [ ] UI/UX polish
- [ ] Testing & bug fixes
- [ ] Beta release

**Expected Beta Release:** Q1 2026

---

*Made with ❤️ and ☕ by [Er. Sangam Krishna](https://github.com/SnakeEye-sudo)*
**© 2025 Sangam Krishna. All Rights Reserved.**

</div>
