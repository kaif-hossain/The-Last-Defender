# 🧟 The Last Defenders Monopoly

> **A Zombie Survival Monopoly Game built with JavaFX, Scene Builder, AI, Networking, and Advanced Object-Oriented Programming.**

**Team Name:** The Last Defenders
**Project Type:** Advanced Object-Oriented Programming (AOOP)
**Language:** Java
**GUI Framework:** JavaFX
**UI Design:** Scene Builder
**JDK:** Java 21

---

## 📖 About The Project

**The Last Defenders Monopoly** is a zombie-survival strategy game inspired by the classic Monopoly board game. It combines traditional property management and strategic decision-making with an apocalyptic zombie survival theme.

Players must move around the board, purchase and restore properties, manage limited resources, defend themselves against zombie attacks, and make strategic decisions to survive.

The game supports **Human and AI players**, allowing players to compete against intelligent computer-controlled opponents. Multiplayer functionality is also implemented using **socket-based networking and multithreading**, allowing multiple players to participate in the same game session.

The project was developed as an **Advanced Object-Oriented Programming (AOOP)** project to demonstrate practical applications of:

* Encapsulation
* Inheritance
* Polymorphism
* Abstraction
* Exception Handling
* Serialization
* Multithreading
* Networking
* AI-based decision making
* Event-driven programming

---

## 🎮 Game Concept

The world has been devastated by a zombie outbreak, and survival is no longer guaranteed.

Players must travel across a dangerous Monopoly-style board while:

* 🏠 Purchasing and restoring properties
* 💰 Managing money and resources
* 🧟 Fighting zombie attacks
* 🎲 Rolling dice and moving around the board
* 🤖 Competing against AI opponents
* 👥 Playing with other human players
* 🛡️ Defending their territory
* ⚔️ Making strategic decisions
* 🏆 Trying to become the last surviving defender

**Survive. Defend. Conquer. Become the Last Defender.**

---

## ✨ Key Features

### 🎲 Interactive Game Board

A visually interactive Monopoly-style board where players can move between different locations, purchase properties, and encounter special zombie-related events.

### 👥 Multiplayer Mode

The game supports multiplayer gameplay through **socket-based networking**. Multiple players can connect to a game session from different windows or computers.

### 🤖 AI Players

AI-controlled opponents can participate in the game and make decisions such as:

* Purchasing properties
* Managing resources
* Responding to events
* Making strategic decisions
* Competing with human players

### 🧟 Zombie Survival System

The traditional Monopoly gameplay is enhanced with zombie survival mechanics. Players may encounter dangerous events and must use their resources strategically to survive.

### 🏚️ Property Restoration

Players can purchase damaged locations and restore them to make them useful for survival. Restored properties can also provide strategic advantages during gameplay.

### 🔊 Sound & Animation

JavaFX media functionality is used to provide:

* Background music
* Dice-roll sounds
* Zombie encounter effects
* Gameplay sound effects
* Interactive animations

### 💾 Save & Load System

Game progress can be saved using **Java serialization**, allowing players to continue their game later.

### ⚠️ Exception Handling

The application uses exception handling to manage invalid inputs, unexpected runtime conditions, and network-related errors.

### 🧵 Multithreading

Multiple threads are used to handle concurrent operations such as:

* Network communication
* Multiplayer interactions
* AI processing
* Game events
* Background tasks

---

## 🛠️ Technologies Used

| Technology       | Purpose                     |
| ---------------- | --------------------------- |
| ☕ Java           | Core programming language   |
| 🎨 JavaFX        | GUI and game interface      |
| 🧩 Scene Builder | UI and FXML design          |
| 🌐 Java Sockets  | Multiplayer networking      |
| 🧵 Java Threads  | Concurrent operations       |
| 🤖 AI Logic      | Computer-controlled players |
| 💾 Serialization | Save and load game data     |
| 🔊 JavaFX Media  | Music and sound effects     |
| 🏗️ OOP          | Application architecture    |

---

## 🏛️ Object-Oriented Programming

The project demonstrates the four major principles of Object-Oriented Programming.

### 🔒 Encapsulation

Game data such as player information, money, health, properties, and game states are encapsulated within appropriate classes.

### 🧬 Inheritance

Common functionality is shared through inheritance between related game entities such as different types of players or game components.

### 🔄 Polymorphism

Different player and game-object behaviors can be implemented through polymorphic methods, allowing the game to treat different objects through common interfaces or parent classes.

### 🧩 Abstraction

Complex game operations are hidden behind classes, interfaces, and methods so that different parts of the system can interact without knowing their internal implementation.

---

## 🌐 Multiplayer Architecture

The multiplayer system uses **client-server architecture**.

```text
             ┌─────────────────────┐
             │       SERVER        │
             │                     │
             │   Game Management   │
             │   Player Management │
             │   Game State        │
             └──────────┬──────────┘
                        │
              Socket Connections
           ┌────────────┼────────────┐
           │            │            │
           ▼            ▼            ▼
      ┌─────────┐  ┌─────────┐  ┌─────────┐
      │ Client 1│  │ Client 2│  │ Client 3│
      │ Player  │  │ Player  │  │ Player  │
      └─────────┘  └─────────┘  └─────────┘
```

