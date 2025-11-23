🚗🔍 A* Pathfinding & Motion Simulation on the Romania Map
1️⃣ Objective

The objective of this project is to develop an intelligent route-planning system that identifies the shortest path between cities using the A* search algorithm.
Once the optimal route is found, the project simulates motion parameters such as velocity, acceleration, and rotation to show how a robot or autonomous vehicle might behave while traveling along that path.

The project combines AI pathfinding and basic motion modeling to provide both an optimal route and a visual representation of movement dynamics.

2️⃣ Environment

The project is built in a Python environment and uses:

A predefined Romania map graph (cities and road distances)

Heuristic values (straight-line distances to Bucharest)

Randomized motion values for each path segment

Numpy for numerical operations

Matplotlib for plotting and analysis

Heapq for priority queue management in A*

The environment is static — there are no moving obstacles or real-time updates.
The focus is entirely on:

Optimal route discovery

Motion behavior visualization

3️⃣ Algorithm Used — A* Search

The A* algorithm is used to compute the shortest route between two cities.

Why A*?

Because it uses both:

g(n): the cost already traveled

h(n): the estimated cost to the goal
and finds the most cost-effective path.

Key Steps in the Algorithm

Start from the initial city

Select the best neighbor using f = g + h

Expand the node with the lowest f-value

Continue until Bucharest is reached

Reconstruct the path

After obtaining the route, the project generates:

A velocity value for each segment

An acceleration value

A rotation rate (turning angle)
These mimic physical movement and give each path segment unique motion behavior.

4️⃣ Results
✔️ Path Found

The algorithm successfully finds the shortest path to Bucharest.
Example output:

Arad -> Sibiu -> Rimnicu Vilcea -> Pitesti -> Bucharest
Total Cost: 418

✔️ Motion Parameters Generated

For every transition between cities, the system generates:

Velocity (5–15 m/s)

Acceleration (0.1–2.0 m/s²)

Rotation rate (−30° to +30°)

✔️ Visualization

A Matplotlib plot is created showing the three motion parameters across the path transitions.
This allows easy analysis of:

Speed variations

Acceleration patterns

Turning behavior

It provides a clear picture of simulated robot motion along the optimal route.
