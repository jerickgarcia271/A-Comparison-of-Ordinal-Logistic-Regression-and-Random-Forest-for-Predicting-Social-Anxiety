# Predicting Social Anxiety Levels Using Behavioral, Lifestyle, and Psychological Factors: A Comparison of Ordinal Logistic Regression and Random Forest

## Overview

This project develops predictive models for estimating an individual's **social anxiety level** using demographic, behavioral, lifestyle, physiological, and psychological factors. The study compares a traditional **Ordinal Logistic Regression** model with a **Random Forest** classifier to determine which approach better predicts ordered anxiety severity.

The project demonstrates a complete machine learning workflow, including data preprocessing, exploratory data analysis (EDA), feature engineering, model training, evaluation, and interpretation. It also highlights the differences between interpretable statistical models and nonlinear machine learning algorithms when applied to ordinal outcomes.

---

## Project Highlights

- Compared **Ordinal Logistic Regression** and **Random Forest** for predicting ordered social anxiety levels.
- Achieved a **Quadratic Weighted Cohen's Kappa of 0.8456** using Random Forest.
- Identified **Stress Level, Sleep Hours, and Caffeine Intake** as the strongest predictors of social anxiety.
- Implemented a complete machine learning workflow including preprocessing, EDA, model development, evaluation, and feature importance analysis.

---

## Objectives

The project aims to:

- Predict social anxiety levels using behavioral, lifestyle, physiological, and psychological variables.
- Compare the predictive performance of Ordinal Logistic Regression and Random Forest.
- Identify the most influential factors associated with increasing social anxiety.
- Demonstrate a complete supervised machine learning workflow for an ordinal classification problem.
- Evaluate model performance using both conventional classification metrics and ordinal-specific evaluation measures.

---

## Dataset

The dataset contains **10,000+ observations** representing individuals with varying levels of social anxiety.

### Features

#### Demographic Variables
- Age
- Gender
- Occupation

#### Lifestyle Variables
- Sleep Hours
- Physical Activity
- Diet Quality
- Caffeine Intake
- Alcohol Consumption
- Smoking Status

#### Physiological Indicators
- Heart Rate
- Breathing Rate
- Sweating Level
- Dizziness

#### Mental Health Indicators
- Stress Level
- Family History of Anxiety
- Medication Usage
- Therapy Sessions

#### Life Events
- Recent Major Life Event

#### Target Variable
- Anxiety Level (1–10)

**Dataset Source**

- https://www.kaggle.com/datasets/natezhang123/social-anxiety-dataset

- **Note**: The data is already pre-cleaned so minimal pre-processing was done.

---

## Methodology

The project follows a standard supervised machine learning workflow:

1. Data preprocessing
   - Binary encoding
   - One-hot encoding
   - Feature scaling (Ordinal Logistic Regression)

2. Exploratory Data Analysis (EDA)
   - Data preview
   - Correlation exploration (Heatmaps)
   - **Note**: The dataset was already explored prior so I didn't put much here

3. Model Development
   - Ordinal Logistic Regression
   - Random Forest Classifier

4. Model Evaluation
   - Accuracy
   - Precision
   - Recall
   - F1-score
   - Mean Absolute Error (MAE)
   - Quadratic Weighted Cohen's Kappa
   - Confusion Matrix

5. Feature Importance Analysis

---

## Results

| Metric | Ordinal Logistic Regression | Random Forest |
|:-------------------------------|:---------------------------:|:-------------:|
| Accuracy | 23.05% | **34.45%** |
| Weighted Precision | 24.90% | **33.52%** |
| Weighted Recall | 23.05% | **34.45%** |
| Weighted F1-score | 21.39% | **33.34%** |
| Mean Absolute Error | 1.2250 | **0.8523** |
| Quadratic Weighted Cohen's Kappa | 0.7454 | **0.8456** |

The Random Forest classifier consistently outperformed the Ordinal Logistic Regression model across every evaluation metric, indicating that nonlinear machine learning methods better captured the relationships among behavioral, lifestyle, physiological, and psychological variables in this dataset.

---

## Feature Importance

The Random Forest model identified the following variables as the strongest predictors of social anxiety:

| Rank | Feature |
|-----:|---------|
| 1 | Stress Level |
| 2 | Sleep Hours |
| 3 | Caffeine Intake |
| 4 | Physical Activity |
| 5 | Heart Rate |
| 6 | Age |
| 7 | Alcohol Consumption |
| 8 | Breathing Rate |
| 9 | Diet Quality |
| 10 | Therapy Sessions |

Behavioral, physiological, and lifestyle variables contributed substantially more to prediction than demographic characteristics such as gender and occupation.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Statsmodels
- Google Colab

---

## Repository Structure

```text
├── Social_Anxiety_Prediction.ipynb
├── enhanced_anxiety_dataset.csv
├── README.md
```

---

## Future Improvements

Potential extensions include:

- Hyperparameter optimization using GridSearchCV or RandomizedSearchCV.
- Addressing class imbalance through resampling techniques such as SMOTE or class weighting.
- Evaluating additional machine learning models (XGBoost, LightGBM, CatBoost).
- Applying explainable AI techniques such as SHAP values.
- Validating the models using real-world clinical datasets.

---

## Author

**Jerick L. Garcia**

Bachelor of Science in Mathematics  
**University of the Philippines Diliman**
