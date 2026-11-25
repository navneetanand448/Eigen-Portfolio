# Eigen Portfolio Analysis

This Jupyter notebook downloads adjusted daily closing prices for 30 Dow Jones
Industrial Average companies from Yahoo Finance, calculates daily returns,
filters outliers, and uses principal component analysis (PCA) to explore and
backtest eigen-portfolios.

## Requirements

- Python 3.10 or later
- An internet connection to download price data from Yahoo Finance

## Setup on Windows

Open PowerShell in this project folder and run:

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
jupyter lab
```

Open `Eigen Portfolio[1].ipynb` in JupyterLab and choose **Run All Cells**.
The notebook downloads adjusted prices starting in 2000, so no local CSV file
is needed. Its analysis uses dates with available prices for all selected
tickers.

Yahoo Finance data availability and ticker histories can change over time.

## Analysis

- Download adjusted daily closing prices from Yahoo Finance
- Clean price data and calculate daily log and linear returns
- Remove return observations beyond three standard deviations
- Visualize returns and correlations
- Fit PCA, inspect eigen-portfolios, and compare backtest results
