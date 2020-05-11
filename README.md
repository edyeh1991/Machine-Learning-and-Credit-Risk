# Machine-Learning-and-Credit-Risk
# Overview
Machine learning is the use of statistical algorithms to perform tasks such as learning from data patterns and making predictions. There are many different models. In this challenge, you’ll build and evaluate several machine learning models to assess credit risk, using data from LendingClub; a peer-to-peer lending services company.

# Goals
The goals of this challenge are for you to:

Implement machine learning models.
Use resampling to attempt to address class imbalance.
Evaluate the performance of machine learning models.

# Summary and Analysis
Naive Random Oversampling
___________________________________________________________________________________
                   pre       rec       spe        f1       geo       iba       sup
  high_risk       0.01      0.74      0.58      0.02      0.66      0.44       101
   low_risk       1.00      0.58      0.74      0.73      0.66      0.42     17104

avg / total       0.99      0.58      0.74      0.73      0.66      0.42     17205
___________________________________________________________________________________

With the Naive random oversampling method, we get a balanced accuracy score of 66%. 
From out imbalanced classification report we calculate the precision for the high risk to be about 1% and the low risk to be 100%.
This value tells us that this model predicts a large amount of false positives high risk than there are actually in contrast to incorrectly predicting low risk individuals.

As for the recall score, the score of our high risk individuals are 74% as opposed to 58% for our low risk individuals.
This model predicts the high risk individuals with less false negatives than the prediction for the low_risk.

SMOTE Oversampling      
 ___________________________________________________________________________________     
                  pre       rec       spe        f1       geo       iba       sup
  high_risk       0.01      0.62      0.68      0.02      0.65      0.42       101
   low_risk       1.00      0.68      0.62      0.81      0.65      0.43     17104

avg / total       0.99      0.68      0.62      0.81      0.65      0.43     17205
___________________________________________________________________________________

Our balanced accuracy score for the SMOTE oversampling method is 65%.
From out imbalanced classification report we calculate the precision for the high risk to be about 1% and the low risk to be 100%.
This value tells us that this model predicts a large amount of false positives high risk than there are actually in contrast to incorrectly predicting low risk individuals.

As for the recall score, the score of our high risk individuals are 68% as opposed to 62% for our low risk individuals.
This model predicts the high risk individuals with less false negatives than the prediction for the low_risk.
Although the sensitivity decreased in detecting high risk individuals compared to the naive random oversampling method, this model does better at decreasing the amount of false negative predictions.

Undersampling    
 ___________________________________________________________________________________     
                  pre       rec       spe        f1       geo       iba       sup
  high_risk       0.01      0.66      0.40      0.01      0.52      0.27       101
   low_risk       1.00      0.40      0.66      0.57      0.52      0.26     17104

avg / total       0.99      0.40      0.66      0.57      0.52      0.26     17205

___________________________________________________________________________________

Our balanced accuracy score for the undersampling method is 53%.
From out imbalanced classification report we calculate the precision for the high risk to be about 1% and the low risk to be 100%.
This value tells us that this model predicts a large amount of false positives high risk than there are actually in contrast to incorrectly predicting low risk individuals.

As for the recall score, the score of our high risk individuals are 66% as opposed to 40% for our low risk individuals.
This model predicts the high risk individuals with less false negatives than the prediction for the low_risk.
This model is the worst of the three.

Combination (over and under) sampling  
 ___________________________________________________________________________________     
                  pre       rec       spe        f1       geo       iba       sup
  high_risk       0.01      0.72      0.57      0.02      0.64      0.42       101
   low_risk       1.00      0.57      0.72      0.72      0.64      0.40     17104

avg / total       0.99      0.57      0.72      0.72      0.64      0.40     17205

___________________________________________________________________________________

Our balanced accuracy score for the undersampling method is 64%.
From out imbalanced classification report we calculate the precision for the high risk to be about 1% and the low risk to be 100%.
This value tells us that this model predicts a large amount of false positives high risk than there are actually in contrast to incorrectly predicting low risk individuals.

As for the recall score, the score of our high risk individuals are 72% as opposed to 57% for our low risk individuals.
This model predicts the high risk individuals with less false negatives than the prediction for the low_risk.
This model performs similarly to the naive random oversampling method.


Out of the 4 models we see that the naive random oversampling method does the best with a balanced accuracy score of 66%.
Althought the model predicts a large amount of false positives high risk than there are actually, it is always better to over predict high risk individuals in order to keep the company safe. This model has the added bonus of predicting the high risk individuals with less false negatives than the prediction for the low_risk.


