# Building Energy Forecasting using LSTM and LSTM-GRU

## 1. Project Overview

This project investigates deep learning approaches for short-term building electricity consumption forecasting.

Two recurrent neural network architectures are evaluated:

- Standalone LSTM
- Hybrid LSTM-GRU

A Persistence Baseline is also implemented as a reference forecasting model.

## 2. Forecasting Objective

The objective is to predict the next hour of electricity consumption using the previous 24 hours of historical consumption data.

- Input window: 24 hours
- Forecast horizon: 1 hour ahead
- Target variable: `Robin_office_Gayle`

## 3. Dataset

**Building Data Genome Project 2**

Source: [Kaggle Dataset](https://www.kaggle.com/datasets/claytonmiller/buildingdatagenomeproject2)

The dataset contains hourly building energy consumption measurements.

## 4. Models Architecture

### Model 1: Standalone LSTM

- LSTM layer (32 units)
- Dropout
- Dense output layer

### Model 2: LSTM-GRU Hybrid

- LSTM layer (32 units, return_sequences=True)
- GRU layer (16 units)
- Dense output layer

### Baseline: Persistence

The last observed electricity consumption value is used as the prediction for the next hour.

## 5. Evaluation Metrics

The models are evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- Mean Absolute Percentage Error (MAPE)

## 6. Experimental Results

The LSTM-GRU hybrid model outperformed the standalone LSTM model in the conducted experiment.

| Metric | Improvement |
|---|---:|
| MAE | 6.12% |
| RMSE | 5.76% |
| MAPE | 4.71% |

These results indicate improved forecasting performance from combining LSTM and GRU layers in this experiment.

## 7. Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- TensorFlow / Keras
- Kaggle Notebooks

## 8. Project Status

Completed experimental implementation and model comparison.

Further work may explore multi-step forecasting, model optimization, and integration with AI-based building energy management systems.

## 9. Author

Hassan M. El-Bastawesy

GitHub: [hassan-ai-main](https://github.com/hassan-ai-main)
