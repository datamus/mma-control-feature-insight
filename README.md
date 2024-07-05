# UFC Fight Outcome Prediction

## Introduction
Predicting fight outcomes using only two features might seem unconventional, but this project is designed as a thought experiment and a bit of fun. Control time is a crucial aspect of the fight game, often stirring controversy. Despite causing no direct damage, shifts in control can significantly influence referees' opinions and swing the fight in unexpected directions. This project aims to explore the predictive power of control time statistics in determining UFC fight outcomes.

## Experiment Setup
- **Data**: The dataset contains information about UFC fights, including average control time and average control time against for each fighter.
- **Features**: `CTRL_mean` (average control time) and `CTRL against_mean` (average control time against).
- **Target Variable**: `OUTCOME` (binary outcome: 0 or 1).
- **Data Preparation**:
  - A rolling average was calculated for each fighter to smooth out short-term fluctuations and highlight longer-term trends in their performance.
  - Each row in the dataset represents the differential of the two features (average control time and average control time against) between the two fighters in a respective fight.

## Methods and Models
We evaluated the following machine learning models:
1. Logistic Regression
2. Random Forest Classifier
3. Support Vector Machine (SVM)
4. K-Nearest Neighbors (KNN)
5. Gradient Boosting Classifier (e.g., XGBoost)
6. Naive Bayes Classifier
7. Neural Networks

## Hyperparameter Tuning and Cross-Validation
- **Hyperparameter Tuning**: We used `GridSearchCV` to perform hyperparameter tuning for each model.
- **Cross-Validation**: 5-fold cross-validation was used to evaluate the models.
- **Cross-Validation**: 5-fold cross-validation was used to evaluate the models.
