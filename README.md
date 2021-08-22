# Credit Risk Analysis
## Module 17: Introduction to Supervised Machine Learning
---

### Overview
In this module students were introduced to Supervised Machine Learning, a method by which statistical algorithms learn from training data sets and make predictions based on additional data.  For this exercise, we focused on creating a model which would be able to predict if a particular loan would be high or low risk based on many  parameters(features).  Upon analysis, we discovered that our dataset was quite unbalanced with over 68,470 out of the 68,817 loans considered low risk.  Consequently, we needed to sample our data in a variety of ways to determine which would create the best predictive model.  It will be important for our model to have high sensitivity to identify and avoid the high risk loans.   

### Results
---
### 1. Random Oversampling
This model chooses more of the high risk loans until the class samples are approximately the same size.

![diagram of oversampling](https://github.com/murphyk2021/Credit_Risk_Analysis/blob/9ce6a01ab776718b17e48c0fd2191de89fe3291d/Images/Oversampling_diagram.JPG)

**Low Risk:**  51,352

**High Risk:**  51,352

![classification report](https://github.com/murphyk2021/Credit_Risk_Analysis/blob/80ea56f10d38de7da4a13ba093575b5a0febea4f/Images/Oversampling.JPG)
 - **Accuracy:** 66%
 - **Identifying High Risk Loans:**
    - **Precision:** Of the loans predicted to be "High risk" 1% were, in fact, High Risk
    - **Recall/Sensitivity:** The model accurately predicted 66% of the loans that were High Risk as "High Risk"
    - **f1:** Very Low - There is a disparity between the precision and sensitivity

 - **Identifying Low Risk Loans:**
    - **Precision:** Of the loans predicted to be "low risk", 100% were, in fact, Low Risk
    - **Recall/Sensitivity:** The model accurately predicted 67% of the loans that were Low Risk as Low Risk
    - **f1:**  High - Precision and sensitivity are similar

---
### 2. Synthetic Minority Oversampling Technique (SMOTE)
This model creates synthetic high risk data based on similar data points in the dataset.

![diagram of SMOTE](https://github.com/murphyk2021/Credit_Risk_Analysis/blob/9ce6a01ab776718b17e48c0fd2191de89fe3291d/Images/SMOTE_Oversampling_Diagram.JPG)

**Low Risk:**  51,352

**High Risk:**  51,352

![Classication Report](https://github.com/murphyk2021/Credit_Risk_Analysis/blob/80ea56f10d38de7da4a13ba093575b5a0febea4f/Images/SMOTE_Oversampling.JPG)

 - **Accuracy:** 63%
 - **Identifying High Risk Loans:**
    - **Precision:** Of the loans predicted to be "High risk" 1% were, in fact, High Risk
    - **Recall/Sensitivity:** The model accuratelypredicted 62% of the loans that were High Risk as "High Risk"
    - **f1:** Very Low - There is a disparity between the precision and sensitivity

 - **Identifying Low Risk Loans:**
    - **Precision:** Of the loans predicted to be "low risk", 100% were, in fact, Low Risk
    - **Recall/Sensitivity:** The model accurately predicted 64% of the loans that were Low Risk as Low Risk
    - **f1:**  High - Precision and sensitivity are similar

---
### 3. Undersampling
This model decreased the size of the low risk loans such that the class samples are approximately the same size

![diagram of undersampling](https://github.com/murphyk2021/Credit_Risk_Analysis/blob/9ce6a01ab776718b17e48c0fd2191de89fe3291d/Images/Undersampling_diagram.JPG)

**Low Risk:**  260

**High Risk:**  260

![Classification Report](https://github.com/murphyk2021/Credit_Risk_Analysis/blob/711f7e030257672a186da5f13bfc3c5f9375a8e6/Images/Undersampling.JPG)

 - **Accuracy:** 51%
 - **Identifying High Risk Loans:**
   - **Precision:** Of the loans predicted to be "High risk" 1% were, in fact, High Risk
    - **Recall/Sensitivity:** The model accurately predicted 60% of the loans that were High Risk as "High Risk"
    - **f1:** Very Low - There is a disparity between the precision and sensitivity

 - **Identifying Low Risk Loans:**
    - **Precision:** Of the loans predicted to be "low risk", 100% were, in fact, Low Risk
    - **Recall/Sensitivity:** The model accurately predicted 43% of the loans that were Low Risk as Low Risk
    - **f1:**  High - Precision and sensitivity are similar
    
---   
### 4. SMOTE + Edited Nearest Neighbor (SMOTEENN) 
This model oversamples the high risk data and undersamples the the low risk data by dropping any data that are borderline.

![diagram of SMOTEENN](https://github.com/murphyk2021/Credit_Risk_Analysis/blob/9ce6a01ab776718b17e48c0fd2191de89fe3291d/Images/SMOTEENN_diagram.JPG)

**Low Risk:**  68,460

**High Risk:**  68,460

![Classification Report](https://github.com/murphyk2021/Credit_Risk_Analysis/blob/711f7e030257672a186da5f13bfc3c5f9375a8e6/Images/Combo_Sampling.JPG)

 - **Accuracy:** 64%
 - **Identifying High Risk Loans:**
   - **Precision:** Of the loans predicted to be "High risk" 1% were, in fact, High Risk
    - **Recall/Sensitivity:** The model accurately predicted 70% of the loans that were High Risk as "High Risk"
    - **f1:** Very Low - There is a disparity between the precision and sensitivity

 - **Identifying Low Risk Loans:**
    - **Precision:** Of the loans predicted to be "low risk", 100% were, in fact, Low Risk
    - **Recall/Sensitivity:** The model accurately predicted 57% of the loans that were Low Risk as Low Risk
    - **f1:**  High - Precision and sensitivity are similar
    
---
### 5. Balanced Random Forest
This model uses several decision trees which generate a simple model from a subset of the data which are then combined to make predictions

![diagram of random forest](https://github.com/murphyk2021/Credit_Risk_Analysis/blob/d00ae3952f922462d60a4f4f87e97fec126df9db/Images/Random_Forest_diagram.JPG)

![Random Forest Classification Report](https://github.com/murphyk2021/Credit_Risk_Analysis/blob/1d60616666887c10fdc9352ccf15c66f0b124e86/Images/Random_Forest_Report.JPG)

 - **Accuracy:** 79%
 - **Identifying High Risk Loans:**
   - **Precision:** Of the loans predicted to be "High risk" 4% were, in fact, High Risk
    - **Recall/Sensitivity:** The model accurately predicted 67% of the loans that were High Risk as "High Risk"
    - **f1:** Very Low - There is a disparity between the precision and sensitivity

 - **Identifying Low Risk Loans:**
    - **Precision:** Of the loans predicted to be "low risk", 100% were, in fact, Low Risk
    - **Recall/Sensitivity:** The model accurately predicted 91% of the loans that were Low Risk as Low Risk
    - **f1:**  High - Precision and sensitivity are very similar
---
### 6. Easy Ensemble AdaBoost
In this method models are trained based on the errors of other models. 
![AdaBoost Diagram](https://github.com/murphyk2021/Credit_Risk_Analysis/blob/4fa5e29f310c6fc5ad119ee066962634b07e7238/Images/AdaBoost_Diagram.JPG)

![AdaBoost Classification Report](https://github.com/murphyk2021/Credit_Risk_Analysis/blob/4fa5e29f310c6fc5ad119ee066962634b07e7238/Images/AdaBoost_Classification_Report.JPG)

 - **Accuracy:** 93%
 - **Identifying High Risk Loans:**
   - **Precision:** Of the loans predicted to be "High risk" 7% were, in fact, High Risk
    - **Recall/Sensitivity:** The model accurately predicted 91% of the loans that were High Risk as "High Risk"
    - **f1:** Very Low - There is a disparity between the precision and sensitivity

 - **Identifying Low Risk Loans:**
    - **Precision:** Of the loans predicted to be "low risk", 100% were, in fact, Low Risk
    - **Recall/Sensitivity:** The model accurately 

    - predicted 94% of the loans that were Low Risk as Low Risk
    - **f1:**  High - Precision and sensitivity are very similar
---

### Summary 
Although none of these models generated a very high precision score for the high risk category, several did have relatively high recall.  If one had to choose between these 6 models, the best one to use would be the Easy Ensemble with Adaptive Boost as it generated, not only the highest accuray score, but also the greatest precision and, more importantly, greatest sensitivity for predicting both high and low risk investments.

