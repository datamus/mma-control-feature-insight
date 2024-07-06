# UFC Fight Outcome Prediction

## Introduction
Predicting fight outcomes with only two features might seem unconventional, but this project serves as a thought experiment and a bit of fun to explore the predictive power of machine learning models in the context of mixed martial arts (MMA). Control time is a crucial aspect of the fight game, often stirring controversy due to its significant influence on referees' decisions. Control can dramatically sway the outcome of a fight, even when no apparent damage is inflicted. This project not only aims to predict fight outcomes using control metrics but also seeks to identify which prediction method yields the best results, paving the way for a deeper analysis in the future.

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
- **Hyperparameter Setting**: I manually set specific hyperparameters for each model without performing cross-validation.
- **Model Evaluation**: Each model was trained on the training dataset and evaluated on the test dataset to calculate accuracy.
- **Reason for Predefined Training and Test Sets:** We predefined the training and test sets to facilitate backtesting of the models against the test set. This approach allows us to determine the overall Profit and Loss (PNL) of the models, ensuring a more realistic evaluation of their performance in a trading context.


\begin{table}[h!]
\centering
\begin{tabular}{|l|c|}
\hline
\textbf{Model} & \textbf{Accuracy} \\
\hline
Logistic Regression & 0.544 \\
Random Forest & 0.552 \\
Support Vector Machine & 0.562 \\
K-Nearest Neighbors & 0.548 \\
Gradient Boosting & 0.556 \\
Naive Bayes & 0.564 \\
\hline
\end{tabular}
\caption{Model Accuracy Results}
\label{tab:results}
\end{table}