The server manages the shared game state, while clients communicate with the server through socket connections.

Multithreading allows the server to handle multiple connected players concurrently.

---

## 🗂️ Project Structure

A simplified structure of the project is:

```text
The-Last-Defender/
│
├── src/
│   └── main/
│       ├── java/
│       │   └── com/
│       │       └── LastDef/
│       │           └── zombiemonopoly/
│       │
│       └── resources/
│           ├── fxml/
│           ├── images/
│           ├── sounds/
│           └── styles/
│
├── README.md
├── pom.xml
└── ...
```

The project is organized into different components for models, controllers, views, networking, utilities, and game logic.

---

## 🎯 Game Flow

```text
        ┌─────────────┐
        │    Start    │
        └──────┬──────┘
               ▼
       ┌───────────────┐
       │ Create / Join │
       │     Game      │
       └───────┬───────┘
               ▼
       ┌───────────────┐
       │ Select Players│
       └───────┬───────┘
               ▼
        ┌─────────────┐
        │  Roll Dice  │
        └──────┬──────┘
               ▼
        ┌─────────────┐
        │ Move Player │
        └──────┬──────┘
               ▼
      ┌──────────────────┐
      │ Tile / Event     │
      │ Interaction      │
      └────────┬─────────┘
               ▼
       ┌───────────────┐
       │ Buy / Restore │
       │ / Defend      │
       └───────┬───────┘
               ▼
        ┌─────────────┐
        │  Next Turn  │
        └──────┬──────┘
               │
               ▼
        ┌─────────────┐
        │ Game Over?  │
        └───┬─────┬───┘
            │ No  │ Yes
            │     ▼
            │  🏆 Winner
            │
            └──► Continue
```

---

## 🚧 Challenges Faced

### 🔊 Sound Integration

Synchronizing background music and event-based sound effects with gameplay events was challenging.

### 🤖 AI Development

Creating AI opponents capable of making meaningful strategic decisions required implementing rule-based decision-making and different game-state conditions.

### 🌐 Networking & Concurrency

Supporting multiple players simultaneously required careful management of:

* Threads
* Socket connections
* Shared game state
* Synchronization
* Client-server communication

### 🎨 GUI Complexity

Maintaining a consistent and responsive interface across different game states was challenging because the UI had to update dynamically based on player actions and game events.

---

## 📚 Resources & References

* **JavaFX** — Used for the graphical user interface, animations, and multimedia.
* **Scene Builder** — Used for designing JavaFX layouts and FXML interfaces.
* **Java SE Development Kit (JDK)** — Used as the core development environment.
* **Gemini 1.5** — Used for collecting and creating visual assets and images.

---

## 🎥 Project Demo

▶️ **YouTube Demo:**
https://youtu.be/8Ic1vljjhoQ?si=BQWDTixj-1KkM5xK

---

## 💻 Project Repository

🔗 **GitHub Repository:**
https://github.com/kaif-hossain/The-Last-Defender

---

## 🚀 Getting Started

### Prerequisites

Before running the project, make sure you have:

* **JDK 21**
* **JavaFX 21**
* **IntelliJ IDEA** or another Java IDE
* **Scene Builder** (optional, for editing FXML files)

### Installation

1. Clone the repository:

```bash
git clone https://github.com/kaif-hossain/The-Last-Defender.git
```

2. Open the project in IntelliJ IDEA.

3. Configure **JDK 21**.

4. Configure the required **JavaFX SDK**.

5. Make sure the JavaFX libraries and VM options are correctly configured.

6. Run the main application.

For multiplayer mode, start the server first and then connect the required client applications.

---

## 👨‍💻 Team

### The Last Defenders

This project was developed as an **Advanced Object-Oriented Programming (AOOP)** project.

The team worked together on:

* Game design
* JavaFX interface
* Game mechanics
* AI development
* Networking
* Multiplayer functionality
* Sound and animation
* Object-oriented architecture
* Testing and debugging

---

## 📸 Screenshots

*Add screenshots of the game interface here.*

Example:

```text
screenshots/
├── main-menu.png
├── game-board.png
├── player-dashboard.png
├── zombie-event.png
└── multiplayer.png
```

You can then display them in the README using:

```markdown
![Main Menu](screenshots/main-menu.png)
![Game Board](screenshots/game-board.png)
```

---

## 🏆 Conclusion

**The Last Defenders Monopoly** successfully combines advanced programming concepts with creative game development.

By integrating **JavaFX, AI, networking, multithreading, serialization, sound, animation, and object-oriented programming**, the project demonstrates how complex software engineering concepts can be applied to create an interactive multiplayer game.

The project not only provides an engaging zombie-survival Monopoly experience but also demonstrates the team's ability to design, develop, and manage a complete software system from concept to implementation.

---

## ⭐ Support

If you find this project interesting, consider giving the repository a ⭐ on GitHub!

**The Last Defenders — Survive the apocalypse. Defend your territory. Be the last one standing. 🧟🎲🏆**
