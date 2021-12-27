# Credit Risk Challenge
 Module 17: Supervised Machine Learning and Credit Risk

## Resources Utilized

- Lending Club: LoanStats_2019Q1.csv
- Jupyter Notebook
- Python 3.7 MLENV
- Additional Software: imbalanced-learn, skikit-learn

## Overview
 
This new challenge consists of three technical analysis deliverables and a written report:

- Deliverable 1: Use Resampling Models to Predict Credit Risk
- Deliverable 2: Use the SMOTEENN Algorithm to Predict Credit Risk
- Deliverable 3: Use Ensemble Classifiers to Predict Credit Risk
- Deliverable 4: A Written Report on the Credit Risk Analysis

## Purpose

- The project had the purpose of investigating credit card risk using supervised machine learning. Most companies that offer lending services such as loans and credit cards must get a feel for the high-risk individuals who are being lent money. The main issue with using machine learning is the imbalance of high and low risk in the dataset. Since it is easier to find low risk than high risk in the dataset.

## Results & Analysis

- To help with the investigation and prediction, a variety of ML models are utilized with differing techniques and accuracy to predict the credit card risk. The machine learning models that were applied in this investigation are outlined:

1. Naive Random Oversampling

![Naive Random Oversampling](https://user-images.githubusercontent.com/88692025/147434655-fff729ec-c18d-4cea-96cd-ec0e2b45b1bc.png)

- The model is decently accurate; it can predict two thirds of the credit risk accurately. From the F-scores we can determine that the Random Oversampling model achieved an average F1 if 0,75 for low risk and an average of 0.02 for high risk, which is not ideal.

2. SMOTE Oversampling

![SMOT Oversampling](https://user-images.githubusercontent.com/88692025/147434827-27a2b7c6-1b3b-4107-b782-c955e074053b.PNG)

- The SMOT Oversampling model proves to be slightly less accurate than the naive random oversampling model, only by 1 percent at 65% accuracy, as for the F-scores, the model's F1 score has a higher average for low-risk credit at 0.82 and the same high-risk credit F1 score for high risk of 0.02 as the first model.

3. Cluster Centroids Undersample

![Cluster Undersample](https://user-images.githubusercontent.com/88692025/147435164-709dde0c-51b3-4bd1-b886-93d832197a7b.PNG)

- The first two models were utilizing the oversampling techniques; this model uses under sampling. The accuracy of the model is considerably lower than the first two oversampling models used. Sitting at 54% accuracy of predicting credit risk, this is not ideal because it is only slightly more accurate than a 50/50 random variable test such as a coin toss. The F-scores of this model are also lower sitting at 0.57 F-1 score for low risk and at an exceptionally low 0.01 for high risk.

4. SMOTEENN Algorithm

![Under Over Combination](https://user-images.githubusercontent.com/88692025/147435535-40fb4249-6217-4956-a7a0-90344b19f447.PNG)

- This algorithm uses a combination of oversampling AND UNDERSAMPLING TO PREDICT THE GAP IN THE underrepresented variable in the dataset. The accuracy of the model is substantially better than the single under sampling technique but falls narrowly short of the first two oversampling techniques at 64%, it is only 1 or 2 percent worse overall. The F-scores for this model are comparable to the oversampling only models, with 0.72 for low risk and 0.02 for high risk.

5. Balanced Random Forest Classifier

![Balanced ForrestPNG](https://user-images.githubusercontent.com/88692025/147435651-026f4169-1492-4206-b9c9-b4d1186aeb10.PNG)

- The following classifier had an extraordinarily strong result of 79% prediction accuracy, this is the second best result out of all the models and provides a strong prediction of credit risk to any firm. The F-scores reflect that with a 0.93 F1 score for low risk and a much-improved high risk F1 score of 0.06, which is line with the objective of finding the more machine learning elusive high-risk credit.

6. Easy Ensemble Classifier

![Easy Ensemble Classifier](https://user-images.githubusercontent.com/88692025/147435820-997b4b2b-38e1-429a-9189-71a6b5417d50.PNG)

- The easy ensemble classifier provided the most accurate model in the entire technique lot, with a very impressive 93% predictive power. The F-scores are also very improved due to the boost this model had, low risk at 0.97 F1 score and high risk which is at 0.16. This is still low overall but performs the best from what we have utilized so far. 

## Summary & Recommendation

- The overall conclusion is that the Easy Ensemble Classifier model had the best results with an accuracy of 93% and 16% precision or F1 score when predicting the high-risk credit candidates. And an impressive 97% when screening for low-risk credit candidates. We also observed that the models with oversampling were more accurate overall than the models with under sampling or a combination. And this was reflected in the F-scores as well.

- Final Recommendation: It is evident that the Easy Ensemble Classifier yielded the most accurate prediction results, the primary objective is to find the high-risk credit candidates, and none of the models were accurate enough, even the Ensemble, in determining the high-risk candidates. Which is why I must go with no recommendation, since even the best model had a predictive percentage of 16% for high-risk credit candidates. This is not good enough for financial institutions as they will end up taking risky clients and turning away a lot of business in the process. Such an elevated risk is not something that lending institutions would be comfortable undertaking, both in cliental and machine learning.
