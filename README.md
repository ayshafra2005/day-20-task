# day-20-task
# Day 19 — California House Price Prediction

A machine learning project that compares three regression models on the California Housing dataset to predict house prices.

---

## Overview

This notebook loads the California Housing dataset, trains three different regression models, evaluates their performance, and visualizes feature importances from the best-performing model.

---

## Dataset

**California Housing Dataset** — sourced via `sklearn.datasets.fetch_california_housing()`

- 8 input features (demographic and geographic)
- Target: median house price (in $100,000s)
- Train/Test split: 80% / 20% (`random_state=42`)

---

## Models Compared

| Model | Description |
|---|---|
| Linear Regression | Baseline linear model |
| Decision Tree Regressor | Non-linear tree-based model |
| Random Forest Regressor | Ensemble of 100 decision trees |

---

## Results

| Model | RMSE | R² Score |
|---|---|---|
| Linear Regression | 0.7456 | 0.5758 |
| Decision Tree | 0.7037 | 0.6221 |
| **Random Forest** | **0.5053** | **0.8051** |

**Winner: Random Forest Regressor** — best RMSE and explains ~80.5% of variance in house prices.

---

## Feature Importance (Random Forest)

Top drivers of house prices identified by the Random Forest model:

1. **MedInc** (Median Income) — by far the most influential feature
2. **AveOccup** (Average Occupancy) — household density matters
3. **Latitude / Longitude** — geographic location reflects regional market differences

A bar chart of all feature importances is generated at the end of the notebook.

---

## Requirements

```
pandas
numpy
matplotlib
scikit-learn
```

Install with:

```bash
pip install pandas numpy matplotlib scikit-learn
```

---

## How to Run

```bash
jupyter notebook day_19.ipynb
```

Run all cells top to bottom. No external data files needed — the dataset is fetched automatically from scikit-learn.

---

## File Structure

```
day_19.ipynb    # Main notebook
README.md       # This file
```

---

## Key Takeaways

- Random Forest significantly outperforms both Linear Regression and Decision Tree on this dataset.
- Median income is the strongest predictor of California house prices.
- Geographic features (latitude/longitude) also carry meaningful predictive signal.
- Further gains could come from hyperparameter tuning or advanced ensemble methods.

# create new repository
