# Data Science Project 2

## Objective:
Develop a machine learning model to predict brain stroke risk, utilizing health and demographic factors. This addresses a critical healthcare challenge, as stroke is the 2nd leading cause of death globally, responsible for approximately 11% of total deaths according to the World Health Organization.

## Overview:
•**Dataset**: 4,908 records with 16 features after preprocessing<br><br>
•**Features include**: gender, age, hypertension, heart disease, marital status, work type, residence type, glucose level, BMI, smoking status<br><br>
•**Tool**s: R (packages: caret, nnet, pROC, gmodels, dplyr, e1071)<br><br>
•**Main techniques**: Logistic Regression, Support Vector Machines (SVM)<br><br>
•**Data partitioning**: 17% test set, 17% of remaining as validation set, rest as training set<br><br>

## Models & Performances:
1. **Logistic Regression**:
   • Validation: Accuracy 91.13%, Recall 80.07%<br><br>
   • Test: Accuracy 90.29%, Recall 39.02%, Precision not provided<br><br>
   • Showed signs of overfitting due to significant drop in recall on test data<br><br>

2. **SVM**:
   • Validation: Accuracy 50.48%, Recall 49.83%, Precision 30.98%<br><br>
   • Test: Accuracy 41.37%, Recall 31.71%, Precision 2.74%<br><br>
   • Performed poorly, close to random guessing<br><br>

## Hurdles and Overcomes:
• **Missing data**: Removed 201 rows with missing BMI values<br><br>
• **Data errors**: Standardized age entries below 2 years old<br><br>
• **Class imbalance**: Addressed using oversampling techniques<br><br>
• **Categorical variables**: Created dummy variables for work type, residence type, and smoking status<br><br>
• **Feature selection**: Used Recursive Feature Elimination (RFE) to identify top 5 predictors<br><br>
• **Overfitting in Logistic Regression**: Identified through performance discrepancy between validation and test sets<br><br>
• **Poor SVM performance**: Highlighted need for hyperparameter tuning<br><br>

## Conclusions :
• Logistic Regression showed initial promise but suffered from overfitting<br><br>
• SVM underperformed significantly, suggesting need for further optimization<br><br>
• Top predictors identified: age, heart disease, smoking status, residence type, glucose level<br><br>
• Data preprocessing and feature engineering were crucial for model development<br><br>
• Class imbalance remains a significant challenge in accurate stroke prediction<br><br>

## Recommendations : 
•Adjust the gap between recency and overall spending by upselling<br><br>
•They need to address the highly important but negatively correlated "teen home" feature<br><br>
•They can capitalize on the high importance "web visits per month" feature to drive even greater online traffic<br><br>


