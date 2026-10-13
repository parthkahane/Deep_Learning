# Assignment 4: LSTM-Based Time-Series Forecasting

## Overview

This project implements a Long Short-Term Memory (LSTM) neural network for time-series forecasting using historical weather data from the Jena Climate Dataset. The model learns temporal patterns from previous weather observations and predicts the temperature for the next hour.

## Problem Statement

Develop an LSTM-based model for time-series forecasting using stock price, weather, or sales datasets.

## Objectives

- Understand the working of LSTM networks for sequential data.
- Process and analyze historical weather observations.
- Predict future temperature using previous hourly observations.
- Evaluate the model using regression metrics.
- Visualize actual and predicted temperatures.

## Dataset

**Dataset Name:** Jena Climate Dataset

The dataset contains weather observations collected at a weather station in Jena, Germany. The original observations were recorded at 10-minute intervals.

The experiment resamples the observations into hourly data and uses the following features:

- Atmospheric pressure (`p (mbar)`)
- Air temperature (`T (degC)`)
- Potential temperature (`Tpot (K)`)
- Dew-point temperature (`Tdew (degC)`)
- Relative humidity (`rh (%)`)
- Wind velocity (`wv (m/s)`)
- Maximum wind velocity (`max. wv (m/s)`)

**Target variable:** Air temperature (`T (degC)`)

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- TensorFlow
- Keras
- LSTM Neural Networks

## Methodology

1. Download and load the Jena Climate Dataset.
2. Convert the date-time column into a datetime index.
3. Select relevant weather features.
4. Handle missing values using interpolation.
5. Resample the data into hourly observations.
6. Split the data into 80% training and 20% testing sets.
7. Apply Min-Max normalization.
8. Create sequences using the previous 24 hourly observations.
9. Build and train an LSTM model.
10. Predict temperature values on the test dataset.
11. Calculate evaluation metrics.
12. Plot actual versus predicted temperatures and training versus validation loss.

## Model Architecture

The LSTM model consists of:

- LSTM layer with 64 units
- Dropout layer with a rate of 0.2
- LSTM layer with 32 units
- Dropout layer with a rate of 0.2
- Dense layer with 16 neurons and ReLU activation
- Output Dense layer with 1 neuron

The model uses the Adam optimizer, Mean Squared Error (MSE) loss, and Mean Absolute Error (MAE) as a training metric. Early stopping is used to help prevent overfitting.

## Evaluation Metrics

- **MSE:** Mean Squared Error
- **RMSE:** Root Mean Squared Error
- **MAE:** Mean Absolute Error
- **R² Score:** Coefficient of determination

## Results

The reported evaluation results are:

| Metric | Value |
|---|---:|
| MSE | 11.6135 |
| RMSE | 3.4079 |
| MAE | 3.1376 |
| R² Score | 0.8228 |

The model achieved an R² score of 0.8228 on the test data, indicating that it captured a substantial portion of the variation in temperature observations.

## Visualizations

The implementation generates:

- Hourly temperature trend
- Actual versus predicted temperature graph
- Training and validation loss graph

## How to Run

1. Open Google Colab or a Python environment with the required dependencies.
2. Install the required libraries:

   ```bash
   pip install numpy pandas matplotlib scikit-learn tensorflow
   ```

3. Copy the assignment implementation into a notebook or Python file.
4. Run the code to download the dataset, preprocess the data, train the model, and evaluate the predictions.

The dataset is downloaded automatically by the implementation.

## Conclusion

This experiment demonstrates how LSTM networks can learn temporal relationships in weather data and forecast temperature from previous observations. The evaluation metrics and prediction plots help assess the model's forecasting performance.

## Author

**Parth Kahane**  
Department: CSE (AI)  
Vishwakarma Institute of Technology, Pune  
Subject: Deep Learning  
Practical No.: 4
