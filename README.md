# 🏦 Consumer Complaint Prediction: Logistic Regression vs. Random Forest

This project compares the performance of **Logistic Regression** (linear model) and **Random Forest Classifier** (tree-based model) to predict consumer complaint outcomes. The dataset is sourced from the [Consumer Financial Protection Bureau (CFPB)](https://www.consumerfinance.gov/data-research/consumer-complaints/) and includes detailed complaint data. The analysis explores the impact of data preprocessing, feature selection, and class imbalance on model performance.

---

## 📋 Table of Contents
- [Project Overview](#project-overview)
- [Data Insights](#data-insights)
- [Preprocessing & Methodology](#preprocessing--methodology)
- [Model Evaluation](#model-evaluation)
- [Visualizations](#visualizations)
- [Conclusion](#conclusion)
- [How to Run the Code](#how-to-run-the-code)
- [Dependencies](#dependencies)

---

## 📜 Project Overview
Understanding and predicting consumer complaint outcomes is crucial for businesses and regulators. This project evaluates:
- The **effectiveness of feature selection** in handling high-dimensional data.
- The impact of **class imbalance solutions** on model fairness and accuracy.
- Comparative performance between **Logistic Regression** (linear) and **Random Forest Classifier** (non-linear).

---

## 📊 Data Insights
The data was sourced from the [CFPB Consumer Complaint Database](https://www.consumerfinance.gov/data-research/consumer-complaints/). Key features include:
- **Categorical:** Company Name, Product, Issue
- **Boolean:** Consumer Consent Provided, Consumer Disputed
- **Numerical:** Complaint ID (used for indexing)

Key statistics:
- Class imbalance was prominent, with outcomes like "Closed with Explanation" overrepresented.
- Non-linear relationships between variables indicated the need for tree-based models.

---

## 🛠 Preprocessing & Methodology
### **Preprocessing Steps**
1. **Encoding Techniques**:
   - **Binary Encoding**: Applied to boolean features like "Consumer Consent Provided."
   - **Frequency Encoding**: Used for high-cardinality categorical features like "Company Name."
   - **One-Hot Encoding**: Applied to unordered categorical features like "Submitted Via."
2. **Feature Selection**:
   - **LASSO Regularization**: Reduced dimensionality by penalizing less important features.
3. **Class Imbalance Handling**:
   - **Random Undersampling**: Balanced the dataset to ensure fair model evaluation.

### **Models Implemented**
1. **Logistic Regression**:
   - Baseline linear model.
   - Applied **Elastic Net Regularization** to balance bias and variance.
2. **Random Forest Classifier**:
   - Tree-based ensemble model.
   - Handles non-linear relationships effectively.

---

## 📈 Model Evaluation
### Metrics Used
1. **Accuracy**: Overall correctness of predictions.
2. **F1 Score**: Balance between precision and recall.
3. **ROC AUC**: Ability to distinguish between classes.
4. **Weighted Precision & Recall**: Accounts for class imbalance.

### Performance Highlights
| Metric                    | Logistic Regression | Random Forest |
|---------------------------|---------------------|---------------|
| **Accuracy**              | 0.24               | 0.52          |
| **F1 Score**              | 0.22               | 0.57          |
| **ROC AUC**               | 0.71               | 0.89          |
| **Weighted Precision**    | 0.57               | 0.71          |
| **Weighted Recall**       | 0.24               | 0.52          |

---

## 📊 Visualizations
### **Key Visuals**
1. **Confusion Matrix**:
   - Random Forest displayed fewer misclassifications than Logistic Regression.
2. **Feature Importance**:
   - Random Forest heavily relied on the "Company" feature, while Logistic Regression distributed importance more evenly.
3. **Grouped Bar Chart**:
   - Compared key performance metrics, showcasing Random Forest’s superior performance.
4. **Spider Chart**:
   - Holistic visualization of all metrics, demonstrating Random Forest’s dominance.

| Logistic Regression | Random Forest Classifier |
|----------------------|--------------------------|
| ![Logistic ROC](path/to/logistic-roc.png) | ![Random Forest ROC](path/to/rf-roc.png) |

---

## 🧐 Conclusion
- **Random Forest Classifier** is better suited for this dataset, as it captures complex non-linear relationships that Logistic Regression struggles with.
- Addressing **class imbalance** and **feature selection** was crucial for improving fairness and model interpretability.
- Random Forest consistently outperformed Logistic Regression across all key metrics.

---

## 💻 How to Run the Code
1. **Clone the repository**:
   ```bash
   git clone https://github.com/samarthsingh1/data_insights.git
