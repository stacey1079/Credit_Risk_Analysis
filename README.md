# Credit_Risk_Analysis

## Overview of the Analysis
The purpose of this analysis was to use different techniques to train and and evaluate models to assess credit risk.  Credit card risk is an unbalanced classification problem because good loans largely outnumber risky loans.  For this analysis, imbalanced-learn and scikit-learn libraries were used to build and evaluate Logistic Regression models using resampling.  A credit card dataset from LendingClub was used to build these Supervised Machine Learning Models.  The data was oversampled using RandomOverSampler and SMOTE algorithms.  The data was undersampled using the ClusterCentroids algorithm.  The last algorithm used was the SMOTEEN algorithm which is a combination of over and undersampling the data.  In the last Deliverable I compared the new machine learning models with BalancedRandomForestClassifier and EasyEnsembleClassifier to determine whether they should be used to determine credit risk. 


## Results Deliverable 1

![Screenshot 2023-03-29 224023](https://user-images.githubusercontent.com/45715246/228714298-3a2fe463-64a2-4dac-8573-10a7faf9455e.png)

### Random Oversampling Model:
![Mod18_Oversampling](https://user-images.githubusercontent.com/45715246/228252329-a1afa9e1-edfd-4fc2-b69a-17b25675420e.png)
* The balanced accuracy rate of this model was 64%.
* The high-risk precision score was only 1% with the recall being 62%.  This in turn gave the model an F1 score of 2%.
* The low-risk precision rate was 100% with the recall at 65%.

### SMOTE Oversampling Model:
![Mod18_SMOTE](https://user-images.githubusercontent.com/45715246/228252437-efb1b7f4-2036-407b-85fb-c749f0bb8f29.png)
* The balanced accuracy score of this model was also 64%.
* The high-risk precision rate was 1% with the recall being 63%.  This gave this model an F1 score of also 2%.
* The low-risk precision rate was 100% with a higher recall at 66%.

### Undersampling With ClusterCentroids:
![Mod18_Undersampling_1](https://user-images.githubusercontent.com/45715246/228252762-8136df73-daab-42e0-994b-7d77717dd176.png)
![Mod18_Undersampling_2](https://user-images.githubusercontent.com/45715246/228252811-1655e021-7ef1-45e7-a82c-4be882e224aa.png)
* The balanced accuracy score of this model was also 64%.
* The high-risk precision rate was again 1% with the recall being 62%.  This gave this model a lower F1 score of 1%.
* The low-risk precision rate was 100% with the recall at only 44%.

### Combined Oversampling And Undersampling With SMOTEEN 
![Mod18_Smoteen_1](https://user-images.githubusercontent.com/45715246/228255266-57abf434-60c6-4f31-aba0-b776658feb40.png)
![Mod18_Smoteen_2](https://user-images.githubusercontent.com/45715246/228255343-e4a17996-e551-4b30-83bf-012e188312dc.png)
* The balanced accuracy score of this model was 65%.  Which is the best accuracy score of all models so far.
* The high-risk precision rate was 1% with the recall being 74%.  This gave this model an F1 score of also 2%.
* The low-risk precision rate was 100% with the recall at 57%.


## Results Deliverable 2

### Balanced Random Forest Classifier
![Screenshot 2023-03-28 093916](https://user-images.githubusercontent.com/45715246/228256139-c457e2c5-6519-4d8b-b0be-680d7ad80d05.png)
* The balanced accuracy score of this model went up to 68%.
* The high-risk precision rate was a high 90% with the recall being 37%.  This gave this model a high F1 score of 52%.
* The low-risk precision rate was again 100% with the recall of also 100%!

### Easy Ensemble AdaBoost Classifier
![Mod18AdaBoost](https://user-images.githubusercontent.com/45715246/228256326-762b9927-4bd5-412a-8e0f-6c91376ea0db.png)
* This model had the largest balanced accuracy score of 93%!
* The high-risk precision rate was 9% with the recall being 92%.  This resulted in a higher F1 score of 16%.
* The low-risk precision rate was again 100% with the recall being 94%!


## Summary

I think it is very clear that the model I would trust most for precision accuracy is the combination EasyEnsembleAdaBoostClassifier.

