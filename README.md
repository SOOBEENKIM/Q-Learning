# 🔍 Q-Learning-Based Maze Navigation (Numerical Analysis Project)

This project implements a simple **Q-Learning algorithm** in MATLAB to simulate and analyze an agent navigating through a maze. It aims to explore the effects of different hyperparameters—especially the discount factor `gamma`—on the learning performance and convergence behavior of the agent.

## 📁 Project Files

- `QLearning_Maze_Walk.m`: Core Q-learning algorithm to train the agent in a grid maze.
- `Random_Maze_Walk.m`: Baseline algorithm using random actions for comparison.
- `Read_Maze.m`: Reads and processes the maze input into a numeric grid.
- `Textscanu.m`: Loads the raw maze text file.

## 🤖 What is Q-Learning?

Q-Learning is a **model-free reinforcement learning algorithm** used to learn the optimal action-selection policy for an agent in a finite Markov Decision Process (MDP). It uses the following update rule to iteratively adjust the Q-value:

\[
Q(s,a) \leftarrow Q(s,a) + \alpha \left[ r + \gamma \cdot \max_{a'} Q(s', a') - Q(s,a) \right]
\]

- `α (alpha)`: Learning rate  
- `γ (gamma)`: Discount factor for future rewards  
- `r`: Immediate reward  
- `s, a, s', a'`: Current state, action, next state, and next action

## 🧪 Experimental Design

We tested the effect of varying the discount factor `gamma` while keeping the learning rate `alpha` fixed at 0.8. The agent was trained in a small maze environment, allowing us to clearly observe convergence behaviors.

### 🔧 Parameter Settings and Observations:

| Alpha | Gamma | Observation |
|-------|-------|-------------|
| 0.8   | 0.99  | Agent explores the maze extensively early on, then converges efficiently |
| 0.8   | 0.70  | Moderate exploration and convergence |
| 0.8   | 0.50  | More variable paths, slower convergence |
| 0.8   | 0.30  | Less focus on long-term rewards, convergence becomes more scattered |

### Key Insight:
Higher gamma values lead to more **exploratory behavior** and prioritize **long-term rewards**, while lower gamma values result in **shorter-term planning** and faster but less stable convergence.

## 📷 Screenshots

The simulation includes a visual console output in MATLAB, displaying the agent’s learned path and Q-values after training. Random exploration results are also included for baseline comparison.

## 🏁 Conclusion

This project demonstrates the effectiveness of Q-Learning in a grid-based environment and highlights how tuning the discount factor influences the learning dynamics. It provides a clear educational example of how reinforcement learning behaves under different parameter settings.

## 👨‍💻 Developed by

SooBeen Kim (김수빈)  
For a Numerical Analysis Team Project
