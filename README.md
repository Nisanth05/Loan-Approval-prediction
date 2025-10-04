
# 🏦 Loan Status Prediction using Machine Learning

### 📘 Project Overview
This project aims to predict whether a **loan application will be approved or not** based on applicant details such as income, education, employment, and credit history.  
It uses **machine learning classification models** to assist financial institutions in making data-driven lending decisions.

---

### 📂 Dataset Information
The dataset contains information about loan applicants, including demographic, financial, and credit-related features.

| Feature | Description |
|----------|--------------|
| Gender | Male / Female |
| Married | Applicant marital status |
| Dependents | Number of dependents |
| Education | Graduate / Not Graduate |
| Self_Employed | Employment type |
| ApplicantIncome | Income of the applicant |
| CoapplicantIncome | Income of the co-applicant |
| LoanAmount | Loan amount in thousands |
| Loan_Amount_Term | Term of the loan in months |
| Credit_History | Credit history meets guidelines (1/0) |
| Property_Area | Urban / Rural / Semiurban |
| Loan_Status | Target variable — Y (Approved), N (Not Approved) |

---

### 🧹 Data Preprocessing
1. **Removed unnecessary columns** – Dropped `Loan_ID`.  
2. **Handled missing values** using median/mode imputation.  
3. **Encoded categorical variables**:
   - Label encoding for `Loan_Status`
   - Binary encoding for `Gender`, `Married`, `Education`, `Self_Employed`
   - One-hot encoding for `Property_Area`
4. **Handled imbalanced data** (422 approved vs 192 rejected).  
5. **Feature scaling** with `StandardScaler`.

---

### 📊 Exploratory Data Analysis
Key visualizations:
- Loan approval rate by **Gender**, **Education**, and **Property Area**
- Distribution of applicant income and loan amount


---

### ⚙️ Model Building

#### Models Used:
- **Support Vector Machine (RBF kernel)**
- **Logistic Regression**
- **Random Forest Classifier**

#### Train-Test Split:
- 80% training data  
- 20% test data  
- Stratified split to preserve class balance  

---

### 🧠 Model Performance

| Model | Accuracy | F1-Score (Class 1) | Recall (Class 1) | Precision (Class 1) |
|--------|-----------|--------------------|------------------|---------------------|
| **Logistic Regression** | **0.86** | **0.91** | **0.99** | 0.84 |
| **SVM (RBF)** | 0.85 | 0.90 | 0.99 | 0.83 |
| **Random Forest** | 0.82 | 0.88 | 0.92 | 0.84 |

✅ **Best Model:** Logistic Regression  
It achieved the **highest F1-score and recall**, meaning it correctly identified almost all approved loan cases while maintaining a good balance between precision and recall.

---

### 🔍 Insights
- Credit history and applicant income are strong predictors of loan approval.
- Applicants with a **strong credit history** have a much higher approval rate.
- Logistic Regression performed best, likely due to the dataset being **linearly separable** after encoding and scaling.

---

### 📦 Tech Stack
- **Python**
- **Pandas, NumPy**
- **Matplotlib, Seaborn**
- **Scikit-learn**

---

### 📈 Future Improvements
- Apply **SMOTE or class-weight balancing** for better handling of imbalance.  
- Experiment with **XGBoost or Gradient Boosting**.  
- Perform **hyperparameter tuning** for Random Forest and SVM.  
- Deploy the model using **Streamlit** or **Flask** for interactive predictions.

---

### 👨‍💻 Author
**Nisanth Jose**  
 

---


