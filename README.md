![Python](https://img.shields.io/badge/Python-3.10-blue)
![Status](https://img.shields.io/badge/Status-Under%20Development-yellow)
![License](https://img.shields.io/badge/License-MIT-green)

# Freqtrade RL Trading Bot

## 🚀 RL Trading System (Research + Engineering Project)

A reinforcement learning framework to design and evaluate trading strategies under real market constraints.

This project focuses on comparing rule-based strategies with RL agents (PPO/DQN) using realistic data, risk management, and backtesting pipelines.

👉 Goal: bridge the gap between theoretical RL and real-world decision systems.

---

## ⚡ Key Highlights

- Built a full trading pipeline using Freqtrade (data, backtesting, evaluation)
- Designed a rule-based baseline strategy (EMA + RSI + ATR + risk management)
- Implemented hyperparameter optimization (Hyperopt)
- Developed a reinforcement learning extension (Gymnasium + Stable-Baselines3)
- Compared RL vs rule-based strategies under identical constraints
- Focus on robustness, reproducibility, and real-world applicability

---

## Overview
This project is a research and engineering framework to evaluate trading strategies using both rule-based methods and reinforcement learning.

It emphasizes realistic constraints such as transaction costs, risk management, and market noise.

The goal is not short-term profit, but understanding how adaptive AI systems perform in real-world environments.

---

## Objectives
- Build a solid **rule-based baseline** using Freqtrade
- Quantify limitations of indicator-driven strategies
- Develop a **reinforcement learning agent** (Gymnasium + Stable-Baselines3)
- Compare RL vs rule-based under identical data and risk constraints
- Deploy a 24/7 trading system on cloud infrastructure

---

## 🎯 Why This Project Matters

Most reinforcement learning projects are tested in simplified environments.

This project brings RL closer to real-world applications by:
- Using real market data
- Incorporating risk and execution constraints
- Comparing against strong rule-based baselines

It reflects how AI systems must operate in uncertain, noisy environments.

---

## Baseline Strategy (Rule-Based)
The current baseline strategy combines:
- EMA trend regime filtering
- RSI mean-reversion entries
- ATR-based volatility filtering
- ROI table + trailing stop risk management

This baseline serves as:
- A **benchmark** for RL agents
- A **fallback production policy**
- A feature generator for RL environments

---

## Experimental Results (Baseline Reference)
Hyperopt was run on:
- Exchange: Binance
- Timeframe: 5m
- Period: ~20 months (2024–2025)
- Objective: Sharpe ratio

Results show limited profitability but **low drawdown**, highlighting the
limitations of static rule-based strategies in noisy markets.

This motivates the transition to adaptive RL agents.

---

## Reinforcement Learning Roadmap
Planned RL stack:
- Custom Gymnasium trading environment
- Observation space: technical indicators + position state
- Action space: Buy / Sell / Hold
- Reward:
  Profit − Drawdown − Fees − Overtrading penalty
- Algorithms:
  PPO (primary)
  DQN (benchmark)

---

## 📊 Future Improvements

- Extend RL training with multi-agent setups
- Integrate more advanced market features
- Explore offline RL / imitation learning
- Deploy live evaluation environment

---

## Tech Stack
- Python 3.10
- Freqtrade
- TA-Lib
- Gymnasium
- Stable-Baselines3
- Binance historical data

---

## Disclaimer
This project is for research and educational purposes.
No financial advice is provided.
