# 🧊 Rubric Cube Solver  
A C++ based Rubik’s Cube solver implementation using advanced search algorithms such as **IDA\***, **IDDFS**, **A\*** and heuristic-based pruning.  
This project simulates cube rotations, evaluates cube states, and computes an efficient sequence of moves to reach the solved state.

---

## 🚀 Features

- ✔ Complete Rubik’s Cube representation  
- ✔ Move simulation (U, D, L, R, F, B + prime + double turns)  
- ✔ **IDA\*** (Iterative Deepening A*) solver  
- ✔ **IDDFS** (Iterative Deepening Depth-First Search)  
- ✔ Pattern-based heuristic evaluation  
- ✔ Fast search with pruning  
- ✔ Clean OOP-based C++ architecture  
- ✔ Easily extendable (add new heuristics or solvers)

---

## 📁 Project Structure

Rubrick_Cube_Solver/
│
├── Cube/
│ ├── Cube.h # Rubik’s Cube implementation
│ └── Cube.cpp
│
├── Solver/
│ ├── IDAstarSolver.h # IDA* algorithm implementation
│ ├── IDDFSSolver.h # IDDFS solver
│ └── Heuristics.h # Heuristic functions
│
├── main.cpp # Program entry point
└── README.md

yaml
Copy code

---

## 🔧 How It Works

The solver pipeline:

1. **Scrambled cube input** →  
2. Convert to internal cube representation →  
3. Evaluate heuristic →  
4. Run IDA\* / IDDFS →  
5. Return optimal move sequence

The solver expands states layer-by-layer with:

- Heuristic guided pruning  
- Depth-limited search  
- Cycle avoidance  
- Move reduction (preventing redundant turns)

---

## 🖥️ How to Build & Run

### **Compile (MinGW / g++)**
```bash
g++ main.cpp Cube/*.cpp -o cube_solver
Run
bash
Copy code
./cube_solver
🧠 Algorithms Used
IDA* (Iterative Deepening A*)
Combines DFS + heuristic

Memory efficient

Ideal for huge state spaces (like 43 quintillion cube states)

IDDFS
Depth-limited BFS

Guaranteed optimal when uniform depth costs

Useful for testing smaller scrambles

🧩 Example Output
python
Copy code
Scrambled State:
U R' F2 L B R2 ...

Solving using IDA*...
Solution found!
Moves: U' R F2 L' B' ...
Steps: 17
Time: 0.42 seconds
