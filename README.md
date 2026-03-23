# LSTM-ESN Fuel Cell Prediction Models

This repository contains Jupyter notebooks implementing hybrid Echo State Network (ESN) + LSTM models optimized via Genetic Algorithm (GA) for predicting key fuel cell performance metrics from time-series data.[file:2][file:4][file:1]

## Overview
The models combine an ESN reservoir layer with LSTM and Dense layers for time-series forecasting. Hyperparameters (ESN size, LSTM units, Dense units) are tuned using DEAP's Genetic Algorithm to minimize validation loss.[file:2]

Data includes fuel cell measurements like current, voltage, power, pressures, temperatures, and flows across cycles.[file:4]

## Notebooks
| Notebook | Target Variable | Description |
|----------|-----------------|-------------|
| LSTM-ESN-Voltage.ipynb | Voltage ratio | GA-tuned ESN-LSTM for voltage prediction |
| LSTM-ESN-Power-4.ipynb | Power | GA-tuned ESN-LSTM for power prediction |
| LSTM-ESN-Energy-2.ipynb| Energy | GA-tuned ESN-LSTM for energy prediction  |
| LSTM-ESN-Energy-cathode-inlet-3.ipynb | Energy (cathode inlet focus) | Variant focusing on cathode inlet conditions  |

## Key Features
- Custom Keras ESN layer implementation
- Data preprocessing: scaling, train-test split, sequence creation
- Model evaluation: MSE, RMSE, MAE, R², plots
- GA optimization over 10 generations, population 20

## Usage
1. Install dependencies: `pip install -r requirements.txt` (numpy, pandas, tensorflow, keras, deap, esn, scikit-learn, matplotlib)
2. Run notebooks sequentially for training/evaluation[file:4]

## Results Summary
Models achieve low validation loss post-GA tuning, with visualizations of training curves, predictions vs actuals.[file:1][file:2]

Authored by Katleho Mokhele (inferred from notebook metadata).[file:4]
