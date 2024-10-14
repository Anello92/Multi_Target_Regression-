# Multi-Target Regression for Predicting Macroeconomic Indicators

## Overview

This project demonstrates the use of **multi-target regression** to predict several macroeconomic indicators (GDP, inflation, and unemployment rate) using a **Random Forest Regressor** as the base model. The technique allows us to predict more than one target variable simultaneously, which can be especially useful in scenarios where the output variables are correlated or where you want to optimize predictions across multiple outputs at once.

The dataset used is synthetically generated to mimic real-world macroeconomic data patterns, such as the relationship between interest rates, exchange rates, industrial production, and their impact on GDP, inflation, and unemployment rates.

## Table of Contents

- [Project Structure](#project-structure)
- [Installation](#installation)
- [Data Overview](#data-overview)
- [Modeling Approach](#modeling-approach)
- [Evaluation Metrics](#evaluation-metrics)
- [Results](#results)
- [Future Improvements](#future-improvements)

## Project Structure

```
📁 Multi_Target_Regression
├── 📄 README.md                   # This file
├── 📄 Multi_Target_Regression.ipynb # Main Jupyter Notebook with code
└── 📁 data/                       # (optional) Folder for any real-world datasets if needed
```

## Installation

To run the notebook, you need to have **Python 3.x** and the following packages installed:

```bash
pip install numpy pandas scikit-learn jupyter
```

Alternatively, you can install the packages from the `requirements.txt` file (if available) using:

```bash
pip install -r requirements.txt
```

## Data Overview

The dataset is synthetically generated to simulate macroeconomic indicators. The input variables include:
- **Interest Rate**
- **Exchange Rate**
- **Industrial Production**

The target variables (outputs) are:
- **GDP (Gross Domestic Product)**
- **Inflation**
- **Unemployment Rate**

The relationships between these variables are built based on predefined mathematical formulas, including random noise to simulate real-world data variability.

## Modeling Approach

The project uses **multi-target regression**, implemented using the `MultiOutputRegressor` from the `scikit-learn` library. The underlying model used is a **Random Forest Regressor**, which works by creating individual regression trees for each target variable.

Key steps:
1. **Data Generation**: Generate synthetic data for inputs and outputs.
2. **Data Preprocessing**: Standardize the input variables using `StandardScaler`.
3. **Model Building**: Use `MultiOutputRegressor` to build and train a Random Forest model on the standardized input data.
4. **Prediction and Evaluation**: Use metrics like **Mean Squared Error (MSE)** and **R² (Coefficient of Determination)** to evaluate model performance for each target variable.

## Evaluation Metrics

The model's performance is evaluated using:
- **Mean Squared Error (MSE)**: Measures the average squared difference between actual and predicted values. The lower the value, the better.
- **R² (Coefficient of Determination)**: Indicates how well the model explains the variability in the data. Values closer to 1 indicate better performance.

## Results

After training the model on the synthetic dataset, we achieved competitive results for all three target variables (GDP, inflation, and unemployment rate), confirming that the model successfully learned the relationships between the input variables and macroeconomic indicators.

- **GDP**: R² = *X.XX*, MSE = *X.XX*
- **Inflation**: R² = *X.XX*, MSE = *X.XX*
- **Unemployment Rate**: R² = *X.XX*, MSE = *X.XX*

## Future Improvements

- **Use of Real Data**: The model can be extended to real-world macroeconomic data for further validation.
- **Other Algorithms**: Explore deep learning models, such as neural networks, that can naturally handle multi-target outputs.
- **Feature Engineering**: Include more economic indicators as input features for improved accuracy.
