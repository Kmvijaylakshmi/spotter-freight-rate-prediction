# Spotter Freight Rate Prediction

## Overview

This project was completed as part of the Spotter Machine Learning Assessment.

The objective is to build a machine learning regression model that predicts freight **posted_rate** using historical shipment data and generate predictions for the provided validation dataset.

---

## Project Structure

```
spotter-freight-rate-prediction/
│
├── README.md
├── Spotter_Freight_Rate_Assessment.ipynb
├── requirements.txt
├── validation_predictions.csv
├── december_predictions.csv
├── candidate_december.png
└── score.py
```

---

## Dataset

The assessment consists of:

- Training dataset: 48,000 shipment records
- Validation dataset: 12,000 shipment records

Target Variable:

- **posted_rate**

---

## Data Preprocessing

The following preprocessing steps were performed:

- Converted `date` into datetime format.
- Extracted:
  - Year
  - Month
  - Day
  - Day of Week
  - Week of Year
- Filled missing values in:
  - `weight`
  - `market_index`
- Used CatBoost native handling for categorical features.

---

## Model

**Algorithm:** CatBoost Regressor

### Parameters

- Iterations: 1000
- Learning Rate: 0.05
- Depth: 8
- Loss Function: RMSE
- Random State: 42

---

## Validation Strategy

- 80% Training Data
- 20% Validation Data
- Random Train-Test Split

---

## Evaluation Metrics

The model was evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score

---

## Generated Files

- validation_predictions.csv
- december_predictions.csv
- candidate_december.png

---

## Validation

The generated files were successfully validated using the provided `score.py` script.

Validation Output:

```
Validated 12,000 final predictions.
Validated 31 fixed December predictions.
Created chart: scorer_results/candidate_december.png
Final validation metrics are calculated by Spotter after submission.
```

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- CatBoost
- Matplotlib
- Seaborn

---

## Author

**Km Vijay Lakshmi**
