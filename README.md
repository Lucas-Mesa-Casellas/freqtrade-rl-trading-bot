![Python](https://img.shields.io/badge/Python-3.10-blue)
![Status](https://img.shields.io/badge/Status-Under%20Development-yellow)
![License](https://img.shields.io/badge/License-MIT-green)

📊 Hyperopt Optimization Results (50 epochs)

The strategy was optimized using Freqtrade Hyperopt on 5-minute Binance data over a 20-month period (2024–2025).
The objective function used was SharpeHyperOptLoss.

Best run:

Epoch: 39 / 50

Total profit: –0.32%

Win rate: 25%

Max drawdown: 0.64%

Average trade duration: 2h02

🔧 Optimized Buy Parameters
buy_params = {
    "ema_period": 53,
    "macd_fast": 13,
    "macd_signal": 12,
    "macd_slow": 27,
    "rsi_buy": 20,
}

🔧 Optimized Sell Parameters
sell_params = {
    "rsi_sell": 89,
}

📈 ROI Table
minimal_roi = {
    "0": 0.206,
    "37": 0.068,
    "68": 0.017,
    "177": 0
}

🛑 Stoploss & Trailing Stop
stoploss = -0.052
trailing_stop = True
trailing_stop_positive = 0.211
trailing_stop_positive_offset = 0.244
trailing_only_offset_is_reached = False

🤖 Future Work: Reinforcement Learning Agent

Next step: develop a Reinforcement Learning (RL) agent using Gymnasium and Stable-Baselines3:

Define a custom trading environment (actions: Buy / Sell / Hold)

Reward = Profit – Drawdown – Transaction Costs

Train PPO or DQN agent on historical data

Compare RL performance with this rule-based strategy

Deploy RL model predictions on Oracle Cloud
