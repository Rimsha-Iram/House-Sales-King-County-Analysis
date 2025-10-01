# House Sales in King County, USA 🏡

This project analyzes house sales in King County, USA (including Seattle) to understand the factors that influence house prices and to build predictive models.

## Dataset
The dataset contains house sales between May 2014 and May 2015, with features such as:
- `price` — Sale price of the house
- `bedrooms`, `bathrooms` — Number of rooms
- `sqft_living`, `sqft_lot`, `sqft_above`, `sqft_basement`, `sqft_living15`, `sqft_lot15` — Various area measurements
- `floors` — Number of floors
- `waterfront` — Waterfront view indicator
- `view` — Quality of view
- `condition`, `grade` — House condition and construction grade
- `yr_built`, `yr_renovated` — Year built/renovated
- `zipcode`, `lat`, `long` — Location coordinates

## Objectives
- Explore and clean the dataset
- Perform exploratory data analysis (EDA)
- Identify key features influencing house prices
- Build predictive models:
  - Single-feature linear regression
  - Multiple linear regression
  - Polynomial regression pipeline
  - Ridge regression with regularization

## Key Findings
- Houses with larger living areas, higher grades, or waterfront views have higher prices.
- `sqft_living` is the strongest single predictor (R² ~ 0.49).
- Multiple features improve prediction accuracy.
- Ridge regression with regularization provides a generalizable model with R² ~ 0.66.

## Methodology
1. **Data Cleaning**
   - Dropped irrelevant columns (`id`, `Unnamed: 0`)  
   - Checked basic statistics using `describe()`
2. **Exploratory Data Analysis**
   - Counted unique values of categorical features (`value_counts`)  
   - Identified price outliers using boxplots  
   - Examined feature-price relationships using regression plots
3. **Modeling**
   - Linear regression (single and multiple features)  
   - Polynomial regression with preprocessing pipeline  
   - Ridge regression with training/test split to avoid overfitting
4. **Evaluation**
   - R² was used to measure model performance on training and test data

## Tools & Libraries
- Python 3.x
- pandas, numpy
- matplotlib, seaborn
- scikit-learn (LinearRegression, Ridge, Pipeline, PolynomialFeatures, StandardScaler)
