# Titanic Survival Prediction

## Overview
This project analyzes the Titanic dataset to predict passenger survival using two machine learning models: **Logistic Regression** and **Random Forest Classifier**. The workflow includes:
- Exploratory Data Analysis (EDA)
- Data preprocessing
- Model training/evaluation
- Performance comparison

## Dataset
Source: [Kaggle Titanic Dataset](https://www.kaggle.com/c/titanic/data)  
Features used:
- `Pclass`: Passenger class (1=1st, 2=2nd, 3=3rd)
- `Sex`: Gender (male/female)
- `Age`: Passenger age
- `SibSp`: # of siblings/spouses aboard
- `Parch`: # of parents/children aboard
- `Fare`: Ticket price
- `Embarked`: Port of embarkation (C=Cherbourg, Q=Queenstown, S=Southampton)
- `Survived`: Target variable (0=No, 1=Yes)

## Results Summary

| Model               | Accuracy | Precision | Recall | F1-Score |
|---------------------|----------|-----------|--------|----------|
| Logistic Regression | 81.00%   | 0.81      | 0.81   | 0.81     |
| Random Forest       | 82.12%   | 0.82      | 0.82   | 0.82     |


**Best Model**: Random Forest (82.12% accuracy)

## How to Run
   ```bash
   git clone https://github.com/<your-username>/Titanic-Survival-Prediction.git
   pip install -r requirements.txt
   jupyter notebook notebooks/Titanic_Survival_Prediction.ipynb
```

## Dataset Notes
```bash
File: data/titanic.csv
Preparation:
Download from Kaggle
Place raw file in /data directory
No preprocessing needed before running notebook
```

## Key Technical Decisions
```bash
Data Cleaning:
Age: Filled 177 missing values with median
Embarked: Filled 2 missing values with mode (S)
Cabin: Dropped (687/891 missing)
Removed non-predictive columns (PassengerId, Name, Ticket)

Feature Engineering:
Label-encoded categorical features:
Sex: male=1, female=0
Embarked: S=2, C=0, Q=1

Model Selection:
Logistic Regression: Baseline model
Random Forest: 100 trees with max_depth=None

Evaluation Metrics:
Primary: Accuracy
Secondary: Precision/Recall/F1-score
Confusion matrix analysis
```
