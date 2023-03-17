# TFT Scenario Forecasting Tool
This repository is a supplement to the paper "Enhanced Conditional Forecasting During Disruptive Events Using a Temporal Fusion Transformer Model". It provides the original code and a supplementary forecasting tool. 

## Content Description
- Data: All data files (trade data, commodity data, weather data) in csv format
- Forecasters: The forecasting codes of the TFT and benchmark (SARIMAX) models (both regular and generalizability assessment). The Scenario Forecasting Tool can also be found here
- Pre-Trained Models: Pre-trained models used in the scenario forecasting tool
- Results Logs: Logs used to store results from training iterations
- Data Descriptive Analysis: jupyter notebook used for Section 4 of the research
- requirements.txt contains all the versions of the packages used in the virtual environment (note that not all packages are necessarily used in the coding)

## How to use the forecaster?
- Make sure that Pytorch is correctly installed!! (see: https://github.com/pytorch/pytorch#from-source for an extensive explanation)
- Change product type to desired target commodity
- Run all cells
- Change product type, energy price and trading intensity to generate scenario forecasts interactively 

## Intuition behind the forecaster (extensive explanation given in paper)
The forecaster aims to provide an indication of the Dutch import price of commodities (wheat, maize and sunflower oil) under different future war scenarios. These war scenario can be constructed using the trading intensity and energy prices, as these have shown to be the main price drivers of the commodities. Using these two topics, the effect of various future scenarios on the average import prices can be investigated. Examples may include:

Surging energy prices, but closed Black Sea Ports:
- Energy price: Very High
- Trading Intensity: Low

Mild winter, resulting in low energy prices and unchanged trading intensity:
- Energy price: Low
- Trading intensity: Moderate

In general, the energy prices seem to impact all three commodities whereas the trade intensity's effect is related to how dependent the Netherlands generally is on Ukraine for its imports.

The frame work of:
Isolating main prices drivers > Simulating future scenarios > Conditional Forecasting
can ofcourse also used in other new situations. The only true adaption that need to be made are changing the regressors, assigning sensible future values and retraining the Temporal Fusion Transformer
