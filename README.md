# Credit Risk Analysis
## Module 17: Introductio to Supervised Machine Learning
---

### Overview
In this module students were introduced to Supervised Machine Learning, a method by which statistical algorithms learn from training data sets and make predictions based on additional data.  For this exercise we focused on creating a model which would be able to predict if a particular loan would be high or low risk based on many other parameters(features).  Upon analysis, we discovered that our dataset was quite unbalanced with over 68,470 out of the 68,817 loans considered low risk.  Consequently, we needed to sample our data in a variety of ways to determine which would create the most effective model.  It will be important for our model to have high sensitivity to identify and avoid the high risk loans.   

### Results ( bulleted list that describes the balanced accuracy score and the precision and recall scores of all six machine learning models)
Oversampling the dataset - This model chooses more of the high risk loans until the class samples are approximately the same size 
Low Risk:  51,352
High Risk:  51,352

Synthetic Minority Oversampling Technique (SMOTE) - This model creates synthetic high risk data based on similar data points in the dataset.
Low Risk:  51,352
High Risk:  51,352

Undersampling - This model decreased the size of the low risk loans such that the class samples are approximately the same size
Low Risk:  260
High Risk:  260

SMOTE + Edited Nearest Neighbor (SMOTEENN) - This model oversamples the high risk data and undersamples the the low risk data by dropping any data that are borderline.
Low Risk:  68,460
High Risk:  68,460

### Summary (recommendation on which model to use, or there is no recommendation with a justification)
