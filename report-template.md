# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
Perform logistic regression and cross validation of data and resample data imbalanced classes.

* Explain what financial information the data was on, and what you needed to predict.
data was on loan risk features and whether the loan defaulted
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
the value count between non default and default was:
0    75036
1     2500
* Describe the stages of the machine learning process you went through as part of this analysis.
select the logistic regression model (model), calculate logit coefficients (fit), and predict 
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
train_test_split() used to parition data, LogisticRegression.fit() and LogisticRegression.predict() used to fit and predict.  accuracy_score() to measure trueness, RandomOverSampler() oversamples data with replacement 
## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.

-Precision of 0 was 1.00 which means There were no instances of false positive (wrongly predict default)
-Recall of 0 was .99 which means there were some loans that defaulted that were not predicted
-Precision of 1 was .85 which means the model falsely identified 15% as default when infact loans were good
-recall was .91 which means the model missed 9% of defaults
-accuracy of .99 means 99% of all the cases were accurately predicted.


              precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.85      0.91      0.88       619

    accuracy                           0.99     19384
   macro avg       0.92      0.95      0.94     19384
weighted avg       0.99      0.99      0.99     19384




* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
  
  
  -the Precision and Recall of the 0 group is unchanged from model 1
  -the Precision is decreased slightly to .84 in the 1 group, meaning there were some false Positives.
  -THe recall is significantly higher.  this is expected since overfitting would result in very high true positive rate.

  
  
                  pre       rec       spe        f1       geo       iba       sup

          0       1.00      0.99      0.99      1.00      0.99      0.99     18765
          1       0.84      0.99      0.99      0.91      0.99      0.99       619

avg / total       0.99      0.99      0.99      0.99      0.99      0.99     19384

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
Model 2 performs better.  It has higher accuracy with apparently limited overfitting issues.
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
Its more important to predict the 1's since defaults are more costly than turning down business due to overfitting of defaults.

If you do not recommend any of the models, please justify your reasoning.
