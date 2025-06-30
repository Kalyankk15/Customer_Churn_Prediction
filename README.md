# 📉 Customer Churn Prediction 

This project focuses on predicting whether a customer is likely to **churn** (i.e., stop using a service) using a dataset from a telecom company. A variety of machine learning techniques were applied, with a focus on Random Forest Classifier with hyperparameter tuning.

---

## 📁 Dataset

It dataset includes customer details such as:

- Demographic info (gender, senior citizen, etc.)
- Services subscribed (phone, internet, streaming)
- Contract details
- Tenure, monthly & total charges
- Churn (Target variable)

---

## 📊 Project Workflow

### 1.  Data Collection

The dataset was collected from a public Kaggle dataset or similar source and imported as a CSV.

### 2.  Data Cleaning

- Removed `customerID` as it was irrelevant to prediction
- Verified no nulls in most columns
- Filled missing values in `TotalCharges` with **0**
- Identified **class imbalance** in the `Churn` target column

### 3.  Exploratory Data Analysis (EDA)

- Used box plots for detecting outliers in numerical columns
- Plotted correlations using heatmaps
- Created countplots for all categorical columns
- Observed imbalance and potential trends in churn rates

### 4.  Data Preprocessing

- Label Encoded target (`Churn`) and categorical variables
- Used `SMOTE` to handle **class imbalance**
- Split the dataset into **training** and **testing** sets

### 5.  Model Training

Trained several models with default parameters:

- Decision Tree
- Random Forest
- XGBoost

Random Forest showed the **best performance** initially and was selected for further tuning.

### 6.  Hyperparameter Tuning

- Performed hyperparameter tuning on the **Random Forest Classifier**
- Selected best parameters based on accuracy and cross-validation

### 7.  Model Evaluation

- Evaluated model performance using:
  - Accuracy Score
  - Confusion Matrix
  - Classification Report (Precision, Recall, F1)
- Final Accuracy: **78%**

### 8.  Model Saving & Deployment

- Saved the trained model using `pickle`
- Created a **predictive system** to take inputs and return churn predictions in real-time

---

## 🛠 Tools & Technologies Used

| Tool/Library     | Purpose                         |
|------------------|----------------------------------|
| Python (pandas, numpy) | Data manipulation           |
| Matplotlib, Seaborn    | Data visualization          |
| Scikit-learn            | Model building and evaluation |
| imblearn (SMOTE)        | Handle class imbalance      |
| XGBoost                 | Gradient boosting model     |
| Pickle                  | Model serialization         |


---



