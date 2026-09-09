# 🚲 Bike Sharing Demand Prediction

This project analyzes a bike-sharing dataset and builds machine learning models to predict the total number of bike rentals (`cnt`).

The project includes **Exploratory Data Analysis (EDA)**, feature engineering, data preprocessing, Linear Regression, and tree-based regression models.

---

## 📌 Project Overview

Bike-sharing systems generate a large amount of data related to weather, time, season, working days, and rental demand.

The main objective of this project is to:

* Explore the bike-sharing dataset
* Understand factors affecting bike rental demand
* Analyze correlations between features and rental counts
* Perform feature engineering
* Prepare data for machine learning
* Train and evaluate different regression models
* Compare model performance

---

## 📊 Dataset

The project uses the **UCI Bike Sharing Dataset**, specifically the hourly data.

Dataset source:

```text
https://raw.githubusercontent.com/muditp19/UCI_Bike-sharing-dataset/master/hour.csv
```

The dataset contains information about bike rentals by hour, including weather and temporal features.

### Target Variable

| Column | Description                  |
| ------ | ---------------------------- |
| `cnt`  | Total number of bike rentals |

The columns `casual` and `registered` were excluded from the final modeling because they directly contribute to the target variable and can cause **data leakage**.

---

## 🔎 Exploratory Data Analysis

The notebook performs several EDA steps:

### Dataset inspection

* Dataset structure
* Data types
* Missing values
* Duplicate rows
* Descriptive statistics

### Correlation analysis

Correlation with `cnt` is analyzed to identify features that have the strongest relationship with bike rental demand.

A correlation heatmap is also created for the most correlated numerical features.

### Visualizations

The project analyzes:

* 🌡️ Temperature vs. bike rentals
* 🕐 Average rentals by hour
* 💼 Working day vs. non-working day
* 🌱 Rentals by season
* 📈 Distribution of total bike rentals

---

## 🛠️ Feature Engineering

The `dteday` column is converted into a datetime format and several new features are extracted:

```text
year
month
day
day_of_week
day_of_year
week_of_year
is_weekend
```

The original `dteday` column is then removed.

This allows the models to work with more meaningful temporal information.

---

## 🧹 Data Preprocessing

Several preprocessing techniques are used throughout the project.

### Removing leakage

The following columns are removed:

```text
registered
casual
```

These variables are directly related to `cnt` and therefore should not be used as independent predictors.

### Feature scaling

`StandardScaler` is used to standardize numerical features before Linear Regression.

### One-Hot Encoding

Categorical variables are transformed using:

```python
OneHotEncoder(handle_unknown="ignore")
```

### Target transformation

For one of the Linear Regression experiments, the target variable is transformed using:

```python
y = np.log1p(df["cnt"])
```

Predictions are converted back to the original scale using:

```python
np.expm1()
```

---

## 🤖 Machine Learning Models

Several regression algorithms are tested.

### 1. Linear Regression

A baseline Linear Regression model is trained using selected features.

The model is evaluated using:

* MAE
* MSE
* RMSE
* Median Absolute Error
* R²
* MAPE

---

### 2. Multiple Linear Regression

A second Linear Regression experiment uses multiple available features after preprocessing and scaling.

---

### 3. Linear Regression with One-Hot Encoding

Categorical variables are encoded using `OneHotEncoder`, while numerical variables are standardized.

The target variable is also transformed using `log1p`.

---

### 4. Extra Trees Regressor

An `ExtraTreesRegressor` model is trained with:

```python
n_estimators=500
min_samples_leaf=2
max_features=0.8
random_state=42
```

---

### 5. Random Forest Regressor

A `RandomForestRegressor` is also evaluated with:

```python
n_estimators=500
min_samples_leaf=2
max_features=0.8
random_state=42
```

---

### 6. HistGradientBoosting Regressor

The project also tests `HistGradientBoostingRegressor` with:

```python
max_iter=500
learning_rate=0.05
max_leaf_nodes=31
l2_regularization=0.1
random_state=42
```

---

## 📏 Evaluation Metrics

The following metrics are used to evaluate regression models:

### MAE — Mean Absolute Error

Measures the average absolute difference between actual and predicted values.

### RMSE — Root Mean Squared Error

Penalizes larger prediction errors more strongly than MAE.

### R² — R-squared

Measures how much of the variation in the target variable is explained by the model.

Higher R² generally indicates better performance.

### MAPE — Mean Absolute Percentage Error

Measures prediction error as a percentage of the actual value.

---

## 🧰 Technologies & Libraries

The project is implemented in Python using:

* Python
* NumPy
* Pandas
* Matplotlib
* Plotly
* Scikit-learn
* Jupyter Notebook

Main Scikit-learn components include:

```text
LinearRegression
ExtraTreesRegressor
RandomForestRegressor
HistGradientBoostingRegressor
StandardScaler
OneHotEncoder
ColumnTransformer
Pipeline
train_test_split
```

---

## 📁 Project Structure

```text
Bike-Sharing/
│
├── Bike-Sharing.ipynb
└── README.md
```

## 📈 Project Workflow

```text
Dataset
   ↓
Data Inspection
   ↓
Data Cleaning
   ↓
Exploratory Data Analysis
   ↓
Correlation Analysis
   ↓
Feature Engineering
   ↓
Feature Selection
   ↓
Scaling / Encoding
   ↓
Train-Test Split
   ↓
Model Training
   ↓
Model Evaluation
   ↓
Model Comparison
```

---

## 👤 Author

**Suhrobjon Ibodullayev**

---

## 📄 License

This project is intended for educational and portfolio purposes.

