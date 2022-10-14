# Credit_Risk_Analysis

## Overview

With a variety of resampling methods available, this credit risk analysis thoroughly explores a number of resampling techniques for modeling in search of the most ideal match for this particular Loan dataset. The goal is to find the greatest accuracy score and the healthiest imbalanced classification report. After using pandas get_dummies function to convert string columns to binary, we train test split the data in preparation for the modeling process.

## Results

The Results of the sampling and modeling are as follows:

* RandomOverSampler
  * A balanced accuracy score of approximately 61%
  * A precision score of 1% for the high_risk category and 100% for the low_risk category
  * A recall score of 58% for the high_risk category and 65% for the low_risk category 

* SMOTE 
  * A balanced accuracy score of approximately 62%
  * A precision score of 1% for the high_risk category and 100% for the low_risk category
  * A recall score of 59% for the high_risk category and 66% for the low_risk category 

* ClusterCentroids
  * A balanced accuracy score of approximately 51%
  * A precision score of 1% for the high_risk category and 99% for the low_risk category
  * A recall score of 59% for the high_risk category and 42% for the low_risk category 
 
* SMOTEENN
  * A balanced accuracy score of approximately 64%
  * A precision score of 1% for the high_risk category and 100% for the low_risk category
  * A recall score of 70% for the high_risk category and 58% for the low_risk category 
 
* BalancedRandomForestClassifier
  * A balanced accuracy score of approximately 78%
  * A precision score of 3% for the high_risk category and 100% for the low_risk category
  * A recall score of 65% for the high_risk category and 90% for the low_risk category 
 
* EasyEnsembleClassifier
  * A balanced accuracy score of approximately 94%
  * A precision score of 3% for the high_risk category and 100% for the low_risk category
  * A recall score of 65% for the high_risk category and 90% for the low_risk category 
 
 
## Summary

With precision being the predicted yes or the predictions of true positive over false positive and recall being the score for the actual yes or the true positive over false negative, one might find higher value in recall as it is more relavant to the larger scope of the data. With such low precision for the discovery of what we find truly relevant being the observations of high risk, sensitivity would seem the better metric. Our EasyEnsembleClassifier presents an incredible accuracy score of 94% and a recall score of 65% for high risk and 90% percent for low risk. The recommended sampling model for this dataset is the EasyEnsembleClassifier.
