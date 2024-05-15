# Credit Risk Analysis Report
---
**An Overview of the Analysis**: This analysis uses a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.
> - *Part 1: Split the data into training and testing datasets* - The analysis takes in as input historical lending data with the corresponding file being named as *lending_data.csv*
> - *Part 2: Create a Logisitical Regression Model with the Original Data* - A logistic regression model is created using the training data and its performance is evaluated using a *confusion matrix*.
> - The primary data element of interest in the original dataset is that of *loan status*. The following fields are analyzed to determine the loan status based on the original data - loan size, interest rate, borrower income, debt to income ratio, number of accounts, derogatory marks and total debt.
> - Based on the target values of `loan_status`, the analysis is used to predict two variables - `loan_status = 0` that indicates healthy loans and a `loan_status = 1` that indicates a high risk of default.
> - *Logistical Regression Model Steps*: As part of the analysis, the following steps were used for the logistical regression model on the lending data:
>>> **Step 1:** Fit a logistic regression model by using the training data.<br>
>>> **Step 2:** Save the predictions for the testing data labels by using the testing feature data and the fitted model.<br>
>>> **Step 3:** Evaluate the model’s performance by generating a confusion matrix and printing the related classification report to determine its accuracy scores.<br>
> - Finally, a brief overview of the results is provided based on the output of the regression model and its performance in the corresponding Jupyter Notebook source code file. 

**Results**: Based on the classification report of the underlying regression model, both the macro and weighted average of its accuracy scores are computed along with the precision and recall scores for each of healthy and high-default risk loan types based on the trained datasets of the original data. <br>
> - *Precision Scores*: This model has a precision score of 100% for the healthy loans and 87% for the high-risk loans. The precision scores imply that the healthy loans were classified correctly as positive 100% of the times. However, for the high-risk loans, the classification was correct only 87% of the times. This can perhaps be attributed to the imbalance and skewness in data where the vast majority of the datasets `75036 out of 77536` point to healthy loans.
> - *Recall Scores*: This model has a recall score of 100% for the healthy loans and 89% for the high-risk loans. The scores imply that for all the instances where the loans were actually healthy, they were classified correctly. However, for all the instances where the loans were actually high-risk, they were classified correctly only 89% of the times.

**Summary**: Based on the output of the regression model, the following can be inferred:
> 1) Precision measures the proportion of correctly predicted instances out of the total predicted instances for a specific label. For the *healthy loan* class, the precision is 1.00, indicating that the model predicts this label with perfect precision. For the *high-risk loan* class, the precision is 0.87, meaning that 87% of the predicted high-risk loans are correct.
> 2) Recall, also known as sensitivity or true positive rate, measures the proportion of correctly predicted instances out of the total actual instances for a specific label. The recall for the *healthy loan* class is 1.00, indicating that the model captures all the actual healthy loans. The recall for the *high-risk loan* class is 0.89, meaning that the model identifies 89% of the high-risk loans correctly.
> 3) The F1-score is the mean of precision and recall and provides a balanced measure of the model's performance. For the *healthy loan* class, the F1-score is 1.00, indicating perfect performance. The F1-score for the *high-risk loan* class is 0.88, representing a good balance between precision and recall for this label. Based on the above accuracy score of 99%, this model performs exceptionally well.<br>
---
