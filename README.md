# Credit_Risk_Analysis

## Overview
The purpose of this analysis is to determine which machine learning model is best suited to predict credit risk. The Machine Models we have evaluated are: Random Oversampling, SMOTE Oversampling, ClusterCentroids Undersampling, SMOTEENN Sampling, BalancedRandomForestClassifier, and EasyEnsembleClassifier.

## Balanced Accuracy Scores:
![balanced](https://user-images.githubusercontent.com/91210001/151275844-1f7bd6b5-fb91-4ba5-ab5a-c657d57d8194.PNG)

### SMOTE Oversampling
![smote](https://user-images.githubusercontent.com/91210001/151275866-93e0db42-db98-4a93-81c8-403ac3112c6e.PNG)

### ClusterCentroids Undersampling
![clusterCentroids](https://user-images.githubusercontent.com/91210001/151275884-1c6ec928-126a-465a-baa6-8bc613b646ff.PNG)

### SMOTEENN Balanced Accuracy
![smoteeennn](https://user-images.githubusercontent.com/91210001/151275897-95fe87f5-74c2-4fee-84a8-24632ec46263.PNG)

### Balanced Random
![BalancedRandom](https://user-images.githubusercontent.com/91210001/151275910-2d281cba-a788-4cd3-8848-9e15ffca616f.PNG)

### Easy Ensemble AdaBoost Classifier 
![easy](https://user-images.githubusercontent.com/91210001/151275932-40e7b7bf-de3a-4185-8ae2-37a50156166d.PNG)

## Precision and Recall (Sensitivity) Scores:

### Naive Random Oversampling Imbalanced Classification Report
![Preceision](https://user-images.githubusercontent.com/91210001/151277195-9644d279-4111-4237-8384-574f3d913e37.PNG)

### SMOTE Imbalanced Classification Report
![smote](https://user-images.githubusercontent.com/91210001/151277205-0ccfe061-2d81-4f67-9409-a370996bc3e9.PNG)

### ClusterCentroids Undersampling Imbalanced Classification Report
![cluster](https://user-images.githubusercontent.com/91210001/151277218-ca586f3f-32b2-44f2-aa99-0883566fabae.PNG)

### SMOTEENN Imbalanced Classification Report
![smoteeeenn](https://user-images.githubusercontent.com/91210001/151277235-37f0ae86-280c-4e13-ad2a-a2aa422a5ac8.PNG)

### BalancedRandomForestClassifier Imbalanced Classification Report
![Balanced Random](https://user-images.githubusercontent.com/91210001/151277239-d34776f8-82cd-419f-843e-05787dd0b86d.PNG)

### EasyEnsembleClassifier Imbalanced Classification Report
![easy](https://user-images.githubusercontent.com/91210001/151277247-d571f072-2023-4c5a-b0e6-0a54f6b91dba.PNG)

## Summary

Six models were used, listed ranked in order of accuracy score:
  * EasyEnsembleClassifier - 93#
  * BalancedRandomForestClassifier- 78%
  * SMOTE- 66%
  * SMOTEENN- 64%
  * NAive- 64%
  * ClusterCentroids- 54%
  * 
Based on the Imbalanced Classification Reports of each model, it appears that every model is able to predict with 100% accuracy applications with low credit risk as the Precision score for the low risk category are all at 100%. That is relatively unimportant though as what is more important during a credit approval process is the ability to identify high risk applications as accurately as possible to avoid potential defaults.

With that in mind, our focus will switch to the high risk category.

Precision Scores:
All models have less than 10% Precision scores which means that there are lots of false positives i.e. applications that are not high risk but identified as high risk. That is bad for business as that would result in many unnecessary rejections.

Recall Scores:
The EasyEnsembleClassifier has the highest Recall score for the high risk category of 92%. All other models have scores of around 70%.

I would not recommend the EasyEnsembleClassifier even though it is the best model that we tested.  The F1 score is too low for the model to be used with accuracy out in the wild.
