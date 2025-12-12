# Gymnasium Blackjack RL (Q-Learning / SARSA / Monte Carlo) + Web Demo

A reinforcement learning project for **Gymnasium `Blackjack-v1`** implementing **Q-Learning**, **SARSA**, and **Monte Carlo** control, trained offline and deployed in a **Flask + HTML/CSS/JS** web interface that auto-plays episodes and visualizes hands, actions, and outcomes.

## Demo (What You’ll See)
- Choose an algorithm: **Q-Learning**, **SARSA**, or **Monte Carlo**
- Auto-play full episodes using the learned greedy policy `argmax_a Q(s,a)`
- Live stats per algorithm:
  - Episodes, Wins/Losses/Draws, Win Rate
- Blackjack table visualization:
  - Dealer upcard + hidden hole card (revealed at the end)
  - Player hand with “soft hand” indicator (usable ace)
  - Action chips (HIT/ STAND) and final outcome banner

---

## Project Structure (Typical)
```text
gymnasium/
  app.py                   # Flask server (loads Q-tables, serves UI, runs episodes)
  train_agents.py          # Offline training script (produces trained_*.json)
  trained_qlearning.json   # Saved Q-table (dict-like)
  trained_sarsa.json       # Saved Q-table (dict-like)
  trained_montecarlo.json  # Saved Q-table (dict-like)
  templates/
    index.html             # Front-end UI (HTML/CSS/JS)
