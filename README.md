## Analysis

**Purpose of the Analysis:**

The purpose of this analysis was to evaluate and predict loan risk using machine learning models. Specifically, the goal was to classify loans into two categories: healthy loans (0) and high-risk loans (1), based on various financial features.

**Data Overview:**

The dataset contains financial information about loans, including:
- `loan_size`: The amount of the loan.
- `interest_rate`: The interest rate on the loan.
- `borrower_income`: The income of the borrower.
- `debt_to_income`: The ratio of the borrower's debt to income.
- `num_of_accounts`: The number of accounts the borrower has.
- `derogatory_marks`: The number of derogatory marks on the borrower's credit report.
- `total_debt`: The total debt of the borrower.
- `loan_status`: The target variable indicating whether the loan is high-risk (1) or healthy (0).

**Variable Distribution:**

- **`loan_status` value counts:**
  - Healthy loans (0): 18,765
  - High-risk loans (1): 619

**Machine Learning Process:**

1. **Data Preparation:**
   - Loaded data from `lending_data.csv`.
   - Separated the target variable (`loan_status`) and features.
   - Split the data into training and testing sets.

2. **Model Training:**
   - Used a logistic regression model to fit the training data.

3. **Prediction and Evaluation:**
   - Made predictions on the testing set.
   - Evaluated the model using confusion matrix and classification report.

**Methods Used:**

- **Logistic Regression:** A classification algorithm used to model the probability of a binary outcome (high-risk vs. healthy loans).

## Results

- **Machine Learning Model 1: Logistic Regression**
  - **Accuracy:** 99%
  - **Precision (for healthy loans):** 1.00
  - **Recall (for healthy loans):** 0.99
  - **Precision (for high-risk loans):** 0.85
  - **Recall (for high-risk loans):** 0.91

## Summary

- **Best Performing Model:**
  - The Logistic Regression model achieved a high accuracy of 99%, with very high precision and recall for healthy loans, and decent precision and recall for high-risk loans.

- **Performance Consideration:**
  - **Healthy Loans:** High precision and recall are crucial to minimize false positives (incorrectly labeling a healthy loan as high-risk) and ensure the majority of healthy loans are correctly identified.
  - **High-Risk Loans:** It's also important to identify as many high-risk loans as possible, so the model’s recall for high-risk loans (0.91) indicates it performs well in catching potential issues.

- **Recommendation:**
  - The Logistic Regression model is recommended due to its high accuracy and reliable performance across both classes. The model performs well in predicting healthy loans and also maintains a reasonable ability to identify high-risk loans.

If you need to improve the model further, consider exploring additional algorithms or techniques such as:
- **Cross-validation** for better generalization.
- **Feature engineering** to enhance model performance.
- **Other classification algorithms** (e.g., Random Forest, Gradient Boosting) for comparison.
