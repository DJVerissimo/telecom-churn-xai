Telecom Churn Prediction with XAI
=================================

This repository contains the code and datasets used in the experimental part of an MSc thesis on customer churn prediction in telecommunications.

The work compares machine learning models and ensemble strategies on two public telecom churn datasets. The experiments focus on recall-oriented churn detection, class imbalance, model comparison, and explainability with SHAP.

Repository contents
-------------------

- `telcotesesemo6GPcomAP.ipynb`: experiment notebook for the IBM Telco Customer Churn dataset.
- `c2cclsemo6GPcomAP.ipynb`: experiment notebook for the Cell2Cell dataset.
- `Cópia de WA_Fn-UseC_-Telco-Customer-Churn.csv`: IBM Telco Customer Churn dataset used by the Telco notebook.
- `cell2celltrain.csv`: Cell2Cell dataset used by the C2C notebook.

Methods
-------

The notebooks evaluate five base classifiers:

- Logistic Regression
- Random Forest
- XGBoost
- LightGBM
- CatBoost

They also evaluate four ensemble strategies:

- Hard Voting
- Soft Voting
- Weighted Average
- Stacking

The main evaluation metric is the F2-score, because the study gives more importance to recall than precision. Accuracy, precision, recall, ROC-AUC, and Average Precision are also reported to give a broader view of model behavior.

Explainability
--------------

SHAP is used to interpret the results in two ways:

- feature-level importance for the base models;
- ensemble-level contribution analysis, showing how much each base model contributes to the ensemble predictions.

How to run
----------

Open the notebooks with Jupyter Notebook, JupyterLab, VS Code, or a compatible notebook environment.

The CSV files should remain in the same folder as the notebooks unless the file paths inside the notebooks are updated.

Main Python packages used by the notebooks include:

- pandas
- numpy
- scikit-learn
- imbalanced-learn
- xgboost
- lightgbm
- catboost
- optuna
- shap
- matplotlib
- seaborn

Notes
-----

The repository is intended to support reproducibility of the thesis experiments. The notebooks include saved outputs from the final experimental runs.
