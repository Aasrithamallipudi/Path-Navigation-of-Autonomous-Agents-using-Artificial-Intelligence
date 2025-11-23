# 🚗🗺️ A* Pathfinding + Motion Simulation (Romania Map)

This project shows how an agent (like a robot or an autonomous car) can find the best route between cities and then simulate movement along that route. It uses the classic **Romania map** from AI textbooks and applies the **A\*** algorithm to plan the path.

After planning the route, the code also simulates some fun motion values like velocity, acceleration, and rotation — just to see how a robot might "behave" as it travels.


## 🌟 What This Project Does

### 👉 1. Finds the best path using A*
The A* algorithm picks the shortest path between two cities using:
- Real road distances  
- A straight-line heuristic toward Bucharest  

For example, starting from **Arad** and ending at **Bucharest**, the output may look like:



### 👉 2. Simulates motion between each pair of cities
For every step in the path, it randomly generates:
- **Velocity** (how fast the robot is moving)
- **Acceleration** (how quickly it's speeding up)
- **Rotation rate** (how sharply it’s turning)

These values aren’t real physics — just a simple way to visualize how movement might change along the way.

---

### 👉 3. Visualizes everything in a chart
The results are plotted using Matplotlib so you can see:
- How velocity changes  
- How acceleration fluctuates  
- How much rotation happens between cities  

It gives a nice overall picture of how the robot behaves along the route.

