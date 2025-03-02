# Causal Discovery with Structured Interventions

## Overview

This project explores **causal discovery and reasoning** in reinforcement learning (RL) environments, particularly in a **symbolic version of Montezuma’s Revenge**. Unlike traditional RL agents that optimize rewards through action sequences, **causal agents** aim to infer the underlying structure of their environment. 

The project leverages **pre-planned interventions** and **Causal Bayesian Networks (CBNs)** to discover relationships between actions, objects, and outcomes. Structure learning algorithms are applied to infer causal dependencies, laying the groundwork for **future integration with tractable probabilistic models**.

## Key Features

- **Symbolic Gridworld Representation** of Montezuma’s Revenge.
- **Pre-planned Interventions** to generate interventional data.
- **Causal Bayesian Networks (CBNs)** for structure learning.
- **Curriculum-based learning** to introduce progressively complex causal dependencies.
- **Comparison with Atari-reset environment** as a baseline.
- **Exploration of inference challenges** in high-dimensional causal graphs.

## Motivation

Reinforcement learning often relies on direct state-action mappings to maximize rewards, leading to:
- **Limited generalization** across new tasks.
- **Inefficient exploration**, particularly in sparse-reward environments like Montezuma’s Revenge.
- **Lack of structured reasoning**, making it difficult for agents to adapt to novel scenarios.

By incorporating **causal reasoning**, this project aims to enhance RL by enabling:
- Efficient **planning of action sequences** without exhaustive trial-and-error.
- **Generalization across tasks** using learned causal structures.
- **Inference of consequences** for untested actions.

## Methodology

### 1. **Symbolic Gridworld Design**
   - A simplified version of Montezuma’s Revenge was implemented in a symbolic environment.
   - The environment includes **keys, doors, obstacles, and agent actions**, capturing essential causal relationships.

### 2. **Pre-planned Interventions**
   - Interventions allow agents to **actively modify variables** to observe causal effects.
   - Modeled using **Pearl’s do-calculus**:  
     \[
     P(Y | do(X = x)) = P(Y | X = x, Pa(X))
     \]
   - This enables **disentangling correlation from causation** in action outcomes.

### 3. **Causal Graph Learning**
   - **PC Algorithm** was used for structure learning.
   - A **causal Bayesian network (CBN)** was constructed from interventional data.

### 4. **Baseline Comparison (Atari-reset)**
   - OpenAI’s **Atari-reset environment** was used to compare RL-based learning with causal discovery.
   - Challenges in **inference scalability** were noted.

## Results

- **Learned graphs** accurately captured simple causal relationships in small environments.
- **Inference challenges** remain for larger environments.
- **Baseline comparisons** with RL agents highlight the potential of causal discovery for efficient exploration.

## Future Work

- **Integration with Interventional Sum-Product Networks (iSPNs)** for tractable inference.
- **Expansion to partially observable environments**.
- **Full RL-based benchmarking** against standard agents.

## Installation & Setup

### Requirements
- Python 3.8+
- NumPy
- NetworkX
- OpenAI Gym (for Atari-reset comparisons)
- PyTorch (if deep learning models are added)

### Running the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo-name.git
   cd your-repo-name
