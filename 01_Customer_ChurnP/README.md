# Customer Churn Prediction

Predict whether an e-commerce customer is likely to leave the platform using machine learning.

## Overview

Customer churn is one of the biggest challenges for online businesses. Losing existing customers is often more expensive than acquiring new ones.

This project performs data analysis, preprocessing, feature engineering, and machine learning to predict customer churn based on customer behavior and transaction history.

## Dataset

The dataset contains **5,630 customer records** with **20 features** describing customer behavior and demographics.

### Target Variable

- Churn
  - `0` → Customer stays
  - `1` → Customer leaves

### Features

- CustomerID
- Tenure
- PreferredLoginDevice
- CityTier
- WarehouseToHome
- PreferredPaymentMode
- Gender
- HourSpendOnApp
- NumberOfDeviceRegistered
- PreferedOrderCat
- SatisfactionScore
- MaritalStatus
- NumberOfAddress
- Complain
- OrderAmountHikeFromlastYear
- CouponUsed
- OrderCount
- DaySinceLastOrder
- CashbackAmount

---

## Project Workflow

### 1. Data Loading

- Import dataset
- Explore feature descriptions
- Inspect dataset structure

### 2. Exploratory Data Analysis (EDA)

- Dataset overview
- Missing value analysis
- Distribution analysis
- Numerical feature visualization
- Categorical feature visualization
- Correlation analysis

### 3. Data Preprocessing

- Handle missing values
- Encode categorical variables
- Prepare numerical features
- Remove unnecessary columns
- Split train and test datasets

### 4. Machine Learning

Train a classification model to predict customer churn.

General workflow:

- Feature selection
- Train/Test split
- Model training
- Prediction
- Performance evaluation

### 5. Model Evaluation

Common evaluation metrics include:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix
- ROC-AUC

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab
- Plotly

---

## Repository Structure

```
Customer-Churn-Prediction/
│
├── Customer Churn.ipynb
├── README.md
```

---

## Installation

Clone the repository

```bash
git clone https://github.com/yourusername/Customer-Churn-Prediction.git
```

Install dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

---

## Usage

Open the notebook in Google Colab or Jupyter Notebook.

Run each cell sequentially to:

- Load the dataset
- Explore the data
- Preprocess features
- Train the model
- Evaluate performance

---

## Project Goals

- Understand customer behavior
- Identify factors affecting churn
- Build a predictive machine learning model
- Improve customer retention strategies

---

## Future Improvements

- Hyperparameter tuning
- Cross-validation
- Feature engineering
- Compare multiple ML algorithms
- Deploy the model with Streamlit
- Build an interactive dashboard

---

## Author

Sukhrobjon Ibodullayev

GitHub:
https://github.com/Suhrobjonibodullayev

---

## License

This project is released under the MIT License.
