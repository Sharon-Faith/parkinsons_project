# Parkinson's Disease Detection
#### By **Sharon Faith**

## Overview
Parkinson’s Disease is a debilitating neurodegenerative movement disorder that has no cure, and whose etiology is not well understood. There is currently no definitive test for its diagnosis. It is characterized by the progressive loss of dopaminergic neurons in the substantia nigra of the brain, and the typical motor symptoms often do not appear until a significant proportion of these neurons are lost. This factor coupled with the fact that many of its motor and non-motor symptoms overlap with other disorders make diagnosis difficult, especially in the early stages.

**Objective**: This project’s main aim was to build a classifier that can detect whether a patient has Parkinson’s Disease or not, which could be a useful tool to aid with diagnosis as well as present an opportunity to further explore the biomarkers and other indicators of this complex disorder.

**Metrics**: Evaluation metrics included accuracy, f-1 score, precision, roc-auc, and recall. Recall was the primary metric, and it was optimized for during hyperparameter tuning, as a key aim with diagnosis is to minimize false negatives. 

## Dataset
The dataset is a synthetic dataset for Parkinson’s disease analysis that was obtained from [Kaggle](https://www.kaggle.com/datasets/rabieelkharoua/parkinsons-disease-dataset-analysis). It originally consisted of 2105 observations and 35 columns: 34 predictors and the outcome column. Three columns (an index column, redacted column, and UPDRS column-label leakage) were excluded before using the dataset further, resulting in 31 features and 1 outcome (diagnosis).

## Methodology
Data Cleaning ➡️ EDA and Preprocessing ➡️ Model Training and Evaluation

## Models
* Logistic Regression
* Linear Discriminant Analysis
* Quadratic Discriminant Analysis
* Naive Bayes Classifier
* K-Nearest Neighbors
* Random Forest Classifiers
* Gradient Boosting Classifiers
* XGBoost
* Support Vector Machines

## Results
The best performing model was XGBoost, with a recall of 96.4%, f1 score of 85.42%.

<img width="835" height="793" alt="image" src="https://github.com/user-attachments/assets/96897dca-558a-456b-9074-33f52861267c" />

## Conclusion
The model that performed best on unseen test data was the XGBoost model. Generally, flexible, non-parametric methods worked best on the given dataset. Ensemble tree methods performed the best, and linear methods the worst, which suggested that the decision boundary was complex. 

To improve results:
* **SVM note** - The radial kernel in SVM resulted in a degenerate model when metrics such as recall or precision were directly used for scoring in the grid-search; it benefits from inherently balanced metrics such as f-1. The use of recall but with an adjusted decision threshold or constrained values of gamma and c in the hyperparameter grid could be explored.
* **Generally** - Test expanding hyperparameter search space, different feature selection methods, additional model types such as Neural Networks.


## Run
* Access the Colab notebook [here](https://colab.research.google.com/drive/1-Qxujb_EKyhVm_ewguOxOIVd02RoW5eb?usp=sharing).

## Technologies Used
* Language and Environment: Python, Google Colab (Jupyter notebook)
* Libraries: Pandas, Numpy, Scikit-learn, ISLP, StatsModels, Matplotlib, Seaborn, XGboost

## Support and contact details
Github account: Sharon-Faith

## License
All rights reserved. Copyright (c) {2026} **Sharon Faith**
