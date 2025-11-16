# King County House Sales Analysis & Price Prediction

This project analyzes house sales data from King County, Washington (May 2014 – May 2015) to explore trends and build predictive models for house prices using regression techniques.

## About the Dataset

The dataset contains detailed information on house sales in King County, including Seattle.  

- **Source:** [Kaggle](https://www.kaggle.com/harlfoxem/housesalesprediction)  
- **Data File:** `kc_house_data_NaN.csv` (the script downloads it as `housing.csv`)  

## Project Structure

- **`House_Sales_in_King_Count_USA.ipynb`**: Main script containing the full analysis.  
  - Designed to run in Pyodide-enabled environments (e.g., IBM Skills Network Labs on Coursera).  
  - Handles package installation and dataset download automatically.  

## Analysis & Modeling Workflow

### 1. Data Import & Cleaning
- Downloads the dataset.
- Removes irrelevant columns (`id`, `Unnamed: 0`).  
- Handles missing values using `dropna()`.  

### 2. Exploratory Data Analysis (EDA)
- Examines data types (`.dtypes`) and statistical summaries (`.describe()`).  
- Counts unique values for features like `floors`.  
- Uses **Seaborn** for visualization:  
  - Boxplots for price outliers with/without waterfront views.  
  - Regression plots for correlation between `sqft_above` and `price`.  

### 3. Regression Modeling
- **Model 1 (Simple Linear Regression):** Predicts price using `sqft_living`.  
- **Model 2 (Multiple Linear Regression):** Uses 11 selected features.  
- **Model 3 (Pipeline):** Combines `StandardScaler`, `PolynomialFeatures`, and `LinearRegression`.  

### 4. Model Evaluation & Refinement
- Splits dataset into **training (85%)** and **testing (15%)** sets.  
- **Model 4 (Ridge Regression):** Ridge model with `alpha=0.1`, evaluated with R².  
- **Model 5 (Polynomial Ridge Regression):** 2nd-degree polynomial transformation with Ridge regression, evaluated on transformed test data.  

## Requirements
- Python 3.x  
- Libraries: `pandas`, `numpy`, `seaborn`, `scikit-learn`, `matplotlib`  

## How to Run
use
House_Sales_in_King_Count_USA.ipynb
