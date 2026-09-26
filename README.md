# Burnout Risk Prediction

A machine learning project that predicts **Burnout Risk** as a binary classification problem using a Work Productivity dataset.

The project explores data preprocessing, feature selection, dimensionality reduction, machine learning model comparison, and hyperparameter tuning.

---

## Project Overview

The goal of this project is to build machine learning models capable of predicting whether an individual is at risk of burnout based on work productivity-related features.

The workflow includes:

- Data preprocessing
- Exploratory data analysis
- Feature selection
- Dimensionality reduction
- Machine learning model comparison
- Hyperparameter tuning
- Performance evaluation

---

## Dataset

**Dataset:** Work Productivity Dataset

**Target:** Burnout Risk

The target variable is treated as a **binary classification problem**.

The dataset contains work and productivity-related features that are used to predict burnout risk.

---

## Data Preprocessing

Several preprocessing steps were performed before training the models.

### Data Cleaning

- Checked for missing/null values
- Checked for duplicate records
- Encoded categorical variables
- Removed outliers using the IQR method
- Scaled numerical features

### Visualization

Boxplots were used to visualize the distribution of features and identify potential outliers.

---

## Dimension Reduction & Feature Selection

Different techniques were explored to reduce the number of features and identify useful predictors.

The techniques included:

- Correlation Matrix
- Variance Threshold
- Chi-Square Feature Selection
- ANOVA F-test (`f_classif`)
- Principal Component Analysis (PCA)

A PCA scree plot was also used to examine the explained variance of the principal components.

---

## Machine Learning Models

Five model configurations were tested:

1. Logistic Regression
2. Decision Tree
3. Random Forest
4. Support Vector Classifier (SVC)
5. PCA + Logistic Regression

The models were evaluated both **before and after dimension reduction** to investigate how reducing the feature space affected model performance.


## Hyperparameter Tuning

After dimension reduction, hyperparameter tuning was performed using **GridSearchCV**.

### Configuration

- GridSearchCV
- 5-fold cross-validation
- Hyperparameter search across the tested models

The tuning process was used to identify suitable hyperparameter combinations and improve or validate model performance.

---

## Results

The experiments showed that dimension reduction **improved or maintained accuracy across the tested models** in this project.

The final model results are presented using the evaluation metrics generated during the experiments.

### Evaluation

The models can be evaluated using metrics such as:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

---

## Machine Learning Workflow

```text
Work Productivity Dataset
          ↓
     Data Cleaning
          ↓
   Null & Duplicate Check
          ↓
       Encoding
          ↓
    IQR Outlier Removal
          ↓
        Scaling
          ↓
 Feature Selection / Reduction
          ↓
 ┌────────┼────────┬────────┐
 ↓        ↓        ↓        ↓
Variance  Chi²   F-test    PCA
Threshold
          ↓
    Model Comparison
          ↓
   Before vs After
          ↓
   Hyperparameter Tuning
          ↓
      GridSearchCV
          ↓
       5-Fold CV
          ↓
    Final Evaluation
