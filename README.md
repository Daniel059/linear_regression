# 🏠 Linear Regression: Predicting House Prices by Bedrooms

This project applies **Linear Regression** using Python and Scikit-learn to predict house prices based on **number of bedrooms**.

---

## 📌 Project Overview

This project demonstrates:
- ✅ Predicting house prices based on number of bedrooms
- ✅ Using linear regression with Scikit-learn
- ✅ Evaluating model accuracy using MAE, RMSE, and R² Score
- ✅ Visualizing results with scatter plots and regression lines

---

## 🧰 Technologies Used

- Python 🐍  
- Pandas 📊  
- Matplotlib 📈  
- Scikit-learn 🤖  
- Jupyter Notebook 📓 / Google Colab ☁️  

---

## 🗂️ Project Structure

| File / Folder | Description |
|---------------|-------------|
| `home_price_bedrooms_linear_regression.ipynb` | Main Jupyter notebook |
| `homeprices-m.csv` | Dataset used for training/testing |
| `assets/` | Folder containing screenshots |
| `README.md` | This project overview |

---

The analysis uses the `homeprices-m.csv` dataset, which contains information about house properties, including:
* `area`: Size of the house (square feet)
* `bedrooms`: Number of bedrooms
* `age`: Age of the house
* `price`: Price of the house (target variable)

For this specific project, we focus exclusively on the `bedrooms` and `price` columns.

## 🚀 Project Steps

### 1. Data Loading and Exploration

This step involves loading the dataset and getting a first look at its structure and content.

```python
# Importing necessary Python modules
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_absolute_error, mean_squared_error, r2_score

# Load the dataset
homeprices_m_df = pd.read_csv('homeprices-m.csv')

print("--- Data Loading and Initial Exploration ---")
print("Homeprices-m DataFrame - First 5 rows:")
print(homeprices_m_df.head().to_markdown(index=False, numalign="left", stralign="left"))
print("\nHomeprices-m DataFrame - Column Information:")
print(homeprices_m_df.info())
