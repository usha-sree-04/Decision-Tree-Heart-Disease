# Decision Tree Classification – Heart Disease Prediction

## Overview

This project implements a Decision Tree Classification model for predicting heart disease using the Heart Disease Dataset.

The assignment covers data exploration, preprocessing, Decision Tree model building, evaluation, tree-depth experimentation, visualization, and parameter comparison.

## Dataset

**Dataset:** Heart Disease Dataset

The dataset contains 1025 records and 14 columns.

The target variable is:

* `target`

The features include:

* `age`
* `sex`
* `cp`
* `trestbps`
* `chol`
* `fbs`
* `restecg`
* `thalach`
* `exang`
* `oldpeak`
* `slope`
* `ca`
* `thal`

## Assignment Contents

### Part A – Conceptual Questions

* Decision Tree
* Split Criterion
* Gini Impurity vs Entropy
* Overfitting
* `max_depth`

### Part B – Data Exploration

* Dataset shape
* Column names
* First five rows
* Target and feature identification
* Missing values
* Data types

### Part C – Data Preprocessing

* Missing-value checking
* Feature and target separation
* 80:20 train-test split
* `random_state=42`

### Part D – Model Building

* Decision Tree Classifier
* `criterion='gini'`
* Model training
* Test-data prediction

### Part E – Model Evaluation

* Accuracy
* Confusion Matrix
* Classification Report
* Class-wise performance
* Overfitting analysis

### Part F – Tree Depth Experiment

The following values of `max_depth` were compared:

* `max_depth=2`
* `max_depth=5`
* `max_depth=None`

### Part G – Tree Visualization

The best-performing Decision Tree was visualized with:

* Feature names
* Class names
* Decision nodes
* Gini impurity

### Part H – Reflection

The assignment discusses:

* Why Decision Trees are suitable for medical datasets
* Why Decision Trees are easy to interpret
* Why Decision Trees are used in ensemble methods

## Additional Experiments

The following parameters were also compared:

* `criterion='gini'`
* `criterion='entropy'`
* Different `min_samples_leaf` values

## Results

The Decision Tree with `criterion='gini'` achieved approximately **98.54% testing accuracy** on the given train-test split.

The `max_depth` experiment showed that the unrestricted tree (`max_depth=None`) achieved the highest testing accuracy among the tested models.

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

from sklearn.tree import plot_tree

plt.figure(figsize=(25, 15))

plot_tree(
    model3,
    feature_names=X.columns,
    class_names=['0', '1'],
    filled=True,
    rounded=True,
    fontsize=8
)

plt.title("Decision Tree - Heart Disease Prediction")
plt.show()

