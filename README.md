# 🎮 Arcade Game Collection

# 🧠 Introduction

This system is a **timed reactive application** developed using the **Lingua Franca (LF)** coordination language with a **C target**. It demonstrates how interactive software — such as an arcade-style game collection — can be built on top of a **deterministic and concurrent reactive model**. Instead of managing low-level threads or event loops manually, the system relies on **logical time**, **reactors**, and **reactions** to manage interactions and timing with precision.

At its core, the application models **user input** (via keyboard) and **internal behavior** (such as timers and game logic) as **events** that trigger **reactions** across independent computational components known as **reactors**. These reactors communicate **asynchronously** at runtime, but are synchronized **logically** through **timestamps** and **event scheduling**.

---

# 🧩 Reactive Model and System Design

## 🧭 Timed Reactive Behavior

One of the core design elements of this system is its **timed behavior**:

- **Timers** (e.g., a 10-second countdown for a mini-game) are implemented as **logical actions**.
- `lf_schedule(...)` is used to schedule these actions at precise points in **logical time**.
- Once scheduled, a corresponding **reaction** executes **exactly when the timestamp is reached**.
- This models **real-time deadlines** and **durations** allows the **control** of time-interactions.

---

## 🔄 Concurrency, Synchrony & Asynchrony

This system exhibits a rich combination of execution properties:

| Concept            | Description                                                                 |
|--------------------|-----------------------------------------------------------------------------|
| **Synchronous (Logical)**  | All reactions at the same logical time appear to execute simultaneously. |
| **Asynchronous (Physical)** | User inputs (keyboard events) and OS callbacks arrive in real time.        |

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

The game is controlled using single keypress input without needing to press Enter.

---

## 💡 Features

- Raw terminal input handling for real-time interaction.
- Multi-game logic within a single Lingua Franca application.
- Time-constrained reactions using LF's `logical action` timers.
- Modular design with `GameLogic` reactor managing game state.

---

## ⚙️ Installation
### 🔧 Prerequisites

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
└── bin/           # Contains compiled binaries after `make`
```

---

## 🧑‍💻 Authors

**Moayad Maher &** 
**Abdelmseh Nabil &** 
**Ahmed Mahmoud** 


---
