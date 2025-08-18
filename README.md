# Advanced Telco Customer Churn Prediction (EDA)

## Introduction
Customer churn is a critical business problem in the telecom industry. Companies want to predict which customers are likely to leave (churn) so they can take preventive actions.  

This project performs **Exploratory Data Analysis (EDA)** and **data preprocessing** on the **Telco Customer Churn dataset** to uncover key insights and prepare data for machine learning modeling.  

---

## 📊 Dataset Information
- **Source**: [Kaggle – Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)  
- **Size**: ~7,043 rows, 21 columns  
- **Target variable**: `Churn` (Yes/No)  

### Features
- Customer demographics: `gender`, `SeniorCitizen`, `Partner`, `Dependents`  
- Service information: `PhoneService`, `InternetService`, `Contract`, `PaymentMethod`  
- Account info: `tenure`, `MonthlyCharges`, `TotalCharges`  
- Churn label: `Churn`  

---

## Installation & Requirements
To run this project, install dependencies from `requirements.txt`:  

```bash
git https://github.com/Tenura2001/Telco_Customer_Churn_Prediction-EDA.git
cd TELCO_CUSTOMER_CHURN_PREDICTION
pip install -r requirements.txt
```

**Main Libraries Used**  
- `pandas`, `numpy` → data manipulation  
- `matplotlib`, `seaborn` → visualization  
- `scikit-learn` → preprocessing  

---

## Exploratory Data Analysis (EDA) & Preprocessing

### Step 0: Handling Missing Values  
- Converted `TotalCharges` column to numeric.  
- Imputed missing values with median/mode as appropriate.  
- Saved as: `Churn_Missing_Value_Handled.csv`.  

### Step 1: Handling Outliers  
- Identified outliers using boxplots.  
- Applied capping/transformations.  
- Saved as: `Churn_Outliers_Handled.csv`.  

### Step 2: Feature Binning  
- Binned `tenure` into categories (e.g., New, Mid-term, Long-term).  
- Saved as: `Churn_Binning_Applied.csv`.  

### Step 3: Feature Encoding  
- Applied label encoding & one-hot encoding for categorical variables.  
- Saved as: `Churn_Encoded.csv`.  

### Step 4: Feature Scaling  
- Standardized/normalized numerical features.  
- Produced final dataset: `Churn_Final.csv`.  

---

## 📂 Project Structure
```
ADVANCED_TELCO_CUSTOMER_CHURN_PREDICTION/
│── data/
│   ├── raw/
│   │   └── Telco-Customer-Churn.csv
│   └── processed/
│       ├── Churn_Missing_Value_Handled.csv
│       ├── Churn_Outliers_Handled.csv
│       ├── Churn_Binning_Applied.csv
│       ├── Churn_Encoded.csv
│       └── Churn_Final.csv
│
│── 0_handle_missing_value.ipynb
│── 1_handling_outliers.ipynb
│── 2_feature_binning.ipynb
│── 3_feature_encoding.ipynb
│── 4_feature_scaling.ipynb
│── requirements.txt
│── README.md
│── .env
```

---

## 📈 Key Insights
- Senior citizens and customers with month-to-month contracts are more likely to churn.  
- Higher monthly charges are correlated with higher churn.  
- Longer tenure significantly reduces churn probability.  

---

##  How to Run
1. Clone the repo.  
2. Install requirements.  
3. Open Jupyter Notebook.  
   ```bash
   jupyter notebook 0_handle_missing_value.ipynb
   ```
4. Run notebooks in sequential order (`0 → 4`).  

---

##  Next Steps
- Build machine learning models (Logistic Regression, Random Forest, XGBoost).  
- Compare model performance.  
- Deploy best model via Flask/Streamlit.  

---

## 📚 References
- Dataset: [Kaggle – Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)  
- Documentation: [scikit-learn](https://scikit-learn.org/stable/)  
