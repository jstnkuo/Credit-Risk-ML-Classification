## Overview of the Analysis

The purpose of this machine learning analysis is to build a predictive model to identify loan applicants who are likely to default on their loans. The analysis uses a dataset of loan applications and their corresponding outcomes (approved or denied) to train and test a logistic regression model. The initial model is then evaluated using balanced accuracy score, confusion matrix, and classification report.

Since the original dataset is imbalanced, with a significantly higher number of approved loans compared to denied loans, the analysis also employs random oversampling technique to address the imbalance. The oversampled dataset is then used to train and test a new logistic regression model, and its performance is evaluated using the same metrics as the initial model. The goal is to compare the performance of the original and oversampled models to determine if the oversampling technique has improved the accuracy of the model in predicting loan defaults.

The variable that the analysis was trying to predict is "loan_status", which represents the outcome of a loan application.

The stages of the machine learning process I went through as part of this analysis are as follows: 

1) Importing the necessary modules
2) Loading and reviewing the dataset
3) Separating the input and target variables
4) Splitting the data
5) Building the initial Logistic Regression model
6) Evaluating the performance of the initial mode
7) Applying random oversampling
8) Building the resampled Logistic Regression model
9) Evaluating the performance of the resampled model

In this analysis, several machine learning methods and techniques were used, including:

Logistic Regression: A supervised learning algorithm that is commonly used for binary classification problems like the one in this analysis. The LogisticRegression module from scikit-learn was used to instantiate and fit the logistic regression model to the training data.

Random Over Sampling: A technique used to address class imbalance in a dataset by oversampling the minority class (in this case, the "Charged Off" loans) to create a balanced dataset. The RandomOverSampler module from the imbalanced-learn library was used to oversample the training data.

## Results

Logistic Regression Model (Before Resampling):

• Balanced Accuracy Score: 0.952
• Precision Scores:
  • Healthy loans: 1.00
  • High-Risk loans: 0.85
• Recall Scores:
  • Healthy loans: 0.99
  • High-Risk loans: 0.91 
  
Logistic Regression Model (After Resampling):

• Balanced Accuracy Score: 0.994
• Precision Scores:
  • Healthy loans: 1.00
  • High-Risk loans: 0.84
• Recall Scores:
  • Healthy loans: 0.99
  • High-Risk loans: 0.99 

## Summary

In this analysis, we built and evaluated two logistic regression models to predict whether a loan will be healthy or high-risk. The first model was trained on the original dataset without any resampling, while the second model was trained on a resampled dataset using the RandomOverSampler method.

The balanced accuracy score for the first model was 0.952, which indicates that it correctly predicted the loan status for 95.2% of the test data. The balanced accuracy score for the second model was 0.993, indicating that it performed significantly better than the first model.

Precision and recall scores for both classes also improved in the resampled model. This suggests that the resampled model is likely to be more effective than the original model in predicting loan defaults.

Based on these results, I would recommend using the resampled model for predicting loan defaults. This is because it achieved a much higher balanced accuracy score, suggesting that it is better at correctly identifying loan defaults. While the first model performed well, it may not be as effective in identifying loan defaults, which is likely the more important class for lenders to predict accurately.

Overall, the performance of these models may depend on the problem we are trying to solve. In this case, accurately predicting loan defaults is likely to be more important than accurately predicting fully paid loans, as lenders need to manage their risks appropriately.
