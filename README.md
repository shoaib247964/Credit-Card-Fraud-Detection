# Credit-Card-Fraud-Detection
Credit Card Fraud Detection using Random Forest Classifier
1. Introduction
Credit card fraud detection is a crucial task in the financial industry. In this project, a machine learning approach using a Random Forest Classifier was employed to identify fraudulent transactions. The dataset was highly imbalanced, and appropriate resampling techniques were used to address this issue.
2. Dataset Overview
The dataset used contains credit card transactions, with features transformed using PCA for privacy reasons. The target variable is 'Class', where 0 represents a legitimate transaction and 1 represents fraud.
Class Distribution Before Resampling:
0.0: 14268
1.0: 65
Class Distribution After Resampling:
0.0: 14268
1.0: 14268
3. Data Preprocessing
Data preprocessing included checking for missing values, standardizing features, and resampling the dataset using techniques like SMOTE to handle class imbalance.
4. Model Building and Evaluation
A Random Forest Classifier was used. Hyperparameter tuning was done using GridSearchCV, and the best parameters found were:
{'bootstrap': False, 'max_depth': None, 'min_samples_leaf': 1, 'min_samples_split': 2, 'n_estimators': 100}
The model showed excellent performance on the test set, with the following evaluation metrics:
Confusion Matrix:
[[3566    2]
 [   0   16]]
Classification Report:
              precision    recall  f1-score   support
         0.0       1.00      1.00      1.00      3568
         1.0       0.89      1.00      0.94        16

    accuracy                           1.00      3584
   macro avg       0.94      1.00      0.97      3584
weighted avg       1.00      1.00      1.00      3584
5. Confusion Matrix Visualization
A heatmap was plotted using Seaborn to visualize the confusion matrix for better interpretation.
6. Conclusion
The Random Forest Classifier performed exceptionally well on the fraud detection task, especially after handling class imbalance. Hyperparameter tuning contributed to further performance improvement.
