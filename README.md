# ROADS-X

An explainable machine learning system for predicting traffic accident severity and analyzing the factors associated with accident outcomes. The project compares multiple machine learning models and uses SHAP to provide interpretable insights into model predictions.

## Overview

Traffic accident datasets contain a wide range of environmental, temporal, and road-related attributes that can influence accident severity. This project applies machine learning to classify accident severity while incorporating explainability techniques to understand the factors contributing to predictions.

The system uses the **US Accidents dataset** and evaluates Decision Tree and XGBoost models for accident severity classification.

## Features

* Accident severity classification using machine learning
* Comparison of Decision Tree and XGBoost models
* Feature importance analysis
* SHAP-based model explainability
* Identification of important factors influencing accident severity
* Data processing and analytical feature extraction using DuckDB

## Dataset

The project uses the **US Accidents dataset** containing approximately 3 GB of data.

For the current experiment:

* Samples used: **100,000**
* Features: **51**
* Target: **Accident Severity**
* Severity classes: **1–4**

The dataset is not included in this repository.

## Models

Two models were evaluated:

| Model         | Train Accuracy | Test Accuracy |
| ------------- | -------------: | ------------: |
| Decision Tree |         88.40% |        87.39% |
| XGBoost       |         95.99% |    **90.49%** |

XGBoost achieved the highest test accuracy among the evaluated models.

## Explainability

The project uses **SHAP (SHapley Additive exPlanations)** to interpret model predictions and identify the features that contribute to accident severity classification.

This allows the system to go beyond prediction by providing insights into **which factors influence the model's decisions**.

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
├── README.md
└── requirements.txt
```

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/<your-username>/Explainable-Traffic-Accident-Prediction.git
cd Explainable-Traffic-Accident-Prediction
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Dataset

Download the US Accidents dataset from Kaggle and update the dataset path in the notebook.

### 4. Run the notebook

Open:

```text
traffic_accident_prediction.ipynb
```

using Jupyter Notebook, JupyterLab, or VS Code and execute the cells sequentially.

## Results

The XGBoost model achieved a **90.49% test accuracy** on the 100,000-sample experimental dataset.

SHAP analysis was then used to examine feature contributions and provide an interpretable view of the model's accident severity predictions.

## Future Improvements

* Evaluate the models on a larger portion of the dataset
* Perform hyperparameter tuning and cross-validation
* Address class imbalance using appropriate sampling or weighting techniques
* Add interactive visualizations for accident factor analysis
* Develop a web interface for real-time prediction and explanation

## Author

**[Your Name]**

[GitHub](https://github.com/<your-username>)
