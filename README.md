# PredictMyOwnRanked

## Overview
This project predicts the probability of winning the next Valorant match and recommends the **top 3 agents per map** based on:
- **Temporal patterns (LSTM in PyTorch)** → learns win/loss streaks and recent performance trends.
- **Tabular features (XGBoost in scikit-learn)** → evaluates map, agent, kills, deaths, assists, and predicts both win probability and expected KDA.
- **Hybrid combination** → averages both models’ probabilities to provide a more realistic recommendation.

## Workflow
1. **Data Preparation**
   - Load `stats.csv` (your match history).
   - Reverse order (CSV is stored with most recent matches at the top).
   - Encode categorical features (`map`, `agent`).
   - Scale numeric features (`kills`, `deaths`, `assists`).

2. **Models**
   - **LSTM (PyTorch)**: Trained on sequences of 10 matches to capture temporal win/loss patterns.
   - **XGBoost (scikit-learn)**:
     - Classifier → predicts win probability.
     - Regressor → predicts expected KDA.

3. **Prediction**
   - For each Valorant map:
     - Take the last 10 matches played on that map.
     - Compute average kills, deaths, assists.
     - Evaluate all agents you have played on that map.
     - Combine LSTM and XGBoost predictions.
     - Output the **top 3 agents** with highest win probability and expected KDA.

## Requirements
For linux/mac
Install dependencies:
```bash
pip install pandas numpy scikit-learn xgboost torch
```

## Output
Map: Ascent
  - Jett | Win Probability 0.72 | Expected KDA 2.10
  - Reyna | Win Probability 0.65 | Expected KDA 1.95
  - Killjoy | Win Probability 0.60 | Expected KDA 1.80



