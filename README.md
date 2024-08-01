# Data Science Project2

## Objective:
Develop a machine learning model to predict brain stroke risk, utilizing health and demographic factors. This addresses a critical healthcare challenge, as stroke is the 2nd leading cause of death globally, responsible for approximately 11% of total deaths according to the World Health Organization.

## Overview:
• Dataset: 4,908 records with 16 features after preprocessing
• Features include: gender, age, hypertension, heart disease, marital status, work type, residence type, glucose level, BMI, smoking status
• Tools: R (packages: caret, nnet, pROC, gmodels, dplyr, e1071)
• Main techniques: Logistic Regression, Support Vector Machines (SVM)
• Data partitioning: 17% test set, 17% of remaining as validation set, rest as training set

##Models & Performances:
1. Logistic Regression:
   • Validation: Accuracy 91.13%, Recall 80.07%
   • Test: Accuracy 90.29%, Recall 39.02%, Precision not provided
   • Showed signs of overfitting due to significant drop in recall on test data

2. SVM:
   • Validation: Accuracy 50.48%, Recall 49.83%, Precision 30.98%
   • Test: Accuracy 41.37%, Recall 31.71%, Precision 2.74%
   • Performed poorly, close to random guessing

##Hurdles and Overcomes:
• Missing data: Removed 201 rows with missing BMI values
• Data errors: Standardized age entries below 2 years old
• Class imbalance: Addressed using oversampling techniques
• Categorical variables: Created dummy variables for work type, residence type, and smoking status
• Feature selection: Used Recursive Feature Elimination (RFE) to identify top 5 predictors
• Overfitting in Logistic Regression: Identified through performance discrepancy between validation and test sets
• Poor SVM performance: Highlighted need for hyperparameter tuning

##Conclusions :
• Logistic Regression showed initial promise but suffered from overfitting
• SVM underperformed significantly, suggesting need for further optimization
• Top predictors identified: age, heart disease, smoking status, residence type, glucose level
• Data preprocessing and feature engineering were crucial for model development
• Class imbalance remains a significant challenge in accurate stroke prediction

## Recommendations : 
  - Expand training data size and diversity to improve generalization
  - Explore advanced techniques like ensemble methods or neural networks
  - Conduct more rigorous hyperparameter tuning, especially for SVM
  - Consider other evaluation metrics beyond accuracy, given the imbalanced nature of the problem
  - Incorporate domain expertise to refine feature selection and engineering
