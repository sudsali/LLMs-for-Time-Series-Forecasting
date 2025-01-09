# LLMs for Time Series Forecasting

This repository explores the application of Large Language Models (LLMs) for time series forecasting, comparing their performance against traditional forecasting methods using stock market data.

## Project Overview

This research investigates how LLMs can be adapted for time series forecasting, particularly in financial markets. The project compares various models including traditional approaches (ARIMA, XGBoost, LSTM) and LLM-based solutions (GPT-2, T5).

## Model Performance

| Model | RMSE |
|-------|------|
| GPT-2 | 51.39 |
| LSTM | 51.70 |
| T5 | 53.64 |
| ARIMA | 95.03 |
| XGBoost | 191.60 |

## Hyperparameter Optimization Results

**ARIMA**
- Best Configuration: p=2, d=0, q=2, P=1, D=0, Q=0, s=12
- Optimization Time: 2364.64 seconds

**XGBoost**
- Best Configuration:
```python
params = {		
	objective': 'reg:squarederror',		
	booster': 'gbtree',				
    max_depth: 1,
    learning_rate: 0.118,	
    n_estimators: 1000,
    min_child_weight: 6,	
    subsample: 0.92,	
    colsample_bytree: 0.59
	}		
```
- Optimization Time: 727.33 seconds

**LSTM**
- Best Configuration:
```python
params = {
    'hidden_layer_size': 61,
    'num_layers': 2,
    'dropout_rate': 0.178,
    'learning_rate': 0.0019,
    'batch_size': 16
}
```
- Optimization Time: 5748.93 seconds

## Repository Structure

```
├── data/
│   └── yahoo.csv
├── notebooks/
│   ├── ARIMA.ipynb
│   ├── LSTM.ipynb
│   ├── T5_stock.ipynb
│   ├── gpt_2_model.ipynb
│   └── xGBoost.ipynb
├── README.md
└── requirements.txt
```

## Getting Started

1. Clone the repository:
```bash
git clone https://github.com/yourusername/LLMs-for-Time-Series-Forecasting.git
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Run the notebooks in the following order:
- ARIMA.ipynb
- LSTM.ipynb
- xGBoost.ipynb
- gpt_2_model.ipynb
- T5_stock.ipynb
