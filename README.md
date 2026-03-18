# Greenhouse Control Study

A Jupyter notebook for simulating and comparing greenhouse control strategies including PID, fuzzy logic, PPO reinforcement learning, shield-only control, LLM-only control, and the GreenGuard hybrid controller.

## Overview

This project evaluates multiple greenhouse temperature-control approaches in a shared simulation environment. The notebook combines weather-driven greenhouse dynamics, controller design, experiment execution across multiple random seeds, statistical analysis, and publication-style visualization.

The goal is to compare how different control methods perform in terms of:

- tracking accuracy
- operational cost
- safety violations
- decision latency

## Controllers Compared

The notebook compares the following methods:

- **PID** — classical proportional-integral-derivative control
- **Fuzzy** — rule-based fuzzy logic controller
- **PPO** — reinforcement-learning controller using Proximal Policy Optimization
- **Shield-Only** — safety-focused rule controller
- **LLM-Only** — language-model-based decision controller
- **GreenGuard** — hybrid intelligent controller

## Notebook Structure

The notebook is organized into the following sections:

1. **Dependencies**  
   Installs and imports the required Python libraries.

2. **Language Model Setup**  
   Loads the `Qwen/Qwen2.5-1.5B-Instruct` model when available.

3. **Environment and Data Structures**  
   Defines crop profiles, telemetry, actions, greenhouse dynamics, and weather integration.

4. **Reinforcement-Learning Wrapper**  
   Wraps the greenhouse simulator in a Gymnasium-compatible environment.

5. **Controllers**  
   Implements PID, fuzzy logic, PPO, shield-only, LLM-only, and GreenGuard agents.

6. **Experiment Loop**  
   Runs repeated simulations across multiple seeds and records performance metrics.

7. **Summary Analysis**  
   Produces summary statistics, boxplots, and t-tests against GreenGuard.

8. **Visualization Data**  
   Builds data snapshots for controller behavior analysis.

9. **Dashboard Figure**  
   Creates a publication-style dashboard with comparative plots.

## Metrics Used

The notebook evaluates each controller using:

- **RMSE** — root mean squared error for control accuracy
- **Cost** — estimated operational cost of heating and ventilation
- **Violations** — count of unsafe or undesired operating conditions
- **Latency** — controller decision time

## Features

- Weather-informed greenhouse simulation
- Multiple control paradigms in one framework
- Reinforcement-learning integration with Gymnasium and Stable-Baselines3
- Language-model-based control experiment
- Multi-seed evaluation for more reliable comparison
- Statistical testing against the GreenGuard baseline
- Publication-style result figures and dashboard plots

## Requirements

Recommended Python version:

- Python 3.10+

Main libraries used:

- transformers
- accelerate
- torch
- pandas
- numpy
- scipy
- seaborn
- matplotlib
- requests
- gymnasium
- stable-baselines3
- shimmy
- scikit-learn

## Installation

Clone the repository:

```bash
git clone https://github.com/your-username/greenhouse-control-study.git
cd greenhouse-control-study
