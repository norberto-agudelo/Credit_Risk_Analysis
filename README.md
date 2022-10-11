# Module 17. Credit_Risk_Analysis. Supervised Machine Learning

## Overview 

The purpose of this challenge is to apply some skills and subjects related with big data learned during the week. By using the “credit card credit dataset from LendingClub, a peer-to-peer lending services company” we have to use some algoritms like RandomOverSampler and SMOT to predict loans risk.

Some techniques will be applied to to train and evaluate models with unbalanced classes. On loans business  good loans easily outnumber risky loans so it is necessary to create models to manage unbalanced data sets.

BalancedRandomForestClassifier and EasyEnsembleClassifier are going to be used to predict credit risk, too. Finally we have to evaluate the performance of these models and “make a written recommendation on whether they should be used to predict credit risk”.


## Results. Deliverables/Analysis

First I got a baseline of performance using logistic regression classifier to make predictions and evaluate the model’s performance.

The accuracy score of the model was 0.995 what it means that it has a good performance.

 ![image](https://user-images.githubusercontent.com/107591542/194986967-e97f2da1-b283-4df1-9bb9-538271ca4cab.png)


![image](https://user-images.githubusercontent.com/107591542/194986992-c31266c9-f463-475c-87c4-86ad4cd9259f.png)
 

The confusion matrix and the imbalanced classification report show that the model is not very good in predicting high risk, recall is 0.23 and F1  is 0.33. They show that there are a high amount of  false positive what is not acceptable for this kind of business.


### Deliverable 1. Use Resamplig Models to predict Credit Risk

#### After using Oversampling Models we got these results

The accuracy score of the model was 0.8324, less than the baseline performance. It means that OverSampling process didn’t improve the model accuracy

 ![image](https://user-images.githubusercontent.com/107591542/194987048-bf054f70-adbb-4c9c-b10e-71b6ecaec19a.png)

![image](https://user-images.githubusercontent.com/107591542/194987074-00d7bfe2-592a-46c6-8f28-f03099f59a9a.png)



The confusion matrix and the imbalanced classification report for this Oversampling Model don’t show a significant change. We can affirm that it is less efficient than the base line.  F1 is only 0.07 for high_risk less than 0.33 in the base line.

Even, recall is less than 1.0, the value in the base line. The oversampling process didn’t improve the base model.


#### After using SMOTE Oversampling Model we got these results

The accuracy score of the model was 0.8440, less than the baseline performance and the same than the previous model  (Oversampling). It doesn’t improve the accuracy of the model either.

 ![image](https://user-images.githubusercontent.com/107591542/194987192-d3fb80fe-7e25-4bcd-9a44-1c086c142506.png)

![image](https://user-images.githubusercontent.com/107591542/194987217-09af9a0b-0f27-4fc0-be1f-75dee0e7234d.png)


The confusion matrix and the imbalanced classification report for this SMOTE Oversampling Model don’t show a significant change either. We can affirm that that this model is almost the same than the previous one.

#### After using Undersampling Models (Cluster Centroids) we got these results

The accuracy score of the model was 0.8440, less than the baseline performance but a little better than Oversampling model. So, It improves the accuracy of the model only a little.

 ![image](https://user-images.githubusercontent.com/107591542/194987250-6293c8cb-1442-407d-8893-11ecfbec8102.png)

![image](https://user-images.githubusercontent.com/107591542/194987285-d75ff8b3-bf51-4a3d-85f0-bf28c17a56d5.png)

 
As previous models, this undersampling process doesn’t show any improvement. F1 shows the same values than Over Sampling model shows


### Deliverable 2. Use the SMOTEEN Algoritm  to predict Credit Risk

Using a combination (Over and Under) Sampling we got the same results than previous model. It means that using the SMOTEEN Algoritm didn’t improve our model

 ![image](https://user-images.githubusercontent.com/107591542/194987369-b02a1d79-3adf-455b-abf2-94584f17c96e.png)

![image](https://user-images.githubusercontent.com/107591542/194987384-b50a54ce-3464-4c04-920a-d297cea94668.png)


### Deliverable 3. Use the Ensemble Classifiers  to predict Credit Risk

By using the BalancedRandomForestClassifier we got this results

The accuracy score of the model was 0.759 less than any other model created before. It shows that this model didn’t  improve the prediction accuracy

 ![image](https://user-images.githubusercontent.com/107591542/194987451-204b5ead-5940-473e-b80c-44fadf063065.png)

![image](https://user-images.githubusercontent.com/107591542/194987473-6c900057-c7a6-4c61-8281-1c16e7c419fa.png)
 

The confusion matrix and the imbalanced classification report, for this ensemble model, show a F1 = 0.06 even lesser than F1 in other models.

Recall values are lesser than others, too. It means that this model isn’t good predicting low and high risk.

The chart above shows  the important features sorted in descending order

 ![image](https://user-images.githubusercontent.com/107591542/194987513-ca6b21f0-3ff5-472d-a5c9-118a83e6eb4e.png)


By using the Easy Ensemble AdaBoost Classifier we got this results

The balance accuracy score is (EasyEnsembleClassifier) is  0.9319. It is a good score compared with all other models but the base line.

 ![image](https://user-images.githubusercontent.com/107591542/194987549-79a3518b-62b6-4be9-b7ec-425dbc7be36a.png)

![image](https://user-images.githubusercontent.com/107591542/194987583-49c7b39d-d5a0-4609-b666-d1a4c9cf0ba4.png)
 

The confusion matrix and the imbalanced classification report for this EasyEnsemble Model dshow better  values than all the models created in previous processes.

F1 is only 0.16 not to high but it is a good value compared with them. Precision and recall show good values too

## Summary

It seem that the Easy Ensemble Classifier is the best model with a F1 value of 0.16 for high risk. This is not an excemt value for predicting high risk loans but it is the best of all others. I could affirm that the base line model is better than all models created in this project.

The resampling models didn’t generate good values. F1 was so low all the times and didn’t have good results predicting high risk.

I think that new processes including new data must be performed.

