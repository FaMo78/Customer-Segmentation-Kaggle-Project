# 🎯 Customer Risk Segmentation & Default Prediction — A Kaggle-Based Simulation for Thesis Preparation

This repository presents a **Kaggle-based simulation** developed to support and prepare for my academic thesis on credit risk modeling. The project mimics real-world banking scenarios by combining **advanced clustering techniques** and **predictive modeling** to classify loan applicants and predict their default risk.

---

## 📁 Files Included
- `kmeans_kaggle.html` → Implementation of **K-Means and hybrid Genetic Algorithm–K-Means clustering** for customer segmentation based on financial behavior.
- `Otherclustering_Ranking_Predict_kaggle.html` → **Hierarchical clustering**, risk ranking, and **default prediction using XGBoost and Logistic Regression**.
- `train.csv`, `test.csv` → Dataset with features such as loan history, overdue amounts, payment status, income, and employment duration.

> 💡 **Tip**: Open `.html` files directly in your browser to view full code, visualizations, and model outputs — no installation required.

---

## 🎓 Project Overview

This simulation was designed to mirror the methodology of my thesis research, focusing on:
1. **Segmenting loan applicants** into risk-based groups using clustering algorithms.
2. **Predicting the probability of default** for each segment using machine learning models.

The framework follows a hybrid approach:
- **Unsupervised learning** for customer segmentation
- **Supervised learning** for default risk prediction

It serves as a practical foundation for my thesis on **"Credit Risk Management for Enhancing Facilities Allocation to Bank Customers"**.

---

### 🔍 Methodology & Key Techniques

#### 🧩 1. **Weight of Evidence (WOE) Transformation**
Before modeling, **categorical and binned numerical features** were transformed using **Weight of Evidence (WOE)**:
- WOE measures the **predictive power** of a feature by comparing the distribution of "good" (non-default) vs. "bad" (default) customers within each category.
- Formula:  
  $$
  \text{WOE} = \ln\left(\frac{\% \text{ of non-defaults in group}}{\% \text{ of defaults in group}}\right)
  $$

All features were WOE-encoded before being used in clustering and prediction phases.

#### 🧠 2. **Customer Segmentation**
- **K-Means Clustering**: Initial segmentation based on risk-related features.
- **Hybrid GA-KMeans**: A genetic algorithm was used to **optimize the initial centroids** of K-Means, reducing sensitivity to initialization and avoiding local optima.
- **Validation**: Elbow method, and cluster stability analysis.

#### 📉 3. **Default Risk Prediction**
After segmentation, each cluster’s risk profile was analyzed, and a predictive model was trained:
- **Target Variable**: Loan default (binary: 0 = repaid, 1 = defaulted)
- **Models Used**:
  - **Logistic Regression** 
  - **XGBoost** 
- **Evaluation Metrics**: AUC-ROC, Precision, Recall, F1-Score

---

### 🧠 Key Findings
Using **Logistic Regression (WOE-based)** and **XGBoost**, the model successfully predicted the **default probability** for each segment, enabling:
- Better loan approval decisions
- Reduced credit risk exposure
- Improved resource allocation

---

## 🚀 How to Use
1. Clone the repository:
   ```bash
   https://github.com/FaMo78/Segmentation-Kaggle-Project
