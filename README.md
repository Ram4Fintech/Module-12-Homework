# Module-12-Homework
## Credit Risk Classification:
The Credit Risk Annalysis Report has fully explained the purpose, the method and the various models used and their results in a detailed manner
This READ ME file only is a summary of the same
# Purpose:
In order to eliminate the bias caused by the overwhelming prseence of good loans in the entire population, this assignment creates a resampling dataset and using the same Logistic Regression model, prdicts a slightly different outcome as copmpared to the same model using the original dataset.
# The method used:
1) Splitting the data into training and testing sets: Firstly the data was read from csv file and converted into a dataframe. After cleaning the data for features(X) and targets(y), the data was split into training and testing datasets by using the train_test_split function;
2) Logistic Regression Model with original data: The Logistic Regression model was fitted with the training sets for X and y. Predict function was employed on the X_test and the resuly saved in a separate variable
3) The above model was then evaluated for accuracy score, confusion matrix and using classification report and the results were summarised
4) Logistic Regression with resampled data: Using the RandomOverSampler from the imbalanced library, the data was resampled. then the same Logistic Regression model was fitted with this resamopled data and predictiosn were made similar to the above
5) Repeating the same process as above the predictions were evaluated for its accuracy score, confsuion matrix and using classification report and the results were summarised
6) A comparison of the effectiveness of the two methods was done