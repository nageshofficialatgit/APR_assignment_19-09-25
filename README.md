# APR_assignment_19-09-25

# Heart Disease Classification using SVM

This repository implements a binary Support Vector Machine (SVM) model to predict the presence of heart disease using the CSE422_BRAC dataset from BRAC University.

## Dataset

- **Source**: Kaggle – Heart Disease Classification Dataset (CSE422_BRAC)
- **Format**: CSV (`heart disease classification dataset.csv`)
- **Size**: 13.93 KB, 303 samples
- **Features**: 15 clinical variables (age, gender, chest pain type, resting blood pressure, cholesterol, maximum heart rate, etc.)
- **Target**: Binary label (0 = No Disease, 1 = Disease Present)


## Notebook Overview

`Heart_Disease_SVM_Classification.ipynb` includes:

1. **Data Loading \& Exploration**
    - Load CSV, inspect structure, check missing values, duplicates, and class balance.
2. **Exploratory Data Analysis**
    - Visualize target distribution, age by disease status, feature correlations, and distributions of key features.
3. **Data Preprocessing**
    - Handle categorical variables, stratified train-test split, feature scaling (StandardScaler), and feature selection (SelectKBest).
4. **SVM Model Training**
    - Train four SVM kernels (Linear, RBF, Polynomial, Sigmoid) on selected features.
    - Compute accuracy, F1-score, ROC-AUC for each model.
5. **Hyperparameter Optimization**
    - Grid search with 5-fold CV on the best kernel using weighted F1-score.
    - Include class weighting to address any class imbalance.
6. **Comprehensive Evaluation**
    - Classification report, confusion matrix, sensitivity, specificity, precision, and F1-score.
    - ROC and Precision-Recall curves, prediction confidence analysis, and error pattern review.
7. **Visualization Dashboard**
    - Model comparison charts, ROC/PR curves, feature importance, and class-wise performance.


## Usage

1. Install dependencies:
`pip install pandas numpy scikit-learn matplotlib seaborn joblib`
2. Place `heart disease classification dataset.csv` in the working directory.
3. Run the notebook:
`jupyter notebook Heart_Disease_SVM_Classification.ipynb`


## Expected Outcomes

- High diagnostic performance with accuracy typically above 85%.
- Sensitivity and specificity optimized for clinical screening.
- Feature importance highlighting key clinical predictors.

