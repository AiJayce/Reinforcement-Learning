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

## [2. Atari Breakout — Asynchronous Advantage Actor-Critic (A3C)](https://github.com/AiJayce/Reinforce-Learning/tree/Breakout)
   - State: The game screen, including the ball, paddle, and remaining bricks, represented as image frames.
   - Action: Move the paddle or perform other available game actions.
   - Reward: Gain positive rewards by breaking bricks and maximize the score while avoiding losing the ball.
   - Algorithm: A3C combines an Actor, which learns a policy for selecting actions, and a Critic, which estimates the state value. Multiple agents interact with the environment in parallel and asynchronously update shared model parameters to improve learning efficiency.





----------------
# Applications in Bioinformatics

### Motivation

Biological systems continuously change through gene expression, cellular differentiation, and responses to external stimuli. However, conventional bioinformatics approaches primarily identify statistical associations and structural patterns, limiting their ability to explore potential cellular transition pathways.

Reinforcement Learning (RL) provides an alternative by learning state transitions through reward-driven optimization. By defining cellular states in gene expression or latent spaces, RL can explore transition trajectories and investigate the effects of gene perturbations.

Motivated by this potential, the following projects explore RL as a complementary bioinformatics approach, focusing on cellular state transitions, trajectory exploration, and gene regulatory dynamics.

## [1. scDQ-path](https://github.com/AiJayce/scDQ-path)

**scDQ-path** is a reinforcement learning-based framework for exploring single-cell dynamics and generating perturbation-associated virtual cells.

### Algorithm
- Compresses high-dimensional transcriptomic profiles into a 16-dimensional latent space using a Variational Autoencoder (VAE).
- Employs Double Deep Q-Networks (Double DQN) to learn reward-guided cellular state transitions.
- Explores optimal and alternative latent trajectories beyond conventional pseudotime-based inference.
- Identifies dynamically varying transcription factors along inferred cellular trajectories.
- Performs counterfactual gene knockout simulations through latent-space optimization with a frozen VAE decoder.
- Constructs directed perturbation-response networks from simulated transcriptional changes.
- Integrates multi-trajectory exploration with density-based probabilistic sampling to generate heterogeneous virtual cell populations.
- Supports single-target and multi-target knockout simulations.

### Key Novelty
- Reinforcement learning-driven exploration of continuous latent-space trajectories.
- Identification of alternative and potentially compensatory cellular response paths.
- Integration of counterfactual perturbation modeling and density-guided virtual cell generation.

### Core Technologies
`Python` · `PyTorch` · `VAE` · `Double DQN` · `Reinforcement Learning` · `scRNA-seq`
