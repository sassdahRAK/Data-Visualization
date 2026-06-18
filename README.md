# Logistics Data Analytics & ML Project

A complete data analytics and machine learning pipeline for logistics shipment data using Python, Pandas, SQLite, and Scikit-Learn, organized as presentation-ready Jupyter Notebooks.

## Project Structure

```
project/
├── data/
│   ├── logistics_heavy.csv      # Raw dataset (400K rows)
│   └── final_data.csv           # Cleaned + feature-engineered dataset
│
├── database/
│   └── data.sqlite              # SQLite database (shipments + clean_shipments)
│
├── preprocessing/
│   ├── eda.ipynb                # Database loading + Exploratory Data Analysis
│   └── cleaning.ipynb           # Data cleaning pipeline
│
├── analysis/
│   └── business_logic.ipynb     # SQL business analysis (8 queries)
│
├── model/
│   ├── linear_regression.ipynb  # Linear Regression model
│   └── decision_tree.ipynb      # Decision Tree model
│
└── README.md
```

## Workflow

The project follows this pipeline, demonstrated step-by-step in Jupyter Notebooks:

```
CSV File → SQLite Database → EDA → Data Cleaning → SQL Analysis → ML Models
```

## Presentation Flow

Present notebooks in this order:

1. **preprocessing/eda.ipynb** — Load CSV into SQLite, verify with SQL queries, perform EDA
2. **preprocessing/cleaning.ipynb** — Handle duplicates, missing values, outliers, save clean data
3. **analysis/business_logic.ipynb** — 8 SQL business queries with interpretations
4. **model/linear_regression.ipynb** — Feature engineering + Linear Regression
5. **model/decision_tree.ipynb** — Decision Tree Regressor + model comparison

## Key Features

- **SQLite Integration**: Dataset loaded into SQLite with verification queries
- **EDA**: Missing values, correlations, distributions, outlier detection
- **Data Cleaning**: Robust handling of mixed date formats, currency symbols, invalid values
- **SQL Analysis**: 8 business queries with purpose, SQL, results, and interpretation
- **ML Models**: Linear Regression and Decision Tree for cost prediction
- **Model Comparison**: MAE, RMSE, R² metrics with best model selection

## Requirements

```
pandas
numpy
matplotlib
seaborn
scikit-learn
scipy
nbformat
joblib
```

## Usage

1. Open any notebook in VS Code or Jupyter
2. Run cells sequentially
3. Follow the presentation flow above

## Dataset

- **Rows**: 400,000
- **Columns**: 20 (shipment details, dates, costs, locations)
- **Target**: `total_cost_usd` (regression)
