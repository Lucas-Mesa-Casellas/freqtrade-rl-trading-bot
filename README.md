![Python](https://img.shields.io/badge/Python-3.10-blue)
![Status](https://img.shields.io/badge/Status-Under%20Development-yellow)
![License](https://img.shields.io/badge/License-MIT-green)

# Freqtrade RL Trading Bot

## Overview
This project is a **long-term experimental trading system** designed to compare
**rule-based strategies** and **reinforcement learning agents** under realistic
market constraints.

It is not a “profit showcase”, but a **research and engineering framework**
focused on robustness, reproducibility, and deployment readiness.

---

## Objectives
- Build a solid **rule-based baseline** using Freqtrade
- Quantify limitations of indicator-driven strategies
- Develop a **reinforcement learning agent** (Gymnasium + Stable-Baselines3)
- Compare RL vs rule-based under identical data and risk constraints
- Deploy a 24/7 trading system on cloud infrastructure

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
