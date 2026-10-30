
# Telecom Customer Churn Prediction

## 1. Project Overview

This project analyzes telecom customer data to understand customer churn and build machine learning classification models to predict whether a customer is likely to leave a telecom service.

The project covers data cleaning, exploratory data analysis (EDA), feature engineering, data preprocessing, model training, and model evaluation.

## 2. Objectives

- Understand customer churn patterns.
- Identify customer segments associated with higher churn.
- Explore the relationship between customer characteristics and churn.
- Train and compare multiple machine learning classification models.
- Evaluate model performance using classification metrics.

## 3. Dataset

**Dataset:** IBM Telco Customer Churn

**Source:** [Kaggle - Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

- Total records: 7,043
- Total original columns: 21
- Target variable: `Churn`
- Target classes: Yes and No

Download the CSV dataset and place it in:

`data/raw/WA_Fn-UseC_-Telco-Customer-Churn.csv`

## 4. Technologies and Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook
- VS Code
- Git and GitHub

## 5. Project Structure

```text
CA2_Telco_Churn_Project/
│
├── data/
│   ├── raw/
│   └── processed/
│       └── telco_churn_cleaned.csv
│
├── notebooks/
│   └── CA2_Telco_Churn_Prediction.ipynb
│
├── reports/
│
├── results/
│   ├── figures/
│   └── model_comparison.csv
│
├── .gitignore
├── README.md
└── requirements.txt
```

## 6. Exploratory Data Analysis

The project investigates:

1. Overall customer churn distribution.
2. Churn by contract type.
3. Customer tenure by churn status.
4. Monthly and total charges by churn status.
5. Churn by payment method.
6. Churn by internet service.

### Key EDA Findings

- Overall customer churn rate: 26.54%.
- Month-to-month contract churn rate: 42.71%.
- Electronic-check payment churn rate: 45.29%.
- Fiber-optic customer churn rate: 41.89%.

These are observed associations and do not establish causation.

## 7. Machine Learning Models

Five classification algorithms were trained and evaluated:

1. Logistic Regression
2. Decision Tree
3. Support Vector Machine (SVM)
4. K-Nearest Neighbors (KNN)
5. Gaussian Naive Bayes

Preprocessing was performed explicitly without using Scikit-learn Pipeline. Numerical features were scaled using StandardScaler, while categorical features were encoded using Pandas `get_dummies()`.

The dataset was divided into 80% training data and 20% testing data.

## 8. Model Evaluation Results

| Model                | Accuracy | Precision | Recall | F1-score | ROC-AUC |
| -------------------- | -------: | --------: | -----: | -------: | ------: |
| Logistic Regression  |   0.7402 |    0.5067 | 0.8048 |   0.6219 |  0.8452 |
| Decision Tree        |   0.7417 |    0.5085 | 0.8021 |   0.6224 |  0.8343 |
| SVM                  |   0.7502 |    0.5193 | 0.7914 |   0.6271 |  0.8304 |
| Gaussian Naive Bayes |   0.6749 |    0.4420 | 0.8556 |   0.5829 |  0.8073 |
| KNN                  |   0.7700 |    0.5718 | 0.5321 |   0.5512 |  0.8001 |

### Best Results

- Highest accuracy: KNN (77.00%).
- Highest precision: KNN (57.18%).
- Highest recall: Gaussian Naive Bayes (85.56%).
- Highest F1-score: SVM (62.71%).
- Highest ROC-AUC: Logistic Regression (0.8452).
- Lowest log loss: SVM (0.4397).

No single model performed best across all metrics.

## 9. Model Evaluation Visualizations

The project includes:

- Model performance comparison chart.
- Confusion matrices for all five models.
- ROC curve comparison.

Generated visualizations are stored in `results/figures/`.

## 10. How to Run the Project

### Step 1: Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

### Step 2: Open the project folder

```bash
cd CA2_Telco_Churn_Project
```

### Step 3: Install dependencies

```bash
pip install -r requirements.txt
```

### Step 4: Add the dataset

Place the Kaggle CSV file in `data/raw/` using the expected filename.

### Step 5: Open the notebook

Open `notebooks/CA2_Telco_Churn_Prediction.ipynb` in VS Code or Jupyter Notebook.

Run the notebook cells from top to bottom.

## 11. Limitations

- Evaluation uses one train-test split.
- Results may differ on new customer data.
- Observed associations do not prove causation.
- Further validation is required before real-world deployment.

## 12. Conclusion

This project demonstrates how exploratory data analysis and machine learning can be used to investigate telecom customer churn.

The analysis identified several customer segments associated with higher churn. Five classification models were compared using multiple evaluation metrics.

The results provide a foundation for further investigation into customer retention strategies and predictive analytics.

---

**Project Category:** Data Science and Machine Learning
**Language:** Python
**Status:** Completed
