# Module 20 Report Template

## Overview of the Analysis


### **Purpose of the Analysis**
The purpose of this analysis was to evaluate credit risk using a dataset containing financial information about loans. Specifically, the goal was to build a machine learning model to predict whether a loan was a **healthy loan** or a **high-risk loan**, enabling lenders to make informed decisions and mitigate financial risks.

---

### **Description of the Data**
The dataset contained credit risk-related financial data, with the target variable being `loan_status`. This variable was binary, representing:

- `0`: **Healthy loan** (low risk of default)  
- `1`: **High-risk loan** (high risk of default)  

#### **Label Distribution**:
Using the `value_counts()` method, the dataset showed:
```
healthy loan     18759
high-risk loan     625
```
This indicates a significant imbalance in the data, with the majority of loans being classified as healthy.

#### **Features**:
The features in the dataset included various financial attributes, such as income, debt-to-income ratio, credit history, and loan amount. These were used as predictors in the analysis.

---

### **Stages of the Machine Learning Process**

1. **Data Preparation**:
   - **Separated features and target variable**: The target variable (`y`) was `loan_status`, while the features (`X`) included all other columns.
   - **Addressed class imbalance** by evaluating performance metrics like precision, recall, and F1-score for both classes.

2. **Model Selection**:
   - Chose a **logistic regression model** for its simplicity, interpretability, and suitability for binary classification tasks.

3. **Model Training**:
   - Split the data into training and testing sets to evaluate model performance.
   - Trained the logistic regression model on the training set.

4. **Evaluation**:
   - Assessed the model’s performance using metrics such as:
     - **Accuracy**: Overall performance.
     - **Precision, Recall, and F1-Score**: Focused on individual class performance, especially the minority class (high-risk loans).



---

### **Methods Used**

- **Logistic Regression**:
   - Logistic regression was chosen due to its effectiveness for binary classification problems.
   - The model was trained using default hyperparameters, which provided strong performance metrics:
     - **Accuracy**: 99%
     - **Precision and Recall**: Demonstrated excellent prediction for healthy loans (100%) and good performance for high-risk loans (87% precision, 95% recall).




## Results


   ### **Machine Learning Model: Logistic Regression**

- **Description of Model Accuracy, Precision, and Recall Scores**:
  - **Accuracy**: 99%  
    The model correctly classified 99% of all loans (both healthy and high-risk).  
  - **Precision**:  
    - **Healthy Loan (0)**: 100% (all predicted healthy loans were correct).  
    - **High-Risk Loan (1)**: 87% (some healthy loans were misclassified as high-risk).  
  - **Recall**:  
    - **Healthy Loan (0)**: 100% (all actual healthy loans were correctly identified).  
    - **High-Risk Loan (1)**: 95% (most high-risk loans were correctly identified, with 5% false negatives).  

- **F1-Score**:
  - Healthy Loan (0): 100% (perfect balance between precision and recall).  
  - High-Risk Loan (1): 91% (reflects good performance despite minor misclassifications).  

This model demonstrated exceptional accuracy for the overall dataset, with near-perfect performance on the majority class (healthy loans) and strong recall for the minority class (high-risk loans).

## Summary


- **Best Performing Model**:  
   The **Logistic Regression** model performed exceptionally well, achieving:  
   - **Accuracy**: 99%  
   - **Healthy Loan (0)**: Perfect precision, recall, and F1-score (100%).  
   - **High-Risk Loan (1)**: High precision (87%) and recall (95%), indicating strong performance in identifying high-risk loans.

- **Why It Performs Best**:  
   The model provides a balanced approach, excelling in both overall accuracy and its ability to detect high-risk loans with minimal false negatives (high recall for class 1). This makes it reliable for practical use, particularly when identifying loans that may pose a financial risk.

---

### **Does Performance Depend on the Problem?**
Yes, performance depends on the problem and the business objectives:

- If **predicting high-risk loans (1)** is more critical (e.g., minimizing financial loss from defaults):  
   - Focus should be on **recall** for high-risk loans to ensure most risky loans are correctly identified, even at the cost of some false positives (misclassified healthy loans).  
   - The Logistic Regression model already achieves 95% recall for this class, which is highly effective.

- If **predicting healthy loans (0)** is more important (e.g., minimizing rejection of good borrowers):  
   - The model’s perfect recall (100%) for healthy loans ensures no healthy loan is misclassified as high-risk.

---

### **Recommendation**
The **Logistic Regression model** is recommended as it performs well across both classes and balances precision and recall effectively. Its strong recall for high-risk loans makes it particularly suited for scenarios where identifying risky loans is critical to minimizing financial loss. 

For further improvement,  hyperparameter tuning could enhance precision for high-risk loans without compromising recall.
