# Forecasting Oil Price Changes with a VAR Model

This repository contains an empirical project analyzing the dynamics of the global oil market using a **Vector Autoregression (VAR)** framework.  
The project follows the methodology of Kilian (2009) and applies a 3-variable VAR to study the interaction between:

- **Oil supply shocks** (percent change in global crude oil production, `dprod`)
- **Global demand shocks** (proxied by real activity index, `rea`)
- **Real oil price changes** (`rpo`)

## Project Objectives
1. Build and estimate a VAR(24) model of oil supply, demand, and price.  
2. Perform **Granger causality tests** to examine directional relationships.  
3. Analyze **Forecast Error Variance Decomposition (FEVD)** to measure the contribution of each shock.  
4. Compute **Impulse Response Functions (IRFs)** to assess dynamic effects of shocks.  
5. Recover **structural shocks** using recursive identification and Cholesky decomposition.  
6. Study the macroeconomic implications of structural oil shocks for **GDP** and **inflation**.

## Repository Structure
'''
├── data/ # input datasets (Excel, CSV, etc.)
├── scripts/ # main R code
├── results/ # figures, tables, model outputs
├── README.md # project documentation
├── LICENSE # license file
└── requirements.txt # required R packages
'''

## Requirements
The following R packages are required:
vars
lmtest
sandwich
tseries
dynlm
ggplot2
ggpubr
xts
readxl


## Install them in R with:
install.packages(c("vars", "lmtest", "sandwich", "tseries", 
                   "dynlm", "ggplot2", "ggpubr", "xts", "readxl"))

## How to Run
Clone this repository:
git clone https://github.com/yourusername/oil-var-forecasting.git
cd oil-var-forecasting
Place the dataset (oildata.xlsx) in the data/ folder.

Open scripts/var_model.R and run in RStudio or R console.

Output plots and results will be saved in the results/ folder.

## Results
VAR lag order selected: 24

Supply shocks explain a small share of oil price fluctuations.

Demand shocks have strong and persistent effects on both GDP and inflation.

IRFs show that oil price shocks propagate through the macroeconomy with delays.

## References
Kilian, L. (2009). "Not All Oil Price Shocks Are Alike: Disentangling Demand and Supply Shocks in the Crude Oil Market." American Economic Review.

Kilian, L., & Lütkepohl, H. (2017). Structural Vector Autoregressive Analysis. Cambridge University Press.
