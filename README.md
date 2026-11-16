# Zappy — Network multiplayer game with autonomous AI

[![School: Epitech](https://img.shields.io/badge/School-Epitech-005696.svg)](https://www.epitech.eu/)
[![Academic Year: 2025-2026](https://img.shields.io/badge/Academic%20Year-2025--2026%20(Tek2)-blueviolet.svg)](#)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)


A network multiplayer game where teams of **autonomous AI** explore a planet (Trantor),
gather resources and level up through incantation. The first team to bring 6 players to
level 8 wins. Built as a team project at Epitech (YEP-400 module).

The project is made of **three independent binaries** communicating over a TCP protocol:

| Component      | Language                | Role                                         |
| -------------- | ----------------------- | -------------------------------------------- |
| `zappy_server` | C++20                   | Game core: world, resources, rules, sockets  |
| `zappy_gui`    | C++20 (SFML 2D / raylib 3D) | Real-time visualization of the game      |
| `zappy_ai`     | Python 3                | Autonomous client playing a team             |

## ✨ Features

- 📡 Server handling many simultaneous clients (sockets, multiplexing)
- 🤖 Fully autonomous AI clients: exploration, resource gathering, team coordination
- 🎮 Real-time 2D (SFML) and 3D (raylib) graphical viewer
- 🔤 Custom TCP protocol designed from scratch (AI + GUI channels)
- ✅ Black-box integration tests (pytest) + server coverage (gcov)

## 🚀 Build & run

```bash
cmake -B build && cmake --build build -j

./launch-self.sh          # local server + AI + 2D GUI, all-in-one

# or manually:
./zappy_server -p 4242 -x 15 -y 15 -n TeamA TeamB -c 3 -f 100
./zappy_gui -p 4242 -h 127.0.0.1 -g ./libzappy_graphic_2d.so
./zappy_ai -p 4242 -n TeamA -h 127.0.0.1
```

## 🛠️ Tech stack

C++20 · Python 3 · CMake · SFML · raylib · TCP sockets · pytest

## 🧠 What I learned

Designing a network protocol from A to Z, managing concurrency server-side, and the
slightly magical feeling of watching AIs "live" on screen.

---

*Project built as part of the Epitech curriculum (YEP-400 module).*
