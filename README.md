# 🏡 Robust Regression Engine

A Machine Learning project that predicts **House Prices** using multiple regression algorithms and compares their performance using **R² Score** and **K-Fold Cross-Validation**.

---

# 📌 Project Objective

The objective of this project is to build and compare different regression models for predicting house prices based on property characteristics such as area, bedrooms, bathrooms, property age, location score, and distance from the city.

---

# 📂 Dataset Features

The dataset contains the following features:

| Feature        | Description                               |
| -------------- | ----------------------------------------- |
| property_id    | Unique identifier for each property       |
| area_sqft      | Total area of the property in square feet |
| bedrooms       | Number of bedrooms                        |
| bathrooms      | Number of bathrooms                       |
| sale_date      | Date of property sale                     |
| property_age   | Age of the property                       |
| distance_city  | Distance from the city center             |
| location_score | Location rating score                     |
| house_price    | Target Variable                           |

---

# 🔍 Exploratory Data Analysis (EDA)

The following analyses were performed:

✅ Missing Value Analysis

✅ Duplicate Detection

✅ Descriptive Statistics

✅ Histogram Analysis

✅ Boxplot Analysis

✅ Correlation Heatmap

✅ Scatter Plot Analysis

### Key Findings

* Area Sqft has a strong positive relationship with House Price.
* Bedrooms and Bathrooms positively influence House Price.
* Location Score positively impacts House Price.
* Distance from City shows a negative relationship with House Price.
* Most numerical features exhibit positive skewness.
* Outliers were identified but retained as they may represent genuine observations.

---

# ⚙️ Feature Engineering

The following features were engineered:

### 📅 Sale Year

Extracted from the `sale_date` column.

### 📅 Sale Month

Extracted from the `sale_date` column.

### ⭐ Premium Location

A new feature created using `location_score` to identify highly rated locations.

After feature extraction, the original `sale_date` column was dropped.

---

# 🧹 Data Preprocessing

### Data Cleaning

* Checked missing values
* Checked duplicate records
* Removed unnecessary features
* Verified data types

### Feature Scaling

* RobustScaler was applied to numerical features.
* Scaling was performed after Train-Test Split to avoid data leakage.

---

# 🤖 Machine Learning Models Used

## Linear Models

* Multiple Linear Regression (MLR)
* Lasso Regression
* Ridge Regression

## Tree-Based Models

* Decision Tree Regressor (DTR)
* Random Forest Regressor (RFR)

## Support Vector Regression Models

* Linear SVR
* RBF SVR

---

# 📊 Model Evaluation

Models were evaluated using:

* R² Score
* K-Fold Cross Validation
* Out-of-Bag (OOB) Score (Random Forest)

---

# 📈 Final Model Comparison

| Model                      | Train R² |    Test R² | Average CV R² |
| -------------------------- | -------: | ---------: | ------------: |
| Multiple Linear Regression |   0.9190 |     0.9136 |        0.9184 |
| Lasso Regression           |   0.9190 |     0.9136 |        0.9184 |
| Ridge Regression           |   0.9190 |     0.9136 |        0.9185 |
| Decision Tree Regressor    |   0.8992 |     0.8813 |        0.8772 |
| Random Forest Regressor    |   0.9268 | **0.9167** |        0.9133 |
| Linear SVR                 |   0.8851 |     0.8859 |        0.8740 |
| RBF SVR                    |   0.9119 |     0.9094 |        0.8944 |

---

# 🏆 Best Model

## Random Forest Regressor

Random Forest Regressor achieved the highest Test R² score of **0.9167**, indicating the best predictive performance on unseen data.

Although Ridge Regression achieved a slightly higher Cross-Validation score, the difference was marginal. Therefore, Random Forest Regressor was selected as the final model due to its superior predictive performance.

---

# 📚 Concepts Applied

* Exploratory Data Analysis (EDA)
* Feature Engineering
* Feature Scaling
* Regularization (Lasso & Ridge)
* Decision Trees
* Random Forest
* Support Vector Regression (SVR)
* Cross Validation
* Model Evaluation
* Model Comparison

---

# 🛠️ Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-Learn
* Jupyter Notebook

---

# 🔄 Project Workflow

Dataset Loading

⬇️

Data Understanding

⬇️

Data Cleaning

⬇️

Exploratory Data Analysis (EDA)

⬇️

Feature Engineering

⬇️

Train-Test Split

⬇️

Feature Scaling (RobustScaler)

⬇️

Model Building

⬇️

K-Fold Cross Validation

⬇️

Model Comparison

⬇️

Final Model Selection

---

# 🎯 Conclusion

Seven regression models were developed and compared for house price prediction. Linear models such as Multiple Linear Regression, Lasso Regression, and Ridge Regression demonstrated excellent stability and generalization performance. Random Forest Regressor achieved the highest Test R² score and was selected as the final model for predicting house prices.
