#  Dynamic Pathfinding Agent

A grid-based pathfinding visualizer implementing **A\*** and **Greedy Best-First Search (GBFS)** with real-time dynamic obstacle re-planning. Built with Python and Pygame.

---

##  Preview

> Run the app and use **Gen Maze** to generate a random grid, then hit **Run Search** to watch the agent find its path in real time.

---

##  Features

- ✅ **A\* Search** — optimal pathfinding using `f(n) = g(n) + h(n)`
- ✅ **Greedy Best-First Search (GBFS)** — fast search using `f(n) = h(n)`
- ✅ **Manhattan & Euclidean** heuristics (toggle in GUI)
- ✅ **Dynamic Mode** — obstacles spawn during agent movement, agent re-plans automatically
- ✅ **Interactive Map Editor** — draw/erase walls by clicking or dragging
- ✅ **Configurable Grid Size** — enter any size e.g. `15x20`
- ✅ **Real-time Metrics** — Nodes Visited, Path Cost, Time (ms), Re-plans
- ✅ **Color-coded visualization** — path, visited nodes, agent, walls all highlighted

---

##  Installation & Run

### 1. Clone the repository
```bash
git clone https://github.com/Arfa-209/Dynamic-Pathfinding-Agent.git
cd Dynamic-Pathfinding-Agent
```

### 2. Install dependencies
```bash
pip install pygame
```

### 3. Run the application
```bash
python pathfinding_agent.py
```

---

##  How to Use

| Action | How |
|--------|-----|
| Draw walls | Click or drag on the grid |
| Move Start/Goal | Select **Start** or **Goal** mode, then click a cell |
| Generate random maze | Click **Gen Maze** |
| Run pathfinding | Click **Run Search** or press `R` |
| Toggle dynamic obstacles | Click **Dynamic Mode** or press `D` |
| Clear path only | Click **Clear Path** or press `C` |
| Clear entire grid | Click **Clear Grid** |
| Resize grid | Type `rows x cols` in the input box e.g. `20x30` and click **Apply** |

---

##  Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `R` | Run Search |
| `G` | Generate Maze |
| `D` | Toggle Dynamic Mode |
| `C` | Clear Path |

---

##  Color Legend

| Color | Meaning |
|-------|---------|
| 🟢 Green | Final Path |
| 🔵 Blue | Visited Nodes |
| 🟤 Dark Grey | Wall |
| 🟦 Teal | Start Node |
| 🟠 Orange | Goal Node |
| 🟣 Purple | Agent (moving) |

---

##  Algorithms

### A* Search
Uses both actual cost and heuristic: **f(n) = g(n) + h(n)**  
Guarantees the **shortest path** when heuristic is admissible.

### Greedy Best-First Search (GBFS)
Uses only heuristic: **f(n) = h(n)**  
Faster but **does not guarantee** optimal path.

### Heuristics
- **Manhattan Distance** — `|r1-r2| + |c1-c2|` (best for grid movement)
- **Euclidean Distance** — `√((r1-r2)² + (c1-c2)²)` (straight-line)

---

##  Project Structure

```
Dynamic-Pathfinding-Agent/
│
├── pathfinding_agent.py   # Main application (all code in one file)
└── README.md              # This file
```

---

##  Requirements

- Python 3.8+
- pygame 2.x

---

## Author

**Arfa   24F-0721** — NUCES Chiniot-Faisalabad Campus  
AI Assignment 2
