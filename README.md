﻿# causal_montezuma
# Causal Co-op Learner for Overcooked

This project explores **cooperative learning in the Overcooked environment**, leveraging **causal discovery and structured interventions** to develop an agent that learns effective teamwork strategies. Unlike standard imitation learning, this approach enables the agent to **actively infer causal relationships** between actions, events, and rewards, allowing for **adaptive and robust cooperation** with human or AI teammates.

## Key Features
- **Causal Discovery in Multi-Agent Coordination** – The agent identifies key dependencies in team actions to enhance cooperation.
- **Structured Interventions for Skill Learning** – Uses interventions to understand causal effects, optimizing decision-making.
- **Generalizable Decision-Making** – Learns across different teammate behaviors and kitchen layouts.
- **Beyond Imitation Learning** – Develops a model that can **reason and plan** causally rather than simply mimicking demonstrations.

## Project Goals
This project aims to **bridge causal learning and cooperative AI**, moving towards more **interpretable, efficient, and human-aligned teamwork strategies**. The agent will:
- Discover causal relationships between actions and outcomes.
- Use structured interventions to refine cooperative decision-making.
- Adapt to various teammate playstyles and new environment layouts.
- Benchmark performance against traditional imitation learning baselines.

## Methodology
The agent’s learning process involves:
1. **Causal Graph Discovery** – Extracts causal dependencies from observed actions.
2. **Interventional Learning** – Uses **do-calculus** to model intervention effects.
3. **Curriculum-based Training** – Learns progressively complex cooperation tasks.
4. **Evaluation in Overcooked-AI** – Benchmarks performance in simulated teamwork.

## Installation & Usage
### Prerequisites
- Python 3.8+
- Dependencies (install using `pip`):
  ```
  pip install gym numpy causal-learn
