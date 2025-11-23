 Path-Navigation of Autonomous Agents using Artificial Intelligence

 1️. Objective

This project simulates how an autonomous agent navigates through a dynamic environment. The goal is to use the **A*** search algorithm to find an efficient route in a grid world — taking into account static obstacles, high-cost zones, and moving cars.
The focus is on real-time decision-making and adaptive behaviour when the environment changes during execution.

 2️.Environment

The simulation is built on a **20 × 20** grid. Each cell models a road segment with a specific type and cost.

**Grid Components**

* **Normal Road** — cost = 1
* **Static Traffic Zone** — cost = 5
* **Roadblock** — impassable
* **Moving Cars** — dynamic obstacles that shift each step

**Behaviour**

* Moving cars update their positions at each time step.
* The agent follows the pre-computed A* path.
* If a moving car blocks the agent’s next target cell, the simulation halts or re-plans.
* A real-time visual update shows the agent’s progress and environment changes.

 **Libraries Used**

* NumPy — for grid representation and logic
* Matplotlib — for visualization & animation
* Random — to simulate moving obstacle behaviour
* heapq — for A* priority queue implementation
* IPython.display — for animation support in notebook environments



 3️. Algorithm Used — A* Pathfinding

The core path-planning module uses the A* algorithm to compute a least-cost path from start to goal.

**Key Features**

* Uses **Manhattan distance** as the heuristic
* Avoids:

  * Roadblocks
  * Cells currently occupied by moving cars
  * Cells with high traffic cost (to reduce overall travel cost)
* Employs a **priority queue (heapq)** to explore nodes by minimum (f + g) cost
* When the goal is reached, the path is reconstructed from goal → start

**Dynamic Component**

* During execution, moving cars may shift into the agent’s path.
* If the next step is blocked by a dynamic obstacle, the simulation halts or triggers a response.
* Visualization refreshes each step, showing agent movement and environment updates.



4️. Results

 ✔️ Path Planning Success

The system generates:

* A valid starting location
* A valid goal location
* An optimal path computed by A* that respects costs and avoids obstacles

 ✔️ Real-Time Navigation

During the simulation:

* Each step is displayed visually on the grid
* Moving cars continue to update
* Two outcomes are possible:

  * 🎯 The agent reaches the goal successfully
  * ⛔ The agent’s path is blocked by a moving car

 ✔️ Visual Output

The visualization shows:

* The grid with different cell types and colours
* Static traffic zones and roadblocks
* Moving cars
* The planned path drawn in black
* Start and goal markers
* A step-by-step animation (e.g., one frame every ~0.5 seconds)



 5️. How to Run the Project

▶️ Running in Google Colab

1. Open the notebook in Google Colab.
2. Run all cells.
3. The script will:

   * Generate the grid
   * Choose start & goal
   * Compute the A* path
   * Animate the agent’s movement
4. The notebook uses `clear_output()` (or similar) to update frames.

💻 Running Locally

Install dependencies:

```bash
pip install numpy matplotlib
```

Then:

```bash
python <your-script-filename>.py
```

(Use the exact filename you already have in your repo.)

---

6️⃣ Developer’s Role

As the developer, you have:

* Designed a dynamic grid environment
* Encoded cost-based terrain and obstacle behavior
* Implemented the A* pathfinding logic
* Integrated moving obstacles and dynamic updates
* Created real-time visualization using Matplotlib
* Handled collision detection or path blocking
* Structured code into modular, readable functions

 **Skills Demonstrated**

* Heuristic search (A*)
* Path planning in grid worlds
* Handling dynamic obstacles in simulation
* Data visualization and animation in Python
* Real-time reactive system design
