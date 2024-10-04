# Credit Risk Analysis

## Overview of purpose of the analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

The purpose of this analysis is to determine the creditworthiness of borrowers to protect lenders from losses when providing loans to borrowers who are likely to default on their loans. 75% of historical lending data was used to train a supervised machine learning Logistic Regression Model(LRM) to reliably classify a loan as healthy or high-risk where the other 25% was used to test the performance of the model. LRM is an appropriare model to use to classify the binary categories as either healthy or high-risk. The metrics to determine the performance of the model is described below. 

## Performance Metrics of Logistic Regression Model

 - **Accuracy:** The overall accuracy of the model was strong, reliably predicting the healthy and high-risk loans 99% of the time.
 - **Precision:**
    - ***Healthy loans: The model predicted the healthy loans very well, in fact, it predicted 100% of them with regard to the precision score. There were no false positives for healthy loans. 
    - ***High-risk loans: It also predicted the high risk loans to a high degree. This is evidenced by the precision value of 0.87 which is a measure of the false positives where 87% of predicted high risk loans were correctly predicted as high-risk loans but 13% were misclassified as high-risk when they were actually healthy.
 - **Recall:
    - ***Healthy loans: The model predicted the healthy loans very well, in fact, it predicted 100% of them with regard to the recall score. There were no false negatives for healthy loans. 
    - ***High-risk loans: The recall value of 0.89 which is a measure of the false negatives where 89% of actual high risk loans were correctly predicted as high risk loans but 11% were misclassified as healthy when they were actually high risk.

## Summary of results

Overall, the performance of the model is very strong. Of all 18,759 healthy loans only 80 were incorrectly predicted to be high risk. Of the 625 high-risk loans only 67 were incorrectly predicted to be healthy. The imbalance of the support for healthy loans has swayed the accuracy score to 99%.

Incorrectly predicting 80 of the healthy loans as high risk presents a lost revenue opportunity to the lender to supply a loan to a customer who was actually a healthy borrower. This is the measure of the precision score and 80 false positives.

The real risk of losses to both the lender and borrower though are attributed to the possibility of irresponsibly lending to 67 of the high-risk borrowers who were incorrectly predicted as healthy borrowers. The proportion of the 67 false negatives to the overall high risk loans is a significant number (>10%). A responsible lender would fine-tune the model further to increase the recall score to reduce the number high-risk borrowers who were predicted to be healthy borrowers. Adding additional features to the model to help identify the false negatives more closely can help to fine-tune the model's predictive performance.

To conlcude, the recall score in this scenario should be very carefully monitored. Imbalanced datasets such as this can provide misleading accuracy of the model. The high accuracy score is not as strong an indicator of reliable prediction as the recall and precision scores. The opportunity to fine-tune the model with additional features, or algorithms should be explored.
