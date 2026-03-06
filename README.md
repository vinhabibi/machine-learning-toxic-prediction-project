# Toxic Classification Machine Learning Project

A machine learning project for binary classification of toxic vs. non-toxic samples using ensemble methods.

## Project Overview

This project implements and compares two machine learning classifiers (Random Forest and Gradient Boosting) to predict toxicity classification. The workflow includes data preprocessing, exploratory data analysis, feature selection, model training, hyperparameter tuning, and comprehensive evaluation.

## Dataset

- **Samples:** 171 entries
- **Features:** 1203 features (after removing target)
- **Target:** Binary classification (Toxic/NonToxic)
- **Class Distribution:** 115 NonToxic, 56 Toxic (imbalanced)

## Methodology

### 1. Data Preprocessing
- Verified no missing values or duplicate rows
- Encoded target variable using LabelEncoder

### 2. Feature Selection
- Applied `SelectKBest` with `f_classif` scoring
- Reduced features from 1203 to 50 most relevant features

### 3. Models Implemented
- **Random Forest Classifier**
- **Gradient Boosting Classifier**

### 4. Hyperparameter Tuning
Used `GridSearchCV` with 5-fold cross-validation optimizing for ROC AUC.

#### Random Forest Best Parameters:
- `n_estimators`: 300
- `max_features`: 'sqrt'
- `min_samples_leaf`: 1

#### Gradient Boosting Best Parameters:
- `n_estimators`: 200
- `learning_rate`: 0.01
- `max_depth`: 4

## Results

| Model | Accuracy | ROC AUC | Precision (Toxic) | Recall (Toxic) |
|-------|----------|---------|-------------------|----------------|
| Tuned Random Forest | 0.63 | 0.63 | 0.39 | 0.27 |
| Tuned Gradient Boosting | 0.61 | 0.62 | 0.38 | 0.29 |

## Key Findings

- Tuned Random Forest slightly outperformed Gradient Boosting (ROC AUC: 0.63 vs 0.62)
- Both models struggle with minority class (Toxic) due to class imbalance
- Hyperparameter tuning improved ROC AUC from 0.52 to 0.63 for Random Forest

## Requirements

```
pandas
numpy
matplotlib
scikit-learn
```

## Usage

1. Place your `data.csv` file in the same directory
2. Run the Jupyter notebook `ml_toxic_assignment_adjusted.ipynb`

## Future Improvements

- Address class imbalance using SMOTE or class weights
- Explore additional algorithms (XGBoost, LightGBM)
- Advanced feature engineering
- Ensemble/stacking methods

## Files

- `ml_toxic_assignment_adjusted.ipynb` - Main analysis notebook
- `data.csv` - Dataset (required)
- `README.md` - Project documentation

## License

This project is for educational purposes.
