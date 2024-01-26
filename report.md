# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
The goal is to determine if the logistic regression model can be accurate in predicting healthy loans versus high risk loans using original data versus resampled data to increase the size of the minority class 

* Explain what financial information the data was on, and what you needed to predict.
loan_status is the predictions 

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
original
values_counts
0   75036
1   2500

oversampled
0   56271
1   56271

* Describe the stages of the machine learning process you went through as part of this analysis.
1. Prepare the data
2. Separate the data to features which X is the columns and y is the outcome 
3. train_test_split
4. Pick the ML model for classification (Logistic Regression)
5. Fit the model with training data
6. Use the model to make predictions with the test data so 25% default test data to be evaluated
7. Evaulate the predictions comparing metrics, confusion matrix, clasification report

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
SKLearn LogisticRegression
train_test_split
confusion_matrix
classification_report

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 
  * Accuracy: 0.99
  * Precision Class 0: 1.00, Class 1: 0.85
  * Recall Class 0: 0.99, Class 1: 0.91



* Machine Learning Model 2:
  * Description of Model 1 
  * Accuracy: 0.99
  * Precision Class 0: 1.00, Class 1: 0.04
  * Recall Class 0: 0.99, Class 1: 0.99

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
Overall the logistic regression performs the best as the prediction the outcome 0 (healthy loans) for class 0 and both the precision and recall were really high

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
For class 1, the high risk loans, the model precision is 0.04 and the recall 0.91. This indicates the model more often gives false positives than false negatives

Given the info, it appears the logistic regression models don't do a great job at predicting both the healthy and high risk loans given the features that used to training set data


If you do not recommend any of the models, please justify your reasoning.
Although the logistic regressions seems promising, it would need to be evaluated against different data sets to confirm that it should be put into use for prediction health status of loans