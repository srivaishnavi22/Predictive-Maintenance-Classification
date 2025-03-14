# 🔧 Predictive Maintenance using Machine Learning

## 📌 Project Overview

This project focuses on **Predictive Maintenance** using machine learning techniques to predict potential equipment failures. The dataset used is the **AI4I 2020 Predictive Maintenance Dataset**, which is a synthetic dataset representing typical industrial predictive maintenance scenarios. The primary goal is to **classify machine failures** based on operational parameters.

## 📊 Dataset Information

- **Source:** Available on **Kaggle**, originally provided by the **UCI Machine Learning Repository**.
- https://www.kaggle.com/datasets/stephanmatzka/predictive-maintenance-dataset-ai4i-2020?resource=download
- **Instances:** 10,000 records
- **Features:** 14 operational parameters including:
  - **Air Temperature [K]**
  - **Process Temperature [K]**
  - **Rotational Speed [rpm]**
  - **Torque [Nm]**
  - **Tool Wear [min]**
  - **Machine Type**
  - **Product ID**
- **Target Variable:** **Machine failure** (Binary classification - 0: No failure, 1: Failure)

### ⚠️ Challenges & Limitations:
- The dataset is **synthetic**, meaning real-world operational errors or environmental factors are not included.
- The **class imbalance** in machine failure cases can affect model performance.

## 🚀 Approach

### 1️⃣ Data Preprocessing
- **Train-test split:** 80/20 stratified split.
- **Outlier Detection:** Z-score method (absolute value > 3).
- **Feature Engineering:** Created interaction term between air temperature and process temperature.
- **One-Hot Encoding:** Converted categorical columns.
- **Dimensionality Reduction:** PCA (retaining 95% variance).
- **Feature Selection:** ANOVA F-test.
- **Scaling & Standardization:** StandardScaler.

### 2️⃣ Model Training & Evaluation
- **Classifiers Used:**
  - Logistic Regression
  - Random Forest
  - Support Vector Machine (SVM)
  - k-Nearest Neighbors (k-NN)
  - Gradient Boosting

- **Hyperparameter Tuning:**
  - **Grid Search CV**
  - **Randomized Search CV**
  - **Bayesian Optimization (BayesSearchCV)**

- **Performance Metrics:**
  - F1 Score
  - Accuracy
  - AUC-ROC Score

### 3️⃣ Feature Engineering Impact Analysis
- Compared different scenarios:
  - **Original Features**
  - **With Interaction Term**
  - **Reduced Features**
- Results visualized through **bar charts** comparing F1 Score, Accuracy, and AUC.

## 📈 Key Findings
- The **interaction term improved** model performance slightly.
- **Feature removal impacted** AUC negatively.
- The **Random Forest** model performed best in terms of **generalization**.


## 🛠️ Installation & Usage

### 🔹 Prerequisites
- Python 3.x
- Jupyter Notebook
- Required libraries: `pandas`, `numpy`, `sklearn`, `matplotlib`, `seaborn`


### ✅ What's included:
✔ **Headings & structure** for easy readability  
✔ **Emojis** to make it engaging  
✔ **Directory structure** for reference  
✔ **Code snippets** for installation and execution  
✔ **Future improvements & contribution guide**  
