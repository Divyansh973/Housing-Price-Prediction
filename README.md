# House Price Prediction

## Project Overview

This project uses machine learning to predict house prices from housing-related features. The project is implemented in Python using the King County housing dataset provided in `Housing.csv`.

The notebook performs exploratory data analysis, prepares the data for machine learning, trains two regression models, compares their performance, and analyzes important features.

## Dataset

The dataset contains **21,613 house records** with information such as:

- Number of bedrooms and bathrooms
- Living area and lot size
- Number of floors
- Waterfront status
- House view and condition
- Construction grade
- Year built and year renovated
- Location information such as latitude, longitude, and ZIP code
- Sale date
- House price

The target variable is:

`price`

The `id` column is excluded from model training because it is an identifier rather than a meaningful predictive feature.

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Machine Learning Models

Two supervised regression models are used:

### 1. Linear Regression

Linear Regression is used as a simple baseline model for predicting house prices.

### 2. Decision Tree Regression

A Decision Tree Regressor is used to model nonlinear relationships between the house features and price.

The tree uses a maximum depth of 5 to keep the model relatively simple.

## Data Preprocessing

The project includes the following preprocessing steps:

- Loading the dataset using Pandas
- Processing the `date` column
- Extracting sale year and sale month
- Removing the original date column
- Removing the `id` column
- Separating features (`X`) and target (`y`)
- Converting features to numeric values
- Handling missing values using median imputation
- Splitting the data into training and testing sets

The dataset is split into **90% training data and 10% testing data**.

## Exploratory Data Analysis

Several visualizations are used to understand the dataset and relationships between variables, including:

- Distribution of bedrooms
- Geographic distribution of houses
- Living area vs. price
- Bedrooms vs. price
- Waterfront status vs. price
- Distribution of floors
- Condition vs. price

## Model Evaluation

The models are evaluated using three common regression metrics:

### Mean Absolute Error (MAE)

Measures the average absolute difference between predicted and actual prices.

### Root Mean Squared Error (RMSE)

Measures the square root of the average squared prediction error. Larger errors receive greater weight.

### R² Score

Measures how much of the variation in house prices is explained by the model.

The performance of Linear Regression and Decision Tree Regression is compared using these metrics.

## Additional Analysis

The project also includes:

- An actual-vs-predicted price visualization for the Decision Tree model
- Decision Tree feature importance analysis
- Principal Component Analysis (PCA) for exploratory dimensionality analysis

## Project Structure

```text
House-Price-Prediction/
│
├── Housing.csv
├── Housing_house_price_prediction.ipynb
└── README.md
```

## How to Run

1. Install the required Python libraries:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter
```

2. Place `Housing.csv` in the same directory as the notebook.

3. Open the notebook:

```bash
jupyter notebook Housing_house_price_prediction.ipynb
```

4. Run the notebook cells to reproduce the analysis and results.

## Project Outcome

The project demonstrates a complete beginner-level machine learning workflow:

**Data → Exploratory Data Analysis → Preprocessing → Train/Test Split → Model Training → Prediction → Evaluation → Feature Analysis**

It provides practical experience with supervised regression, model comparison, data visualization, and basic dimensionality analysis.
