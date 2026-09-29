# Wearable-Sensor-Exercise-Classification
# Practical Machine Learning Exercise Classification

This project uses wearable sensor data to predict how participants performed a barbell lifting exercise. Sensor measurements were collected from the belt, arm, dumbbell, and forearm, and the response variable `classe` represents five different exercise performance categories labeled A through E.

## Project Objective

The goal was to develop a machine learning model that accurately predicts exercise performance, evaluate its expected out-of-sample performance, and generate predictions for 20 provided test observations.

## Analysis Approach

The analysis included:

- Data cleaning and removal of variables with more than 95% missing values
- Removal of identifier, timestamp, and data collection variables
- Retention of 52 sensor-based predictors
- A 70% training and 30% holdout validation split
- Five fold cross validation
- Comparison of a classification tree and Random Forest model
- Evaluation of the final model using a confusion matrix and validation accuracy

## Results

The classification tree achieved a cross validated accuracy of approximately 69.12%.

The Random Forest achieved a cross validated accuracy of approximately 99.14% and was selected as the final model.

On the independent holdout validation dataset, the Random Forest achieved approximately 99.63% accuracy, corresponding to an estimated out-of-sample error of approximately 0.37%.

## Repository Files

- `Practical_Machine_Learning_Course_Project.Rmd` contains the complete reproducible R Markdown analysis.
- `Practical_Machine_Learning_Course_Project.html` contains the compiled report for viewing in a web browser.

## Final Prediction

The selected Random Forest model was refitted using the complete cleaned training dataset and used to predict the exercise classes for the 20 provided test observations.
