# Temp-smart-home-forecasting
Objective: Reduce energy consumption by predicting indoor room temperature.

Regression:
- Transform: Normalization, Standardization.
- Models: Linear Regression, Decision Tree, Random Forest.
- Optional: Regularization (L1, L2, ElasticNet), Hyperparameter Tuning (Grid Search, Random Search).
- Best Model: Random Forest with a validation R-Square of 0.397.
- Note: Not suitable for continuous temperature prediction.

Classification:
- Models: Logistic Regression, Decision Tree, Random Forest, KNN, Custom Scoring, LGBM.
- Optional: Oversampling (Random, SMOTE, Borderline SMOTE, ADASYN) for imbalanced data in label column.
- Best Model: LGBM with the lowest AVG Electricity Cost Val and an ROC AUC score of 85.36%.
- Note: Suitable for binary classification, useful for controlling air conditioning and saving electric costs.

Summary:
- Objective: Reduce energy consumption by predicting indoor room temperature.
- Regression: Models used include Linear Regression, Decision Tree, and Random Forest.
- Classification: Models used include Logistic Regression, Decision Tree, Random Forest, KNN, Custom Scoring, and LGBM.
- Achieved best results with LGBM model, achieving the lowest AVG Electricity Cost Val and an ROC AUC score of 85.36%.
- Implemented oversampling techniques to handle imbalanced data.
- Utilized the predictions for controlling air conditioning and optimizing energy efficiency.


Detail:
In the regression phase, three models were evaluated: Linear Regression, Decision Tree Regressor, and Random Forest. 

1. Linear Regression:
   - Check Polynomial: The polynomial features were explored to capture non-linear relationships between the input features and the target variable.
   - Regularization:
     - Ridge: Ridge regularization was applied to control the complexity of the linear regression model and prevent overfitting.
     - Lasso: Lasso regularization was used to perform feature selection by shrinking irrelevant features' coefficients to zero.
     - Elastic Net: Elastic Net regularization combined Ridge and Lasso regularization techniques to balance model complexity and feature selection.
   - Alpha effects: Grid Search and Random Search methods were employed to find the optimal alpha parameter for regularization.
   - Conclusion: A conclusion was drawn on the effectiveness of the Linear Regression model with different techniques and regularization.

2. Decision Tree Regressor:
   - Check Polynomial: Similar to Linear Regression, polynomial features were considered to capture non-linear relationships within the decision tree model.
   - Strategy on Splitting in Timeseries Dataset: Strategies for splitting the dataset in the context of a timeseries dataset were explored to ensure appropriate model training and evaluation.
   - Tuning Again: The decision tree model was tuned to improve its performance by adjusting parameters and optimizing the tree structure.

3. Random Forest:
   - Conclusion for Regression model: A conclusion was provided for the Random Forest model, which combines multiple decision trees to enhance prediction accuracy and reduce overfitting.

In the classification phase, four models were evaluated: DecisionTreeClassifier, Random Forest, Logistic Regression, and KNN.

1. DecisionTreeClassifier:
   - Random Oversampling, SMOTE, Borderline SMOTE, and ADASYN were used as oversampling techniques to handle class imbalance in the dataset.

2. Random Forest: The Random Forest model was employed for classification tasks without explicitly mentioning specific techniques or modifications.

3. Logistic Regression:
   - Random Oversampling, SMOTE, Borderline SMOTE, and ADASYN were applied as oversampling techniques to address class imbalance in the dataset.

4. KNN:
   - Random Oversampling, SMOTE, Borderline SMOTE, and ADASYN were utilized as oversampling techniques to handle class imbalance.

A conclusion was drawn regarding the effectiveness of each classification model with different oversampling techniques. The evaluation metrics used were ROC AUC Score, which measures the model's ability to distinguish between classes, and F1 Score, which assesses the model's overall performance.

Additionally, an LGBM (LightGBM) model was evaluated separately, with metrics such as ROC AUC Score, average electricity cost, and F1 Score. The LGBM model demonstrated excellent performance, achieving a high ROC AUC Score, low average electricity cost, and high F1 Score.

In summary, the project involved regression and classification tasks. Regression models such as Linear Regression, Decision Tree Regressor, and Random Forest were evaluated, while classification models including DecisionTreeClassifier, Random Forest, Logistic Regression, and KNN were assessed with various oversampling techniques. The evaluation focused on the effectiveness of each model in predicting the target variable or classifying data, using metrics such as ROC AUC Score and F1 Score.
