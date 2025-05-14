# 🎮 Arcade Game Collection in Lingua Franca (C Target)

This project is a terminal-based interactive arcade game suite developed using **Lingua Franca** (LF) targeting **C**. It includes three classic games:

- **Whac-A-Mole**
- **Tap War**
- **Rock, Paper, Scissors**

The game is controlled using single keypress input without needing to press Enter.

---

## 🚀 How to Play

Upon running the program, you'll be prompted with a game selection menu:

```
Welcome to the Game Collection!
Select a game (press key):
1. Whac-A-Mole
2. Tap War
3. Rock, Paper, Scissors
```

- **Press 1** for Whac-A-Mole: Hit the correct mole position (1–9) within 3 seconds.
- **Press 2** for Tap War: Player 1 taps '1', Player 2 taps '2' repeatedly for 10 seconds.
- **Press 3** for Rock, Paper, Scissors: Make your choice within 5 seconds using keys 1 (Rock), 2 (Paper), or 3 (Scissors).

To **exit** a game or return to the main menu, press **0**.

---

## 🧠 Features

- Raw terminal input handling for real-time interaction.
- Multi-game logic within a single Lingua Franca application.
- Time-constrained reactions using LF's `logical action` timers.
- Modular design with `GameLogic` reactor managing game state.

---

## ⚙️ Installation

### 🧩 Java Development Kit (JDK)

Lingua Franca requires **Java 17** or higher. Below are some common JDKs you can install:

| JDK         | Description                                                                 |
|-------------|-----------------------------------------------------------------------------|
| OpenJDK     | Open-source and widely used Java distribution.                              |
| Oracle JDK  | Official JDK from Oracle with performance enhancements.                     |
| Amazon Corretto | Free, production-ready OpenJDK distribution from Amazon.             |
| Adoptium    | Previously AdoptOpenJDK, offers cross-platform OpenJDK builds.              |
| GraalVM     | High-performance runtime supporting multiple languages.                     |

---

### 🖥️ Setting Up Java and Lingua Franca on Linux

1. **Install Java 17**

**For Ubuntu/Debian-based systems:**

```bash
sudo apt update
sudo apt install openjdk-17-jdk
```

**For RHEL-based systems:**

```bash
sudo yum install java-17-openjdk-devel
```

**Verify installation:**

```bash
java -version
javac -version
```

2. **Install Lingua Franca CLI Tools**

```bash
curl -Ls https://install.lf-lang.org | bash -s cli
```

This script installs the latest Lingua Franca command-line tools.

---

## 🛠️ Development Environment

### Option A: Visual Studio Code

1. Install [Visual Studio Code](https://code.visualstudio.com/)
2. Install the LF extension:

```bash
code --install-extension lf-lang.vscode-lingua-franca
```

### Option B: Eclipse with Oomph

1. Download and install [Eclipse](https://www.eclipse.org/downloads/)
2. Use the **Oomph installer** to set up Lingua Franca. Select **Java 17 or higher** as the JRE.

---

## 🧪 Running the Game

Once Lingua Franca and the required environment are set up:

```bash
lfc game5.lf
make
./bin/game5
```

Use your keyboard to interact with the terminal games directly!

---


https://github.com/user-attachments/assets/20530f74-036c-46f6-b929-c5f5ce228280



## 📁 File Structure

```bash
.
├── game5.lf       # Main LF file containing all game logic
├── bin/           # Contains compiled binaries after `make`
└── README.md      # This file
```

---

## 🧑‍💻 Authors

**Moayad Maher** 
**Abdelmseh Nabil** 
**Ahmed Mahmoud** 


---

## 📜 License

This project is licensed under the MIT License.
