# Credit_Risk_Analysis
## Overview of the Analysis:
In this project, we use Python to build and evaluate several machine learning models to predict credit risk.
We adopted the following procedure:

1. oversample the data using the RandomOverSampler and SMOTE algorithms.
2. Undersample the data using the ClusterCentroids algorithm.
3. Use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm.
4. Compare two machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier.

## Results:
* Naive Random Oversampling results: Our balanced accuracy test it 64%, the precision for the high_risk has a very low positivity at 1% and the recall is 65%

![random](https://user-images.githubusercontent.com/90945875/149553422-dda6e93e-310e-48b8-b6c1-b4326375a4be.PNG)

* SMOTE oversampling results: the accuracy score is 63%, the precision for the high_risk loans has a low positvity  at about 1% and recall is 64% overall

![smote](https://user-images.githubusercontent.com/90945875/149554164-73070dc4-2d56-4ea2-bc36-7847fb75ae13.PNG)

* Undersampling results: balanced accuracy score is 50% overall, the precision for the high_risk loans has a low positvity  at about 1% and recall is 44% overall

![Undersampling](https://user-images.githubusercontent.com/90945875/149556028-16e375e5-740b-4d92-89e5-029ff74de17b.png)

* Combination(over and undersampling) results: balanced accuracy score is 62% ,the precision for the high_risk loans has a low positvity  at about 1% and recall is 54% overall

![Combination](https://user-images.githubusercontent.com/90945875/149556648-0bde28f6-e1dc-485a-9006-70fb86c931dc.png)

* Balanced Random Forest Classifier results: the accuracy score is 78% ,the precision for the high_risk loans has a low positvity  at about 1% and recall is 91% overall

![Balanced _Random](https://user-images.githubusercontent.com/90945875/149557376-a56bf25d-2e99-4ef8-81c1-2aa19a5464ef.png)

* Easy Ensemble AdaBoost Classifier results: the accuracy score is 93% ,the precision for the high_risk loans has a low positvity  at about 1% and recall is 94% overall

![Easy_Ensemble](https://user-images.githubusercontent.com/90945875/149557885-d6b30b5b-3280-4368-8b61-770e03c716f2.png)

## Summary:

All the models used to perform the credit risk analysis show weak precision in determining if a credit risk is high.
In the first four models we undersampled, oversampled and did a combination of both to try and determine which model is best at predicting which loans are the highest risk. The next two models we resampled the data using ensemble classifiers to try and predict which which loans are high or low risk. In our first four models our accuracy score is not as high as the ensemble classifiers and the recall in the oversampling/undersampling/mixed models is low as well. Typically in your models you want a good balance of recall and precision which is why I recommend the ensemble classifiers over the first four models. It appears that the Easy Ensemble had the best balance of all the models because of it's high accuracy score and good balance of precision and recall scores.



