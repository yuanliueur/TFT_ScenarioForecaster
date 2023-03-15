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
