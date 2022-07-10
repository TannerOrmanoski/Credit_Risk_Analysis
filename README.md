# Credit_Risk_Analysis

## Purpose

The purpose of this analysis is to use multiple techniques to train and evaluate models with unbalanced classes using out credit card database. We will use imbalanced-learn and scikit-learn libraries to build and evaluate our credit-risk models using resampling.  

## Results

•	Naïve Random Sampling

![](https://github.com/TannerOrmanoski/Credit_Risk_Analysis/blob/main/Module-17-Challenge-Resources/Photos/Screen%20Shot%202022-07-08%20at%207.12.58%20PM.png)

With naïve random oversampling, our accuracy is only 0.64, which is not ideal. The precision score is low for high_risk and a perfect for low_risk, the recall score is similar for high_risk and low_risk at 0.61 and 0.69.

•	SMOTE Oversampling

![](https://github.com/TannerOrmanoski/Credit_Risk_Analysis/blob/main/Module-17-Challenge-Resources/Photos/Screen%20Shot%202022-07-08%20at%207.14.03%20PM.png)

With SMOTE the precison is once again a perfect fit for low_risk and a 0.01 for high_risk. The recall is 0.59 for high_risk and 0.65 for low_risk.

•	Random Under Sampling

![](https://github.com/TannerOrmanoski/Credit_Risk_Analysis/blob/main/Module-17-Challenge-Resources/Photos/Screen%20Shot%202022-07-08%20at%207.14.27%20PM.png)

Using random undersampling we achieve a 0.59 accuracy score, which is not a great fit. Precision in this algorithm is identical to the previous algorithms. The recall is 0.61 for high_risk and 0.57 for low_risk.

•	SMOTEENN

![](https://github.com/TannerOrmanoski/Credit_Risk_Analysis/blob/main/Module-17-Challenge-Resources/Photos/Screen%20Shot%202022-07-08%20at%207.14.43%20PM.png)

SMOTEEN resampling gives us a rather low accuracy score of 0.64. The precision is again 0.01 for high_risk and 1.00 for low_risk. The recall is 0.7 for high_risk and 0.58 for low_risk.

•	Balanced Random Forrest Classifier

![](https://github.com/TannerOrmanoski/Credit_Risk_Analysis/blob/main/Module-17-Challenge-Resources/Photos/Screen%20Shot%202022-07-08%20at%207.15.29%20PM.png)

The accuracy of the Balanced Random Forest Classifier algorithm is 0.79. The high_risk precision is a perfect 1.0 and low_risk is 0.04. The high_risk recall is 0.67, while the low_risk recall is 0.91.

•	Easy Ensemble AdaBoost Classifier

![](https://github.com/TannerOrmanoski/Credit_Risk_Analysis/blob/main/Module-17-Challenge-Resources/Photos/Screen%20Shot%202022-07-08%20at%207.15.43%20PM.png)

The easy ensemble adaboost classifier returns an accuracy score of 0.91. The low_risk has a precision score of 0.07 and a recall score of 0.9. The high_risk is a precision score of 1.0 and a recall score of 0.94. 

## Summary 

The most accurate techniques for training and evaluating our model are the balanced random forest classifier and easy ensemble adaboost classifier models. They both achieve a high accuracy score, while the other models do not breach 0.7. We next look at precision and recall. There is a trade of between these two measurements. Precision allows us to be sure that what we are saying is a positive is a positive, but we might miss out on some positive values in this pursuit. With recall we can make sure we are not missing out on positive observations, but we might have more false positives. For the most part these models seem to do quite well with precision, while being quite average with recall. The precision score suffers for high_risk in the first four models and suffers for low_risk in the last two models. Having a high recall score is preferable in this case, because we want to catch all the possible high_risk credit instances. With this being said the easy ensemble adaboost classifier model should be recommended
