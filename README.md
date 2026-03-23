# LSTM-ESN Fuel Cell Prediction Models

This repository contains Jupyter notebooks implementing hybrid Echo State Network (ESN) + LSTM models optimized via Genetic Algorithm (GA) for predicting key fuel cell performance metrics from time-series data.[file:2][file:4][file:1]

## Overview
The models combine an ESN reservoir layer with LSTM and Dense layers for time-series forecasting. Hyperparameters (ESN size, LSTM units, Dense units) are tuned using DEAP's Genetic Algorithm to minimize validation loss.[file:2]

Data includes fuel cell measurements like current, voltage, power, pressures, temperatures, and flows across cycles.[file:4]

## Notebooks
| Notebook | Target Variable | Description |
|----------|-----------------|-------------|
| [LSTM-ESN-Voltage.ipynb](LSTM-ESN-Voltage.ipynb) | Voltage ratio | GA-tuned ESN-LSTM for voltage prediction [file:2] |
| [LSTM-ESN-Power-4.ipynb](LSTM-ESN-Power-4.ipynb) | Power | GA-tuned ESN-LSTM for power prediction [file:4] |
| [LSTM-ESN-Energy-2.ipynb](LSTM-ESN-Energy-2.ipynb) | Energy | GA-tuned ESN-LSTM for energy prediction [file:1] |
| [LSTM-ESN-Energy-cathode-inlet-3.ipynb](LSTM-ESN-Energy-cathode-inlet-3.ipynb) | Energy (cathode inlet focus) | Variant focusing on cathode inlet conditions [file:3] |

## Key Features
- Custom Keras ESN layer implementation[file:2]
- Data preprocessing: scaling, train-test split, sequence creation[file:4]
- Model evaluation: MSE, RMSE, MAE, R², plots[file:1]
- GA optimization over 10 generations, population 20[file:2]

## Usage
1. Install dependencies: `pip install -r requirements.txt` (numpy, pandas, tensorflow, keras, deap, esn, scikit-learn, matplotlib)
2. Run notebooks sequentially for training/evaluation[file:4]

## Results Summary
Models achieve low validation loss post-GA tuning, with visualizations of training curves, predictions vs actuals.[file:1][file:2]

Authored by Katleho Mokhele (inferred from notebook metadata).[file:4]
