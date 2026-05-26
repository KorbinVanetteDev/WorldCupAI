# WorldCupAI — Neural Networks for Beginners: World Cup Predictions

A complete beginner-friendly tutorial that teaches neural network fundamentals
step by step, culminating in a **FIFA World Cup match outcome predictor**.

## What's Inside

| File | Description |
|------|-------------|
| `neural_network_world_cup_tutorial.ipynb` | The full interactive tutorial notebook |
| `requirements.txt` | Python library dependencies |

## Quick Start

### 1. Install dependencies
```bash
pip install -r requirements.txt
```

### 2. Launch the notebook
```bash
jupyter notebook neural_network_world_cup_tutorial.ipynb
```

### 3. Run cells in order
Press **Shift + Enter** to execute each cell from top to bottom.

---

## Tutorial Contents

### Part 1 — What Is a Neural Network?
- The brain analogy: neurons, weights, layers
- Activation functions (ReLU, sigmoid) explained in plain English
- Input → Hidden → Output architecture diagram

### Part 2 — How Neural Networks Learn
- The learning loop: guess → measure error → adjust → repeat
- Loss curves visualised
- Key terms: epoch, loss, backpropagation, learning rate

### Part 3 — Build a Single Neuron from Scratch
- Sigmoid activation coded by hand
- Weighted sum + bias + activation
- Test cases with football examples

### Part 4 — What Is Training Data?
- Features vs labels
- Train/test split and why it matters
- Overfitting explained

### Part 5 — Warm-Up: Student Pass/Fail Predictor
- Full training pipeline from scratch
- Decision boundary visualisation
- Confusion matrix and classification report

### Part 6 — The World Cup Prediction Project
- 1500-match synthetic dataset with 8 realistic features
- Exploratory data analysis (EDA) with histograms and correlation heatmap
- Feature engineering explanation

### Part 7 — Making Predictions
- 24-team database with real-world inspired stats
- `predict_match()` function with probability output
- Knockout bracket simulator
- Group stage round-robin simulator

### Part 8 — Improving the Model
- Underfitting vs overfitting vs good fit — visualised
- Hyperparameter search with GridSearchCV
- Permutation feature importance
- Probability calibration curves

### Part 9 — Where to Go from Here
- Real data sources (Kaggle, StatsBomb)
- Next topics: PyTorch, XGBoost, LSTM, Bayesian models
- Free learning resources

---

## Sample Output

```
====================================================
              Brazil  vs  Argentina
  Stage: Semi-Final
====================================================
  Brazil Win  :  58.2%  ████████████████
  Draw        :  29.4%  ████████
  Argentina Win:  12.4%  ███
────────────────────────────────────────────────────
  PREDICTED: BRAZIL WIN
====================================================
```

## Requirements

- Python 3.8+
- See `requirements.txt` for library versions
