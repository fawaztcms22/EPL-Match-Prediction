PREDICTING EPL MATCH OUTCOMES USING MACHINE LEARNING 

  Table Of Contents
  1.Overview
  2.Features and Functionality
  3.Input Data Format
  4.Output Data/Plots/Tables
  5.Parameters and Hyperparameters
  6.Challenges and Issues Faced

1. Overview
This project aims to predict the outcomes of EPL matches using three machine learning models: Logistic Regression, Support Vector Classifier (SVC), and Random Forest. the models are trained on historical match data and predict whether a game will win by home team or away team or will it be draw.

2. Features and Functionality
Data Preprocessing: The code loads with match data and selected it based on the team and year. then prepares the features for model training.
Model Training: The model will train three different machine learning models on historical match data.
Prediction: Uses the trained models to predict the outcomes of new matches.
Evaluation: Compares the prediction with actual match results and evaluates the model accuracy.
Visualization: Plots the actual versus predicted results for better understanding.

4. Input Data Format
That dataset contains following columns:
Date- date of the match
HomeTeam- name of home team
AwayTeam- name of away team
FTHG- full time home goals
FTAG- full time away goals 
HS- home shots
AS- away shots
HST- home shots on target
AST- away shots on target
FTR- full time result (H for home win, A for away win, D for draw)
However, in the code only a selection of features is used. Specifically, the features used include HomeTeam, AwayTeam, HomeForm, AwayForm, AvgHomeGoalsScored, AvgHomeGoalsConceded, AvgAwayGoalsScored, and AvgAwayGoalsConceded. Others features like Shots, Half-Time Goals, Half-Time Result, and Date columns are dropped during preprocessing because these are recorded live and are only available after the game is played. Since we want to predict the match outcome beforehand, these wouldn’t be helpful for pre-game predictions.

4. Output Data/Plots/Tables
The output includes:
Predictions: A table comparing actual match results with the predictions from the three models.
Accuracy Metrics: Display the accuracy, precision, recall, and F1- score for each model.
Plots: Line plots showing the actual vs predicted outcomes for each model over time.

5.Parameters and Hyperparameters
Parameters:
team_name: The name of the team which predictions are to be made (e.g: Arsenal)
year: The year for which the match data is to be filtered (e.g: 2012)
Hyperparameters:
Logistic Regression- 'max_iter': Maximum number of iterations for the solver (e.g: 200)
SVC- 'kernel': Type of kernal to be used in the algorithm (e.g: linear)
Random Forest- 'n_estimators': Number of trees in the forest (e.g: 100)

6.Challenges and Issues Faced
Data Availability:  Finding enough good quality data to train the models. inconsistent data format also required careful preprocessing.
Model Performance: Ensuring the models do not overfit and can generalize to new data.
Hyperparameter Tuning: Finding the best hyperparameters for each model required for multiple iterations and testing
Handling Draws: Predicting draw is particularly challenging because they are less frequent and the models often struggle to compare the matches that might result in a draw.
 
