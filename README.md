# Handling-Imbalanced-Dataset-Case-Study
One of the largest auto insurance company is facing problem of inaccuracies in car insurance claim predictions. This eventually leads them to raise the cost of insurance of good drivers and reduce it for bad drivers. The company wants you to  Build a model that predicts the probability that a driver will file an insurance claim in coming year

The dataset has close to 600K observations with 59 columns. This include "id" and "target" column. Therefore 57 features (inputs). Data is annonymized in order to protect the company's trade secrets, but some information about the nature of each varaible. Each row corresponds to a policy holder, and the target columns signifies that a claim was filed.

Values of -1 indicate that the feature was missing from the observation.
Target column signifies whether or not a claim was filed for that policy holder.
Ind is related to individual or driver
Reg is related to region
Car is related to car itself
Calc is a calculated feature
Feature names include the postfix bin to indicate binary features and cat to indicate categorical features.
Features without these designations are either continuous or ordinal

We can handle imbalanced classes by balancing the classes by increasing minority or decreasing majority.
We can do that by following few techniques
1. Random Under-Sampling
2. Random Over-Sampling
3. SMOTE - Synthetic Minority Oversampling Technique
4. ADASYN - Adaptive Synthetic Sampling Method
5. SMOTETomek - Over-sampling followed by under-sampling

In this problem we will use recall as evaluation metric because we would like to capture the performace where we will be rightly predicting positive classes.

Random Forest Classifier with SMOTE+TOMEK model has been finalized and got the below output:
Accuracy:  0.9630216617011268
F1 score:  0.0018140589569160996
Recall:  0.0009219422249539029
Precision:  0.056074766355140186

 clasification report:
               precision    recall  f1-score   support

           0       0.96      1.00      0.98    172056
           1       0.06      0.00      0.00      6508

    accuracy                           0.96    178564
   macro avg       0.51      0.50      0.49    178564
weighted avg       0.93      0.96      0.95    178564


 confussion matrix:
 [[171955    101]
 [  6502      6]]
