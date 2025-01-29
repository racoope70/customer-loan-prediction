# **Loan Approval Prediction using Machine Learning**

## **Table of Contents**
1. [Project Overview](#project-overview)
2. [Methodology](#methodology)
   - [Data Preprocessing](#data-preprocessing)
   - [Handling Class Imbalance](#handling-class-imbalance)
   - [Model Training & Evaluation](#model-training--evaluation)
3. [Results](#results)
4. [Visualizations & Analysis](#visualizations--analysis)
5. [Conclusion](#conclusion)
6. [License](#license)
7. [Acknowledgments](#acknowledgments)
8. [How to Use This Repository](#how-to-use-this-repository)


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

## **Visualizations & Analysis**
### **1. Class Distribution Before and After SMOTE**
- **Why It’s Important:**  
  This chart demonstrates how **SMOTE** balanced the dataset by increasing the representation of the minority class. Originally, loan approvals were significantly fewer than denials. After SMOTE, the dataset was evenly balanced.

![image](https://github.com/user-attachments/assets/0e1ae88e-ffc9-4464-8078-c9e3a350953b)


---

### **2. Confusion Matrix**
- **Why It’s Important:**  
  This matrix shows how well the model performed in predicting **loan approvals (1) vs. non-approvals (0)**. It visualizes the true positives, false positives, true negatives, and false negatives.

![image](https://github.com/user-attachments/assets/fc3181af-8049-40dd-a9f5-70c5d49eb82c)


---

### **3. Correlation Heatmap**
- **Why It’s Important:**  
  This heatmap helps determine **which variables can be used for regression** by showing how strongly features correlate with `Personal Loan`. Features with higher correlation are better predictors.

![image](https://github.com/user-attachments/assets/33ef4483-24e6-45c3-8ad0-2c39683b4406)


---

### **4. Feature Importance**
- **Why It’s Important:**  
  This chart identifies which features had the most impact on loan approval predictions. **High-importance features** like `Income` and `Education` were used in model training, while low-importance ones were removed.

![image](https://github.com/user-attachments/assets/a244b605-716a-4dd2-ae54-804bc9d87dc5)

---

### **5. Income Distribution**
- **Why It’s Important:**  
  Understanding the **distribution of income** helps in analyzing its effect on loan approvals. If most applicants have lower incomes but approvals are skewed towards higher incomes, **bias might exist**.

![image](https://github.com/user-attachments/assets/307780cc-bf48-4290-ba70-0d6bad29a804)


---

### **6. Precision-Recall Curve**
- **Why It’s Important:**  
  This chart evaluates the **trade-off between precision and recall**, which is crucial for handling imbalanced data. A higher precision-recall curve indicates better classification performance.

![image](https://github.com/user-attachments/assets/ca148ea4-e4ad-4c4b-a489-40dcf0ced209)


---

### **7. Residual Plot**
- **Why It’s Important:**  
  A **residuals plot** helps to check for any systematic error in predictions. If residuals are randomly scattered around zero, it indicates that the model does not have a systematic bias.

![image](https://github.com/user-attachments/assets/4063706f-b818-4888-bc80-93cc751b7fcb)

---

### **8. ROC Curve**
- **Why It’s Important:**  
  The **ROC Curve** helps to evaluate how well the model distinguishes between loan approvals and denials. The closer the curve is to the top left, the better the performance.

![image](https://github.com/user-attachments/assets/ff003fe3-d745-4667-8eb0-32498f1e9119)


---

## **Conclusion**
- The **Random Forest model** trained with **SMOTE** and **stratified cross-validation** achieved **exceptional performance**, demonstrating near-perfect accuracy.
- The model effectively distinguishes between **approved and non-approved loan applications**, making it a reliable tool for loan approval prediction.
- Future work may include **threshold tuning, testing on real-world unseen data**, and **deploying the model as an API**.

---

## **License**
This project is licensed under the [MIT License](LICENSE). 

---

## **Acknowledgments**
- This project was built using the [Personal Loan Modeling dataset](https://www.kaggle.com/teertha/personal-loan-modeling) from Kaggle.
- Thanks to [scikit-learn](https://scikit-learn.org/) for machine learning tools.
- Inspired by various open-source loan prediction projects.

---

## **How to Use This Repository**
### **Clone the repository:**
```bash
git clone https://github.com/your-repo-name.git
cd your-repo-name

