# Exploratory Data Analysis & Regression on Car Prices

## Project Overview
This project aims to predict car selling prices using a large dataset of car characteristics. Through data cleaning, exploratory data analysis (EDA), and regression modeling, we uncover key factors that influence selling price and build predictive models for accurate estimation.

**Dataset:** `car_prices.csv`  
**Size:** 558,837 entries  
**Target:** `sellingprice`  

## Objectives
- Clean and preprocess raw car data.
- Explore relationships between car features and selling price.
- Build and compare regression models to predict selling price.
- Identify important features driving price predictions.

## Methodology

### Data Cleaning & Preparation
- Converted sale date to datetime format.
- Dropped duplicates and rows with missing target values.
- Filled missing numeric values with the median and categorical values with the mode.
- Derived new feature: `car_age = 2025 - year`.
- Dropped irrelevant columns: `vin`, `saledate`.

### Exploratory Data Analysis (EDA)
- Visualized selling price distribution with histogram.
- Plotted correlations between numeric features.
- Examined top 10 car makes and price distributions by make.
- Investigated relationships between odometer, car age, and selling price.

### Modeling
- **Features:** Numeric (`condition`, `odometer`, `mmr`, `car_age`) and categorical (`make`, `model`, `trim`, `body`, `transmission`, `color`, `interior`, `seller`, `state`).
- **Target:** `sellingprice`
- Preprocessed data using StandardScaler for numeric features and OneHotEncoder for categorical features.
- Split data into train (80%) and test (20%) sets.

#### Regression Models
- Linear Regression
- Ridge Regression
- Lasso Regression
- Random Forest Regression

### Evaluation Metrics
- R² score
- Root Mean Squared Error (RMSE)

## Results

| Model               | R²      | RMSE    |
|--------------------|---------|---------|
| Linear Regression  | 0.9706  | 1673.75 |
| Ridge Regression   | 0.9711  | 1661.65 |
| Lasso Regression   | 0.9707  | 1673.04 |
| Random Forest      | 0.9720  | 1633.83 |

**Key Observations:**
- Random Forest performed the best with the highest R² and lowest RMSE.
- Features like car age, odometer, and make were the most important drivers of selling price.

## Libraries & Tools
- **Python:** pandas, numpy, matplotlib, seaborn, scikit-learn  
- **Tools:** Jupyter Notebook, Git/GitHub  

## Key Takeaways
- Data cleaning and proper preprocessing are crucial for high-performance models.
- Both linear and ensemble methods can achieve strong performance on large datasets.
- Random Forest regression is effective in capturing complex relationships in car price data.
- Feature importance analysis provides actionable insights into which factors most influence car pricing.

## Future Work
- Experiment with gradient boosting methods (XGBoost, LightGBM) for potentially higher accuracy.
- Incorporate external factors like regional demand and seasonality.
- Explore deep learning models for large-scale predictions.

## Author
**Madelyn McNamara**  
Data Science + Information Science Student @ UIUC | Computer Science Minor  
📧 mnm12@illinois.edu | 🌐 [GitHub](https://github.com/maddymcnamara) | 💼 [LinkedIn](https://www.linkedin.com/in/maddymac)  

---
