# 📱 Megaline Plan Classification

Machine learning classification project to recommend Megaline mobile plans based on customer behavior and monthly usage patterns.

## 📌 Context

The mobile operator **Megaline** wants to migrate customers who still use legacy plans to one of its newer plans: **Smart** or **Ultra**.

Historical behavioral data is available for customers who have already switched to these plans.

The objective of this project is to develop a machine learning model capable of analyzing customer usage behavior and recommending the most appropriate plan.

## 🎯 Business Problem

Megaline needs an automated method to classify customers into one of two plans:

- **Smart**
- **Ultra**

The model uses monthly customer behavior such as calls, call duration, text messages, and internet usage to predict which plan is more appropriate.

The project requires a minimum test accuracy of **0.75**.

## 📊 Dataset

The project uses the `users_behavior.csv` dataset containing monthly behavioral information for Megaline customers.

### Features

- `calls` — number of calls
- `minutes` — total call duration in minutes
- `messages` — number of text messages
- `mb_used` — internet traffic used in megabytes

### Target

- `is_ultra` — customer's current plan:
  - `0` — Smart
  - `1` — Ultra

## 🔎 Machine Learning Approach

The project follows the workflow below:

1. Load and inspect the dataset
2. Separate features and target
3. Split the data into training, validation, and test sets
4. Train multiple classification models
5. Experiment with model hyperparameters
6. Compare validation performance
7. Select the strongest model
8. Evaluate the final model on unseen test data
9. Compare performance with a simple baseline
10. Summarize the results and business implications

## 🤖 Model Development

Different classification algorithms and hyperparameter configurations are evaluated to identify the model that provides the strongest predictive performance.

The validation dataset is used for model selection, while the test dataset remains unseen until the final evaluation.

This separation helps reduce the risk of selecting a model that performs well only on the training data.

## 📏 Evaluation Metric

The primary evaluation metric is **accuracy**.

The project requires the final model to achieve:

```text
Accuracy ≥ 0.75
```

on the test dataset.

A baseline comparison is also used to provide context for the predictive performance of the trained model.

## 💡 Business Applications

A successful classification model could help Megaline:

- Recommend plans based on customer behavior
- Support migration from legacy plans
- Personalize customer communication
- Improve targeting of plan upgrade campaigns
- Automate part of the plan recommendation process

## ⚠️ Limitations

The dataset contains a limited number of behavioral variables and represents aggregated monthly usage.

Real-world plan recommendation systems could also benefit from additional information such as customer demographics, pricing sensitivity, historical plan changes, billing information, customer satisfaction, and profitability.

The model developed here should therefore be interpreted as a machine learning case study rather than a production recommendation system.

## 🛠️ Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook
- Machine Learning
- Classification
- Hyperparameter Tuning
- Model Evaluation

## 📁 Repository Structure

```text
megaline-plan-classification/
│
├── README.md
│
├── data/
│   └── users_behavior.csv
│
└── notebook/
    └── megaline_plan_classification.ipynb
```

## 📌 Project Goal

This project demonstrates an end-to-end supervised machine learning workflow, including data splitting, model comparison, hyperparameter tuning, validation, and final evaluation on unseen test data.
