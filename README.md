# Introduction

<img width="1025" height="415" alt="image" src="https://github.com/user-attachments/assets/af7c6c92-9ff5-4f8e-bda4-83f193dc75dd" />

Reinforcement Learning (RL) is a machine learning paradigm in which an agent learns to make sequential decisions by interacting with an environment and maximizing cumulative rewards. Unlike supervised learning, RL does not require labeled answers for every decision; instead, it improves its policy through reward-driven experience.

### Core Concepts

| Component | Description |
|---|---|
| State | Current condition of the environment |
| Action | Decision made by the agent |
| Reward | Feedback evaluating the outcome of an action |
| Policy | Strategy for selecting actions |
| Value Function | Expected future cumulative reward from a state |
| Q-Function | Expected future cumulative reward of an action in a given state |

Popular RL algorithms include Deep Q-Network (DQN), Asynchronous Advantage Actor-Critic (A3C), and Proximal Policy Optimization (PPO).

### RL in Bioinformatics

RL offers a framework for exploring complex biological systems through sequential decision-making. Potential applications in single-cell transcriptomics and gene regulatory network analysis include:

- **Cellular Trajectory Analysis:** Exploring cellular state transitions while incorporating transcriptional continuity and biological constraints.
- **Gene Regulatory Network Analysis:** Investigating downstream transcriptional effects of gene perturbations.
- **Perturbation Analysis:** Evaluating how sequential interventions may influence gene expression and cellular states.

By integrating biological knowledge into reward functions, RL can complement conventional statistical and machine learning approaches. However, practical applications require carefully designed reward functions, rigorous benchmarking, and independent biological validation.





-------------
# R-L practice

To establish a foundation in reinforcement learning (RL) for its application to bioinformatics, two tutorials were conducted using different RL algorithms: DQN and A3C. Each tutorial explored how an agent learns through states, actions, and rewards.

## [1. CartPole — Deep Q-Network (DQN)](https://github.com/AiJayce/Reinforce-Learning/tree/Cart-pole)
   - State: Cart position and velocity, and pole angle and angular velocity.
   - Action: Move the cart to the left or right.
   - Reward: Receive a positive reward for each time step the pole remains balanced.
   - Algorithm: DQN uses a deep neural network to estimate the Q-value of each action in a given state and selects actions to maximize cumulative future rewards.

## [2. Atari Breakout — Asynchronous Advantage Actor-Critic (A3C)](https://github.com/AiJayce/Reinforce-Learning/tree/Cart-pole)](https://github.com/AiJayce/Reinforce-Learning/tree/Breakout)
   - State: The game screen, including the ball, paddle, and remaining bricks, represented as image frames.
   - Action: Move the paddle or perform other available game actions.
   - Reward: Gain positive rewards by breaking bricks and maximize the score while avoiding losing the ball.
   - Algorithm: A3C combines an Actor, which learns a policy for selecting actions, and a Critic, which estimates the state value. Multiple agents interact with the environment in parallel and asynchronously update shared model parameters to improve learning efficiency.





----------------
# Applications in Bioinformatics

<img width="1024" height="559" alt="image" src="https://github.com/user-attachments/assets/85cb8d58-dfa4-4a34-8b5d-370faddc4ac8" />

### Motivation

Biological systems continuously change through gene expression, cellular differentiation, and responses to external stimuli. However, conventional bioinformatics approaches primarily identify statistical associations and structural patterns, limiting their ability to explore potential cellular transition pathways.

Reinforcement Learning (RL) provides an alternative by learning state transitions through reward-driven optimization. By defining cellular states in gene expression or latent spaces, RL can explore transition trajectories and investigate the effects of gene perturbations.

Motivated by this potential, the following projects explore RL as a complementary bioinformatics approach, focusing on cellular state transitions, trajectory exploration, and gene regulatory dynamics.

## [1. scDQ-path](https://github.com/AiJayce/scDQ-path/tree/scDQpath)

Trajectory-based cellular dynamics analysis, gene regulatory network (GRN) construction, and knockout (KO)-based virtual cell studies using scRNA-seq data primarily rely on artificial temporal axes defined by pseudotime. However, these approaches inherently introduce temporal uncertainty when inferring sequential changes in cellular states and may incorporate atypical cell states that can introduce noise into network dynamics inference. To address these limitations, scDQ-path was developed to provide a more flexible framework for exploring transitions between target cellular states and investigating gene regulatory dynamics.
