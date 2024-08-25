# Temperature Prediction Model

## Overview

This project demonstrates a temperature prediction model using LSTM (Long Short-Term Memory) neural networks. The model predicts future temperatures based on historical data from India, incorporating data preprocessing, model training, and evaluation.

## Requirements

To run this project, you'll need the following Python packages:

- **TensorFlow**
- **Pandas**
- **NumPy**
- **scikit-learn**
- **joblib**
- **Matplotlib**

You can install the necessary packages using pip:

```bash
pip install tensorflow pandas numpy scikit-learn joblib matplotlib
```

## Dataset

Data is taken from https://www.kaggle.com

The raw data comes from the Berkeley Earth data page.

Data source -
https://www.kaggle.com/datasets/berkeleyearth/climate-change-earth-surface-temperature-data?resource=download&select=GlobalLandTemperaturesByCountry.csv

The dataset used is `GlobalLandTemperaturesByCountry.csv`, which contains historical temperature data for various countries. This project focuses on data from India.

## Project Structure

1. **Imports**: Essential libraries for data manipulation, model building, and saving.
2. **Data Importing**: Loads temperature data from a CSV file.
3. **Preprocessing**:
   - Filters data to include only records for India.
   - Converts dates to a suitable format.
   - Normalizes temperature values.
   - Creates sequences for training and testing the model.
4. **Model Building**:
   - Defines an LSTM model to predict temperatures.
   - Compiles and trains the model using the prepared data.
5. **Prediction & Evaluation**:
   - Makes predictions on test data.
   - Inverse transforms predictions to the original scale.
   - Plots actual vs. predicted temperatures for evaluation.
6. **Saving the Model**:
   - Saves the trained model for future use.
   - Saves the scaler used for normalization.

## Usage

1. **Run the Code**: Execute the provided code to preprocess data, build and train the model, and evaluate its performance.
2. **Model and Scaler**:
   - The model is saved to a file, allowing you to reload it for future predictions.
   - The scaler is saved to ensure consistent data normalization when making new predictions.

## Potential Uses

- **Forecasting**: Predict future temperatures based on historical data.
- **Weather Analysis**: Compare predicted temperatures with actual data to identify trends or anomalies.
- **Research**: Analyze model performance and the influence of historical temperatures on future predictions.

## Notes

- The dataset may have missing daily temperature values, which can affect model accuracy. Thus has been removed while preprocessing the data.
- Incorporating additional data and features could enhance the model's performance.

---