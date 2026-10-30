# Introduction

<img width="1025" height="415" alt="image" src="https://github.com/user-attachments/assets/af7c6c92-9ff5-4f8e-bda4-83f193dc75dd" />

## Introduction

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

## 1. **CartPole — Deep Q-Network (DQN)**
   - State: Cart position and velocity, and pole angle and angular velocity.
   - Action: Move the cart to the left or right.
   - Reward: Receive a positive reward for each time step the pole remains balanced.
   - Algorithm: DQN uses a deep neural network to estimate the Q-value of each action in a given state and selects actions to maximize cumulative future rewards.

### Page at : https://github.com/AiJayce/Reinforce-Learning/tree/Cart-pole

## 2. **Atari Breakout — Asynchronous Advantage Actor-Critic (A3C)**
   - State: The game screen, including the ball, paddle, and remaining bricks, represented as image frames.
   - Action: Move the paddle or perform other available game actions.
   - Reward: Gain positive rewards by breaking bricks and maximize the score while avoiding losing the ball.
   - Algorithm: A3C combines an Actor, which learns a policy for selecting actions, and a Critic, which estimates the state value. Multiple agents interact with the environment in parallel and asynchronously update shared model parameters to improve learning efficiency.

### Page at : https://github.com/AiJayce/Reinforce-Learning/tree/Breakout







----------------
# Applications in Bioinformatics

<img width="1024" height="559" alt="image" src="https://github.com/user-attachments/assets/eaa7e2bb-3cab-4fc2-ba2d-104ed096e7b7" />

## Motivation

Biological systems are dynamic, involving continuous changes in gene expression, cellular differentiation, and responses to external stimuli. However, conventional bioinformatics approaches often focus on identifying statistical associations and structural patterns in observed data, making it challenging to investigate potential transition pathways without explicit transition labels.

Reinforcement Learning (RL) offers an alternative framework by learning state transitions through reward-driven optimization. By defining cellular states in gene expression or latent spaces and designing reward functions around biological objectives, RL can explore potential transition trajectories, compare alternative pathways, and investigate the long-term effects of gene perturbations.

This motivated me to explore RL as a complementary approach to bioinformatics, focusing on cellular state transitions, trajectory exploration, and gene regulatory dynamics.
Furthermore, modeling cellular state transitions based on gene expression can reveal associations between changes in gene expression and transition trajectories. Integrating perturbation data, such as gene knockouts or drug treatments, may extend this approach to investigating how specific interventions influence cellular state transitions.

Building on these possibilities, the following projects were conducted to establish a foundational understanding of RL and investigate its potential application to bioinformatics, particularly in exploring dynamic changes in cellular states and potential transition trajectories.
