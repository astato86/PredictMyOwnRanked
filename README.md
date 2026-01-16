# Project 201

## Overview
This project predicts the probability of winning the next Valorant match and recommends the **top 3 agents per map** based on:
- **Temporal patterns (LSTM in PyTorch)** → learns win/loss streaks and recent performance trends.
- **Tabular features (XGBoost in scikit-learn)** → evaluates map, agent, kills, deaths, assists, and predicts both win probability and expected KDA.
- **Hybrid combination** → averages both models’ probabilities to provide a more realistic recommendation.

## Workflow

## Requirements
- Python 3.9+ (recommended).
- Basic knowledge of using the terminal/command prompt.
- Your dataset file: `stats.csv`.

##  to Export Your Matches into a CSV File
1. Visit [tracker.gg/valorant](https://tracker.gg/valorant) and search for your profile.  
2. Scroll down and load as many matches as you want (recommended: at least 100).  
3. Download the page by right-clicking on any blank space and saving it.  
4. Open the `.htm` file, 
## Usage
    
### Packages
```bash
pip install pandas numpy scikit-learn xgboost torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu
```


##### Linux/Mac
```bash
python -m venv valorant-env 
```
```bash
source valorant-env/bin/activate
```
#### Windows
```bash
python -m venv valorant-env
```
```bash
valorant-env\Scripts\activate
```
### Run:

```bash
python launch.py
```

## Output 
Final predictions for match 201 (Top 3 agents per map):

Map: Ascent
  - Jett | Win Probability 0.72 | Expected KDA 2.10
  - Reyna | Win Probability 0.65 | Expected KDA 1.95
  - Killjoy | Win Probability 0.60 | Expected KDA 1.80


