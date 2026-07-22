# Air Ticket Price Prediction

A machine learning project that predicts airline ticket prices using flight information such as airline, source, destination, departure time, arrival time, duration, and other travel-related features.

## Project Overview

The goal of this project is to build and compare multiple regression models to estimate flight ticket prices.

The workflow includes:

- Data loading
- Exploratory Data Analysis (EDA)
- Data preprocessing
- Feature engineering
- Building a preprocessing pipeline
- Training multiple machine learning models
- Model evaluation
- Generating predictions for the test dataset

## Dataset

The project uses two datasets:

- `train_data.csv` — Training dataset
- `test_data.csv` — Test dataset

Target variable:

- `price`

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Plotly
- Scikit-learn

## Machine Learning Models

The following regression algorithms were trained and compared:

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor

## Data Preprocessing

The preprocessing pipeline includes:

- Handling numerical and categorical features
- Feature transformation
- Encoding categorical variables
- Preparing data using Scikit-learn Pipelines

## Model Evaluation

Models were evaluated using regression metrics.

Final comparison showed that:

| Model | Performance |
|--------|------------|
| Linear Regression | Baseline model |
| Decision Tree | Better than baseline |
| Random Forest | Best performing model |

Random Forest achieved the lowest prediction error among the tested models.

## Project Structure

```
├── airticket-price-prediction.ipynb
├── train_data.csv
├── test_data.csv
└── README.md
```

## Workflow

1. Import libraries
2. Load dataset
3. Explore the data
4. Visualize important features
5. Preprocess the dataset
6. Build preprocessing pipeline
7. Train regression models
8. Evaluate model performance
9. Select the best model
10. Predict ticket prices for the test dataset
11. Export submission file

## Results

The Random Forest Regressor produced the best results and was selected as the final model for prediction.

## Future Improvements

- Hyperparameter tuning with GridSearchCV or RandomizedSearchCV
- Feature selection
- Cross-validation
- Ensemble methods such as XGBoost, LightGBM, or CatBoost
- Additional feature engineering


## Author

Suhrobjon Ibodullayev

GitHub: https://github.com/Suhrobjonibodullayev
