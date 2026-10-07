# House Price Prediction Using Machine Learning

A machine learning regression project for predicting residential property prices in Bangalore using data preprocessing, exploratory data analysis, feature engineering, and multiple regression algorithms.

## 📌 Project Overview

Accurate house price estimation depends on several property characteristics such as location, total area, number of bedrooms, bathrooms, and area type.

This project develops and evaluates machine learning regression models to predict house prices using a structured Bangalore housing dataset.

The workflow covers:

- Data cleaning and preprocessing
- Exploratory Data Analysis
- Feature engineering
- Categorical variable encoding
- Outlier handling
- Train-test splitting
- Regression model development
- Model evaluation and comparison
- Feature importance analysis

## 🎯 Objectives

- Analyze the factors associated with residential property prices.
- Prepare raw housing data for machine learning.
- Engineer meaningful features from existing property attributes.
- Compare multiple regression algorithms.
- Evaluate models using RMSE, MAE, and R².
- Identify the most influential features for price prediction.
- Build a reproducible machine learning workflow.

## 📊 Dataset

The project uses a Bangalore/Bengaluru house price dataset containing property-related attributes such as:

- Area Type
- Location
- Size / BHK
- Total Square Footage
- Number of Bathrooms
- Price

The cleaned dataset contained **11,825 usable observations** for the final train-test workflow.

## 🔧 Data Preprocessing

The following preprocessing steps were performed:

- Handling missing values
- Cleaning property-size information
- Converting total square footage ranges into numerical values
- Removing invalid records
- Encoding categorical variables
- Handling outliers
- Creating derived features

### Feature Engineering

Additional features were created to improve the representation of property characteristics:

- `sqft_per_bhk`
- `bathrooms_per_bhk`

A price-per-square-foot variable was used during exploratory analysis but was excluded from the predictive feature set because it is directly derived from the target price.

## 🤖 Machine Learning Models

Three regression algorithms were evaluated:

1. **Linear Regression**
2. **Decision Tree Regressor**
3. **Random Forest Regressor**

## 📈 Model Performance

| Model | RMSE | MAE | R² |
|---|---:|---:|---:|
| Linear Regression | 66.377 | 31.472 | 0.6459 |
| Decision Tree | 67.973 | 30.047 | 0.6286 |
| Random Forest | **59.498** | **27.197** | **0.7155** |

### Best Performing Model

The **Random Forest Regressor** achieved the best overall performance:

- **RMSE:** 59.498
- **MAE:** 27.197
- **R²:** 0.7155

The model produced the lowest RMSE and MAE while explaining approximately 71.55% of the variance in the target variable.

## 🔍 Feature Importance

The Random Forest model identified the following features as the most influential:

| Rank | Feature | Importance |
|---|---|---:|
| 1 | `total_sqft` | 0.722 |
| 2 | `Location` | 0.091 |
| 3 | `sqft_per_bhk` | 0.087 |
| 4 | `area_type` | 0.031 |
| 5 | `bathrooms` | 0.022 |

The analysis indicates that **total property area** was the dominant feature, followed by location and square footage per BHK.

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook / Google Colab

## 📁 Repository Structure

```text
House-Price-Prediction-Using-Machine-Learning/
│
├── House Price Prediction Using Machine Learning.ipynb
├── README.md
└── .gitignore
