# File Structure
```. ```<br>
```├── data ```<br>
```│   ├── final_data.csv ```<br>
```│   └── logistics_heavy.csv ```<br>
```├── database ```<br>
```│   └── data.sqlite ```<br>
```├── model``` <br>
```│   ├── decission_tree.ipynb ```<br>
```│   └── logistic_regression.ipynb ```<br>
```├── preprocessing ```<br>
```│   ├── business_logic.ipynb ``` <br>
```│   └── cleaning.ipynb ```<br>
```├── README.md ```<br>
```└── report ```<br>


# Team Role and Responsibility

## Project: Logistic Regression & Decision Tree Prediction Model

This document describes the responsibility of each team member during the data preprocessing and feature engineering phase.

---

# Team Members

## 1. Virak - Feature Engineer

### Role
Feature Engineer is responsible for transforming cleaned data into meaningful features that improve machine learning model performance.

### Responsibilities
- Analyze cleaned dataset and identify useful features.
- Select important columns for model training.
- Create new features based on existing data.
- Transform raw information into a machine-learning-friendly format.
- Prepare the final dataset for model training.

### Deliverable
`data/final_data.csv`

---

## 2. Naly - Numerical Data Format & Missing Data Analyst

### Role
Responsible for checking data quality related to numerical values and missing information.

### Responsibilities
- Analyze numerical columns.
- Identify incorrect data formats.
- Detect missing values.
- Decide how missing values should be handled.
- Ensure numerical features are ready for machine learning.

### Main Tasks
- Check data types.
- Handle missing values.
- Validate numerical columns.

---

## 3. David - Duplicate Data Handler

### Role
Responsible for detecting and removing duplicate records from the dataset.

### Responsibilities
- Identify duplicated rows.
- Analyze duplicate patterns.
- Remove unnecessary duplicated data.
- Ensure each record is unique.

### Main Tasks
```python
df.duplicated().sum()
df.drop_duplicates()
```

---

## 4. Menghong - Date and Time Handler

### Role
Responsible for processing date and time-related features.

### Responsibilities
- Convert date columns into correct format.
- Extract useful information from dates.
- Prepare datetime features for machine learning.

### Main Tasks
```python
pd.to_datetime(df["date"])
```

Extract:
- Year
- Month
- Day
- Weekday

---

## 5. Tong - Business Logic Developer

### Role
Responsible for applying real-world business rules and domain knowledge into the dataset.

### Responsibilities
- Understand business meaning of data.
- Create business-based features.
- Define rules that improve prediction quality.

### Examples
- Customer categories.
- Risk levels.
- Performance indicators.
- Calculated metrics.

Deliverable:
`business_logic.ipynb`

---

# Team Workflow

```
Raw Dataset
     |
     v
Naly
(Numerical Format + Missing Data)
     |
     v
David
(Remove Duplicate Data)
     |
     v
Menghong
(Date & Time Processing)
     |
     v
Tong
(Business Logic)
     |
     v
Virak
(Feature Engineering)
     |
     v
Final Clean Dataset
     |
     v
Machine Learning Model
(Logistic Regression + Decision Tree)
```

---

# Final Output Structure

```
data/
├── logistics_heavy.csv
└── final_data.csv

preprocessing/
├── cleaning.ipynb
├── business_logic.ipynb
└── feature_engineering.ipynb
```

# Project Goal

The goal of the preprocessing team is to convert raw data into a high-quality dataset that allows machine learning models to achieve better prediction performance.
