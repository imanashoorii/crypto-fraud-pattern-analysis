# Crypto Fraud Pattern Analysis

An exploratory data analysis of 20,000 crypto exchange transactions, investigating where and how scam activity concentrates — and testing common fraud-detection assumptions directly against the data.

## Overview

Simulating a consulting engagement for a mid-sized crypto exchange's Fraud & Compliance team, this project explores transaction-level and wallet-level behavioural signals to answer concrete business questions:

- Which blockchains and platforms carry the highest scam rates?
- Are there time-of-day or day-of-week patterns in scam activity?
- Do transactions on unidentified ("Unknown") platforms carry more risk?
- Does sender wallet age predict scam risk?
- Is the exchange's internal `anomaly_score` a reliable fraud indicator?

The strongest finding: wallets younger than 30 days show a **45.8% scam rate** — roughly 9x every other age group — making wallet age the single most actionable signal in the dataset.

## Dataset

[Crypto Scam Transaction Dataset](https://www.kaggle.com/datasets/muhammadhussnain09/crypto-scam-transaction-dataset) (Kaggle) — 20,000 synthetic transactions across 18 features (blockchain, platform, wallet age, transaction amount, gas fees, velocity/anomaly scores, scam label), generated via behavioural heuristics.

## Structure

```
├── crypto-fraud-pattern-analysis.ipynb   # Main analysis notebook
├── data/
│   └── crypto_scam_transaction_dataset.csv
└── README.md
```

## Tech stack

Python · pandas · NumPy · Matplotlib · Seaborn · Jupyter

## Running it

```bash
pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook crypto-fraud-pattern-analysis.ipynb
```

The notebook loads the dataset directly from this repo, so it runs end to end with no additional setup.

## Author

Iman Ashoori