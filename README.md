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

<img width="1024" height="434" alt="image" src="https://github.com/user-attachments/assets/300c99e0-7007-4a5a-ad6e-45555d939e1e" />

Although applications of reinforcement learning (RL) in bioinformatics remain relatively limited, RL has significant potential to learn optimal strategies for achieving predefined objectives in environments where explicit ground-truth labels are unavailable. Supervised learning focuses on predicting predefined labels, while unsupervised learning aims to identify the underlying distributions and structural patterns of data. In contrast, RL enables an agent to learn from rewards associated with state transitions through interactions with an environment and optimize its policy to maximize long-term cumulative rewards.

Biological systems are dynamic, continuously changing in response to gene expression, cellular differentiation, external stimuli, and microenvironmental conditions. These characteristics align with the RL framework, which is based on state transitions and long-term reward optimization. By leveraging this framework, it may be possible to move beyond analyzing static similarities between cellular states and explore the directionality of state transitions and potential cellular trajectories.

First, a reward function designed around biological objectives can provide a framework for learning dynamic cellular transitions without explicit transition labels. For example, gene expression profiles or positions in a latent space can be defined as states, with rewards assigned to transitions that approach a specific biological objective. This enables the exploration of potential transition trajectories toward a target state.

Second, the value function can account for expected long-term cumulative rewards from the current state and subsequent transitions. This enables the comparison of potential transition pathways and the analysis of biological processes with multiple possible trajectories, such as cellular differentiation and disease progression. Furthermore, incorporating continuity in the state space and similarity between transitions may help model gradual changes in cellular states.

Third, the exploration–exploitation mechanism of RL enables the exploration of diverse candidate pathways that align with a reward function, rather than being restricted to patterns observed in existing data. This approach may facilitate the generation of hypotheses regarding novel transition pathways in biological processes where the sequence of transitions is not clearly established, including cellular differentiation, immune cell activation, and disease progression.

Furthermore, modeling cellular state transitions based on gene expression can reveal associations between changes in gene expression and transition trajectories. Integrating perturbation data, such as gene knockouts or drug treatments, may extend this approach to investigating how specific interventions influence cellular state transitions.

Building on these possibilities, the following projects were conducted to establish a foundational understanding of RL and investigate its potential application to bioinformatics, particularly in exploring dynamic changes in cellular states and potential transition trajectories.
