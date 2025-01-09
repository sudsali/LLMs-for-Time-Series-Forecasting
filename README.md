# LLMs-for-Time-Series-Forecasting

# LLMs for Time Series Forecasting

This repository explores the application of Large Language Models (LLMs) for time series forecasting, comparing their performance against traditional forecasting methods using stock market data.

## Project Overview

This research investigates how LLMs can be adapted for time series forecasting, particularly in financial markets. The project compares various models including traditional approaches (ARIMA, XGBoost, LSTM) and LLM-based solutions (GPT-2, T5).

## Models and Performance

| Model | RMSE Score |
|-------|------------|
| ARIMA | 97.682 |
| GPT-2 | 51.39 |
| T5 | 53.64 |
| LSTM | 65.85 |
| XGBoost | 191.603 |

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

## Dataset

The project uses historical stock market data from Yahoo Finance covering the period 2015-2020, with a standardized sequence length of 60 days for all models.

## Implementation Details

**Data Preprocessing**
- Standardized sequence length of 60 days
- Numerical data encoded as text for LLM compatibility
- MinMax scaling for normalized values

**Model Architecture**
- Traditional Models: ARIMA, XGBoost, LSTM implementations
- LLM Models: Adapted GPT-2 and T5 for numerical sequence prediction
- Evaluation using RMSE (Root Mean Square Error)

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

## Future Work

- Exploration of longer sequence lengths
- Integration of textual data with numerical sequences
- Development of specialized LLM architectures for time series
