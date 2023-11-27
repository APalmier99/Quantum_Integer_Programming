# Quantum Integer Programming
This repository encompasses materials developed during my internship and Master's thesis, focusing on Quantum approaches to combinatorial optimization, with a specific emphasis on Vehicle Routing Problems (VRPs).

# Overview
In this repository, you'll find theoretical materials and code related to my exploration of Quantum algorithms for Integer Programming. Upon graduation, I plan to upload presentation slides and my master's thesis, which can serve as a comprehensive guide to prominent quantum optimization algorithms.

# Thesis Focus
My thesis delves into the Capacitated Vehicle Routing Problem (CVRP), a variant of the Traveling Salesman Problem (TSP) and a fundamental challenge in the broader family of Vehicle Routing Problems. The focus on CVRP arises from its generally smaller size, as more complex variants involve numerous constraints, resulting in impractical variable counts for current Noisy Intermediate-Scale Quantum (NISQ) devices. To address the CVRP, I adopt the Two-Phase Heuristic approach: Cluster First, Route Second.

# Two-Phase Heuristic
According to this heuristic, customers are first clustered to allocate them among available vehicles. Then, for each vehicle, a TSP is modeled on its assigned cluster. To handle subtour elimination in the TSP phase, I employ the recursive Dantzig-Fulkerson-Johnson strategy. For the clustering phase, I explore three approaches: Multi-Knapsack Problem, Modularity Maximization CO problem, and a customized Louvain greedy modularity maximization algorithm.

# Optimization Algorithms
The research evaluates four optimization algorithms: Adiabatic Quantum Computation, Quantum Graver Augmented Multi-seed Algorithm, Variational Quantum Eigensolver, and Quantum Approximate Optimization Algorithm. Each algorithm is thoroughly discussed, including various warm-start strategies.

# Innovative Louvain Approach
My customized Louvain approach enhances the conventional Two-Phase Heuristic, typically reliant on MKP clustering. The Louvain approach not only improves final solutions but is also anticipated to scale better to larger problem instances, as solving Louvain on a large graph is significantly faster than achieving optimality with MKP.

# Code Files

- **QuIP_CVRP.ipynb:** 
  - Final version of the code developed during my research.

- **OLD_Quip_CVRP:**
  - Contains an older version of the code.
  - Experimented with a warm start strategy initializing QAOA parameters from Louvain clusters.
  - Unfortunately, this approach did not yield improvements.
  - Discarded in favor of further optimizations presented in the final notebook.
  
For a comprehensive understanding, I recommend reading the thesis abstract.
