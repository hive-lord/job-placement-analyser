# job-placement-analyser (job_placement _analyzer.ipynb)
My second ML project. This model entails logistic and linear regression models to find if you can get a job.

# Logistic + Linear Regression Comparison

This project demonstrates a comprehensive workflow for analyzing student career performance data using both **Logistic Regression** and **Linear Regression** models, with additional insights from Random Forest models. The notebook guides you through data cleaning, feature engineering, model training, evaluation, and visualization, with detailed markdown explanations for each step.

---

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Workflow Steps](#workflow-steps)
  - [1. Import Libraries](#1-import-libraries)
  - [2. Data Loading & Inspection](#2-data-loading--inspection)
  - [3. Data Cleaning & Preprocessing](#3-data-cleaning--preprocessing)
  - [4. Feature Engineering](#4-feature-engineering)
  - [5. Model Training & Evaluation](#5-model-training--evaluation)
  - [6. Visualization](#6-visualization)
  - [7. Insights](#7-insights)
- [How to Run](#how-to-run)
- [Requirements](#requirements)
- [Key Insights](#key-insights)
- [License](#license)

---

## Overview

The notebook `logistic + linear.ipynb` provides a step-by-step comparison of classification and regression approaches for predicting student placement outcomes and placement scores. It includes:

- Data cleaning and preprocessing
- Handling missing values and outliers
- Training and evaluating Logistic Regression and Random Forest Classifier for placement prediction (classification)
- Training and evaluating Linear Regression for placement score prediction (regression)
- Feature importance analysis
- Visualizations for model performance and comparison
- Key insights and summary

---

## Dataset

- **File:** `student_career_performance.csv`
- **Description:** Contains student records with features such as study hours, sleep hours, internships, projects, CGPA, placement score, and placement status.

*Note: The dataset file is not included in this repository. Please provide your own copy.*

---

## Workflow Steps

### 1. Import Libraries

All necessary libraries for data manipulation, visualization, and machine learning are imported, including:
- `pandas`, `numpy`
- `scikit-learn` (for models and metrics)
- `matplotlib`, `seaborn` (for plotting)

### 2. Data Loading & Inspection

- Load the dataset using pandas.
- Display the first few rows and dataset info to understand its structure and data types.

### 3. Data Cleaning & Preprocessing

- Handle missing values by filling them with median values for key columns.
- Remove outliers and logically inconsistent records (e.g., total hours in a day, CGPA limits, placement score anomalies).

### 4. Feature Engineering

- For **classification**: Use all features except `Placed` as predictors, and `Placed` as the target.
- For **regression**: Use all features except `Placement_Score` as predictors, and `Placement_Score` as the target.
- Drop unnecessary columns such as `Student_ID`.

### 5. Model Training & Evaluation

- **Logistic Regression**: Predicts whether a student is placed or not.
  - Evaluate using accuracy, precision, recall, F1 score, ROC AUC, and confusion matrix.
- **Random Forest Classifier**: Provides feature importance and a comparison classification model.
- **Linear Regression**: Predicts the placement score.
  - Evaluate using mean absolute error, mean squared error, root mean squared error.
  - Visualize actual vs. predicted scores.

### 6. Visualization

- Confusion matrix for classification results.
- Feature importance pie chart from Random Forest.
- Scatter plots for actual vs. predicted values.
- Comparison plot of linear vs. logistic regression predictions.

### 7. Insights

- Summarize the most important features, model performance, and observations about the data and predictions.

---

## How to Run

1. **Clone this repository.**
2. **Add the dataset**: Place `student_career_performance.csv` in the project directory.
3. **Open the notebook**: Launch `logistic + linear.ipynb` in Jupyter Notebook or VS Code.
4. **Run all cells**: Execute each cell sequentially to reproduce the analysis and visualizations.

---

## Requirements

- Python 3.x
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn

Install dependencies with:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

---

## Key Insights

- **Placement_Score** is the most important feature for predicting placement, as shown by Random Forest feature importance.
- Both Logistic Regression and Random Forest models achieve very high accuracy in predicting placement.
- Linear Regression predictions for Placement_Score are tightly clustered near 100, indicating low variance in the target variable.
- The comparison plot shows that logistic and linear regression models generally agree, with a few exceptions.

---

## License

This project is for educational purposes. Please cite appropriately if you use or adapt this work.

---

*For detailed explanations and step-by-step code, see the notebook with markdown explanations above each code cell.*

