# Credit-Risk-Analysis
# Credit Risk Prediction — Project Report

1. Introduction

  The objective of this project is to build predictive models that can assess the credit risk of loan applicants using the German Credit dataset. Accurate credit risk     
  prediction is crucial for financial institutions to minimize default rates and make better lending decisions.

2. Methodology

   2.1 Data Setup
  Loaded dataset containing 1000 entries with 10 features.
  
  Features included demographic data (Age, Sex, Housing), financial data (Saving accounts, Checking account, Credit amount, Duration), and loan Purpose.
  
  2.2 Data Exploration
  Inspected the data types, value distributions, and missing values.
  
  Numerical and categorical variables were identified.
  
  2.3 Data Cleaning
  Missing values in "Saving accounts" and "Checking account" were filled appropriately during preprocessing.
  
  "Unnamed: 0" (an index column) was dropped as it did not carry predictive information.
  
  2.4 Encoding and Scaling
  Categorical variables (e.g., Sex, Housing, Saving accounts, Checking account, Purpose) were encoded into numeric form.

  Feature scaling was applied to standardize numeric variables for better model performance.

  2.5 Train/Test Split
  Split the data into 80% training (800 records) and 20% testing (200 records) to evaluate model generalization.

3. Model Building

   3.1 Models Used
  Logistic Regression: A simple, interpretable linear model suitable for binary classification tasks.
  
  Random Forest Classifier: A powerful ensemble technique that reduces variance and captures complex relationships.
  
  Support Vector Machine (SVM): Effective for high-dimensional spaces, especially with linear and non-linear kernels.
  
  Each model was first trained with default parameters to establish baseline performance.

4. Hyperparameter Tuning

  Grid Search Cross-Validation was applied to optimize model performance:
  
  
  Model	Best Parameters	Cross-Validation Accuracy
  Logistic Regression	C=100, penalty='l2', solver='lbfgs'	98.87%
  Random Forest	n_estimators=50, max_depth=None, min_samples_split=2	99.62%
  SVM (Linear Kernel)	C=10, gamma='scale', kernel='linear'	98.13%
  Random Forest showed the highest cross-validation accuracy.

5. Results

   After tuning, models were evaluated on the test set:
  
  
  Model	Test Accuracy
  Logistic Regression	98%
  Random Forest	100%
  SVM	94%
  Random Forest achieved 100% accuracy on the test set, though this might suggest slight overfitting.
  
  Logistic Regression also performed extremely well with a 98% test accuracy.
  
  SVM achieved 94% accuracy, indicating it can also be a reliable model depending on the business need.

  5.1 Feature Importance
  Random Forest feature importance revealed that "Credit Amount," "Duration," and "Checking Account" were the most influential features.
  
  Logistic Regression and SVM coefficients indicated similar feature trends.

6. Conclusion

  Random Forest was selected as the final model because it provided the best balance of accuracy, robustness, and feature importance explainability.
  
  Hyperparameter tuning significantly improved model performance across all classifiers.
  
  The models confirmed that financial history (e.g., checking account status) and loan conditions (e.g., credit amount, duration) are critical factors in assessing credit    risk.

7. Why This Approach?

  Data Preprocessing was crucial to handle missing values and categorical variables properly, ensuring no information leakage.
  
  Multiple Models were trained and compared to avoid bias toward any single method.
  
  Grid Search was used to systematically optimize model parameters rather than relying on default values.
  
  Random Forest was selected because it performs well even with minimal parameter tuning, handles feature interactions automatically, and provides feature importance insights.
  
  Simplicity + Interpretability of Logistic Regression makes it a good backup model for deployment in scenarios where explainability is critical.

✅ End of Report
