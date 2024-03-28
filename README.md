# Module 12 Report

## Overview

The purpose of this analysis is to develop a model utilizing existing customer data that can predict credit-risk of banking clients requesting a loan.  

Model training and analysis was all done with scikit-learn in Python ([file](Credit_Risk/credit_risk_classification.ipynb)).  [Data](Credit_Risk/Resources/lending_data.csv) from existing customers on loan status (healthy or high risk of default), loan size, interest rate, borrower income, debt to income, number of accounts, derogatory marks, and total debt was split into training data and testing data with scikit-learn train_test_split.  The training data was then used to train a logistic regression model with scikit-learn to determine if loan status would be healthy or high risk based on client characteristics.  To assess the effectiveness of the model, the test data from existing customers was used to make loan status predictions.  These predictions we compared against actual loan status, and used to create a scikit-learn confusion matrix and classification report.  

## Results

Confusion Matrix: 
- [18679, 80], [67, 558]
  - Confusion matrix indicates prescence of false negatives and false positives

Classification Report:
- Accuracy: Accuracy value of 0.99 indicates a strong ability of this model to make predictions.
- Healthy Loan: Precision = 1.00, Recall = 1.00, F1-Score = 1.00, Support = 18759
  - There is high precision, recall, and F-1 score indicating that this model is very effective at identifying "Healthy" loans.
- High-Risk Loan: Precision = 0.87, Recall = 0.89, F1-Score = 0.88, Support = 625
  - There is fairly strong precision, recall, and F-1 scores, indicating that this model is decent at identifying "High-Risk" loans.

## Summary

This model shows more difficulty in predicting high risk loans compared to predicting healthy loans. It would be important to not only minimize false-negatives (potentially not giving loans to individuals that are low risk of default) but also minimize false-positives (potentially giving loans to individuals that are high risk of default).

With a strong 99% accuracy rate I would recommend this model. It is able to capture individuals with healthy loan status, while still minimizing mislabelling of those at a high risk of default.
