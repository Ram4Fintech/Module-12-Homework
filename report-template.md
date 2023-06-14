# Module 12 Report Template

## Overview of the Analysis

# The purpose of this analysis: 
The purpose of this Credit Risk Analysis Report is to compare the two machine learning models used in the homework, one using Logistic Regression with the original data and the other one using the same with resampled training data

# The initial data 
This was in the form of a csv file and this data contained the details of the loan for each customer - loan amount, interest rate, customer income, loan to income ratio etc. it also had markers to indicate whetgher the loan conduct was good or bad. Using the confusion matrix, this data was used to predict and compare the actual good conduct(0) loan s and the bad conduct (1) loans respectively against the predicted good conduct(0) loans and the predicted bad conduct (1) loans

# The different variables that I was trying to predict:
i) Value counts: This gives a break up of the total number of customers that were analysed and give a break up of those with good conduct loans (0) and those with bad conduct loans(1);
ii) Balanced accuracy score: Using the balanvced_accuracy_score function, the accuracy score of this model was calculated which turned out to be over 95%;
iii) Confusion matyrix: tHis method was used to predicted the comparsion of the preicted and actual counts for good and bad loans; and
iv) Classification report: This report predicts the accuracy, precision, recall and other paramters for this model

# The steps of this machine learning process are:
- Reading the csv file into a pandas dataframe;
- Removing the target ('loan_status') from X avariable and relabelling it as a y variable as per requirement;
- Splitting the data intro training and testing data sets;
- Fitting the Logistics Regression model or the Resampling model by using the X-train and y-train datasets;
- making predictions using the testing datasets;and 
- Evaluating the model's performance using the accuracy score, confusion matrix and the classification report.

# The two methods used above are: LogisticsRegression model with original data and the LogisticsRegression model with resampled data
1) LR model with original data: This does the preprocessing, training, validation and prediction using the original data in the csv file;
2) LR model with resampled data: this does the same above mentioned steps with an oversized sample so that the results are unbiased and more representative of the entire data


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

## Machine Learning Model 1:
  # Description of Model 1: Logistic Regression Model with the original data
  Accuracy, Precision, and Recall scores.
Classification Report
              precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.85      0.91      0.88       619

    accuracy                           0.99     19384
   macro avg       0.92      0.95      0.94     19384
weighted avg       0.99      0.99      0.99     19384

# Accuracy:
 Accuracy is a measure of how often the model is correct or the ratio of correctly predicted observations to the total number of observations. At 0.99 as above, this implies that the model is correct 99% of times
# Precision:
 Precision is the ratio of correctly predicted positive observations to the total predicted positive observations. the target of 0 (good loans) has a precision of 1 which means that there are no false positives which means that there are no good loans that are not categorised as good loans. on the contrary, the target 1 (bad loans) has a precision of 0.85, which means that there are 15% of loans that are not categorised as bad loans, but are not bad loans 
 # Recall:
 Recall is the ratio of correctly predicted positive observations to all predicted observations of that class. This means that of all the actual good loans 99% were actually good loans and conversely of all the bad loans 91% were actually bad loans. This means that 9% of the total bad loans were wrongly classified as bad loans

## Machine Learning Model 2:
  # Description of Model: Logistic Regression Model with the resampled data
   Accuracy, Precision, and Recall scores:
            precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.84      0.99      0.91       619

    accuracy                           0.99     19384
   macro avg       0.92      0.99      0.95     19384
weighted avg       0.99      0.99      0.99     19384
# Accuracy:
 Accuracy is a measure of how often the model is correct or the ratio of correctly predicted observations to the total number of observations. At 0.99 as above, this implies that the model is correct 99% of times. This is the same as the previous model
 # Precision:
 Precision is the ratio of correctly predicted positive observations to the total predicted positive observations. the target of 0 (good loans) has a precision of 1 which means that there are no false positives which means that there are no good loans that are not categorised as good loans. on the contrary, the target 1 (bad loans) has a precision of 0.84, which means that there are 16% of loans that are not categorised as bad loans, but are not bad loans. This is slightly worse than the previous model
 # Recall:
 Recall is the ratio of correctly predicted positive observations to all predicted observations of that class. This means that of all the actual good loans 99% were actually good loans and conversely of all the bad loans 99% were actually bad loans. This means that only 1% of the total good loans were actually bad loans and similarly only 1% of the bad loans were actually bad loans

## Summary
Both models have broadly returned the same kind of results. However of the two, the model with the resampled data set appears to be more reliable and accurate because:
  i) The balanced accuracy score is higher at 99.4% as comnpared to the other model which is returning a score of 95.2%;
  ii) Though the precision for target 1 which is bad loans is lower by 1%, the trecall rate for the same category is higher by 8% compared to the model with original dataset; and
  iii) the macro avg for this model is higher than that of the previous one