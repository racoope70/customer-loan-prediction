# **Loan Approval Prediction using Machine Learning**

## **Table of Contents**
1. [Project Overview](#project-overview)
2. [Methodology](#methodology)
   - [Data Preprocessing](#data-preprocessing)
   - [Handling Class Imbalance](#handling-class-imbalance)
   - [Model Training & Evaluation](#model-training--evaluation)
3. [Results](#results)
4. [Visualizations](#visualizations)
5. [Conclusion](#conclusion)
6. [How to Use This Repository](#how-to-use-this-repository)
7. [Author](#author)

---

## **Project Overview**
This project focuses on predicting personal loan approvals using machine learning techniques. To address class imbalance, **SMOTE (Synthetic Minority Over-sampling Technique)** was applied, and model performance was validated using **stratified k-fold cross-validation**. Key evaluation metrics such as **precision, recall, F1-score, and AUC-ROC** were used to ensure robust performance.

---

## **Methodology**

### **Data Preprocessing**
- Cleaned and transformed the dataset.
- Addressed negative values in the `Experience` feature.
- Removed unnecessary features like `ID` and `ZIP Code`.

### **Handling Class Imbalance**
- Applied **SMOTE** to balance the dataset before model training.

### **Model Training & Evaluation**
- Used **Random Forest Regressor** as the primary model.
- Applied **Stratified k-Fold Cross-Validation** for robustness.
- Evaluated performance using:
  - **R² Score**
  - **Mean Squared Error (MSE)**
  - **Precision, Recall, and F1-Score**
  - **AUC-ROC Curve**

---

## **Results**
### **Key Performance Metrics**
| Metric        | Value  |
|--------------|--------|
| **R² Score (Original Test Data)** | **0.9739** |
| **MSE (Original Test Data)**      | **0.0024** |
| **Precision**                     | **0.99**   |
| **Recall**                         | **1.00**   |
| **F1-Score**                       | **1.00**   |
| **AUC**                            | **1.00**   |

- **High Precision (0.99)**: Ensures minimal false positives.
- **Perfect Recall (1.00)**: Successfully identifies all loan approvals.
- **Strong AUC-ROC (1.00)**: Shows excellent classification capability.

---

## **Visualizations**
### **1. Class Distribution Before and After SMOTE**
Demonstrates how SMOTE balanced the dataset by increasing the minority class representation.
![Class Distribution](![image](https://github.com/user-attachments/assets/087b6490-5441-4da7-b11b-c52098d5e53a)


### **2. Confusion Matrix**
Illustrates model accuracy by showing true positives, false positives, true negatives, and false negatives.
![Confusion Matrix](![image](https://github.com/user-attachments/assets/3a07ed21-da21-41f1-a623-2952256687ad)


### **3. Correlation Heatmap**
Displays the relationship between numerical features in the dataset.
![Correlation Heatmap](![image](https://github.com/user-attachments/assets/93e94497-a26d-459a-8a76-961ed58de37b)


### **4. Feature Importance**
Identifies which features had the most impact on loan approval predictions.
![Feature Importance](![image](https://github.com/user-attachments/assets/762813fd-8271-4737-aabe-21073cb62181)


### **5. Income Distribution**
Shows the distribution of income in the dataset.
![Income Distribution](![image](https://github.com/user-attachments/assets/21bcb2ca-805f-43ac-b086-f3388eb9d220)


### **6. Precision-Recall Curve**
Displays the trade-off between precision and recall at different classification thresholds.
![Precision Recall Curve](![image](https://github.com/user-attachments/assets/5ae31541-1594-4ba2-b3fa-d373f00ee012)


### **7. Residual Plot**
Evaluates model prediction errors.
![Residual Plot](![image](https://github.com/user-attachments/assets/dc2ff412-3e01-451c-a790-da733ae06b96)


### **8. ROC Curve**
Illustrates the trade-off between sensitivity (True Positive Rate) and specificity (False Positive Rate).
![ROC Curve](![image](https://github.com/user-attachments/assets/ae221c49-53d9-4557-b201-83b29076f976)


---

## **Conclusion**
- The **Random Forest model** trained with **SMOTE** and **stratified cross-validation** achieved **exceptional performance**, demonstrating near-perfect accuracy.
- The model effectively distinguishes between **approved and non-approved loan applications**, making it a reliable tool for loan approval prediction.
- Future work may include **threshold tuning, testing on real-world unseen data**, and **deploying the model as an API**.

---

## **How to Use This Repository**
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo-name.git
   cd your-repo-name
