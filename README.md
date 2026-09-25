# ROADS-X

An explainable machine learning system for predicting traffic accident severity and analyzing the factors associated with accident outcomes. The project compares Decision Tree and XGBoost models and uses SHAP to interpret model predictions.

## Overview

Traffic accident data contains environmental, temporal, road, and other contextual attributes that can influence accident severity. This project applies machine learning to classify accident severity while using explainability techniques to understand the factors influencing model predictions.

The project uses the **US Accidents dataset** and evaluates Decision Tree and XGBoost models for accident severity classification.

## Features

* Accident severity classification using machine learning
* Comparison of Decision Tree and XGBoost models
* Feature importance analysis
* SHAP-based model explainability
* Analysis of factors influencing accident severity
* Data processing and analytical feature extraction using DuckDB

## Dataset

The project uses the **US Accidents dataset** from Kaggle.

For the current experiment:

* Dataset size: Approximately 3 GB
* Samples used: **100,000**
* Features: **51**
* Target: **Accident Severity**
* Severity classes: **1–4**

The dataset is not included in this repository.

## Model Comparison

Two machine learning models were evaluated:

| Model         | Train Accuracy | Test Accuracy |
| ------------- | -------------: | ------------: |
| Decision Tree |         88.40% |        87.39% |
| XGBoost       |         95.99% |    **90.49%** |

XGBoost achieved the highest test accuracy among the evaluated models.

## Explainability

The project uses **SHAP (SHapley Additive exPlanations)** to interpret the XGBoost model and analyze the contribution of individual features to accident severity predictions.

This helps identify the factors that have the greatest influence on the model's predictions and provides a more interpretable view of the classification results.

## Tech Stack

* **Language:** Python
* **Machine Learning:** XGBoost, Scikit-learn
* **Explainability:** SHAP
* **Data Processing:** Pandas, DuckDB
* **Dataset:** US Accidents
* **Environment:** Jupyter Notebook

## Project Structure

```text
Explainable-Traffic-Accident-Prediction/
│
├── traffic_accident_prediction.ipynb
└── README.md
```

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/<your-username>/Explainable-Traffic-Accident-Prediction.git
cd Explainable-Traffic-Accident-Prediction
```

### 2. Install the required libraries

The notebook requires Python libraries including:

```bash
pip install pandas numpy scikit-learn xgboost shap duckdb matplotlib seaborn
```

### 3. Dataset

Download the **US Accidents dataset** from Kaggle and update the dataset path in the notebook.

The dataset is not included in this repository due to its size.

### 4. Run the notebook

Open `ROADS-X.ipynb` using Jupyter Notebook, JupyterLab, or VS Code and run the cells sequentially.

## Results

The XGBoost model achieved a **90.49% test accuracy** on the 100,000-sample experimental dataset, compared with **87.39%** for the Decision Tree model.

SHAP analysis was used to further interpret the XGBoost predictions and examine the contribution of individual features to accident severity classification.

## Future Improvements

* Evaluate the models on a larger portion of the dataset
* Perform hyperparameter tuning and cross-validation
* Address class imbalance using appropriate sampling or class-weighting techniques
* Add interactive visualizations for accident factor analysis
* Develop a web interface for prediction and explanation


