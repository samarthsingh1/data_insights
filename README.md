# Project: Comparison of Logistic Regression and Random Forest Classifier

This project involves comparing the performance of two machine learning models—**Logistic Regression** (a linear method) and **Random Forest Classifier** (a tree-based method)—on a classification dataset. The objective is to determine which model is better suited for the data, analyze the impact of feature selection and scaling, and evaluate key performance metrics for each model.

## Table of Contents
- [Overview](#overview)
- [Project Structure](#project-structure)
- [Data Preprocessing](#data-preprocessing)
- [Models](#models)
- [Evaluation Metrics](#evaluation-metrics)
- [Visualization](#visualization)
- [Conclusions](#conclusions)
- [How to Run the Code](#how-to-run-the-code)
- [Dependencies](#dependencies)

## Overview
In this project, we applied both linear and non-linear models to a dataset to evaluate which model type best captures the data's underlying relationships. The models were compared using metrics such as **accuracy**, **F1 score**, **ROC AUC**, **weighted precision**, and **weighted recall**.

The Random Forest Classifier consistently outperformed Logistic Regression, indicating that the data contains non-linear relationships that Random Forest can capture more effectively than Logistic Regression.

## Project Structure
- **data/**: Contains the dataset used for training and testing the models.
- **notebooks/**: Jupyter notebooks with exploratory data analysis, model training, and evaluations.
- **src/**: Python scripts for data preprocessing, model training, evaluation, and visualization.
- **README.md**: Project overview and instructions (this file).

## Data Preprocessing
The following preprocessing steps were applied to prepare the data for modeling:
1. **Handling Missing Values**: Missing values were managed based on the feature type.
2. **Feature Encoding**: Categorical features were encoded using one-hot encoding and frequency encoding.
3. **Feature Scaling**: Features were scaled to ensure uniformity across variables.
4. **Class Imbalance Handling**: Undersampling was applied to manage class imbalance.

## Models
1. **Logistic Regression** (with Elastic Net regularization): A linear model used as a baseline.
2. **Random Forest Classifier**: A non-linear, tree-based ensemble model.

## Evaluation Metrics
The models were evaluated based on:
- **Accuracy**: Measures the overall correctness of the model.
- **F1 Score**: Balances precision and recall, especially useful in imbalanced data.
- **ROC AUC**: Evaluates the model's capability to distinguish between classes.
- **Weighted Precision and Recall**: Precision and recall weighted by class frequency to address class imbalance.

## Visualization
To support our findings, several visualizations were included:
1. **Confusion Matrix**: For both models, showing correct vs. incorrect predictions.
2. **Feature Importance Plots**: Highlights the most influential features for each model.
3. **Grouped Bar Chart**: Compares accuracy, F1 score, weighted precision, and recall between models.
4. **Spider Chart**: Provides a holistic view of all performance metrics.

### Sample Visualizations
![Grouped Bar Chart](path/to/grouped-bar-chart.png)
![Spider Chart](path/to/spider-chart.png)

## Conclusions
The project findings indicate that **Random Forest Classifier** is better suited for this dataset, as it consistently outperformed Logistic Regression across all metrics. The results suggest that the data has non-linear relationships, which Random Forest handles more effectively due to its ensemble nature. 

### Key Findings:
- **Random Forest** achieved higher accuracy, F1 score, weighted precision, and recall.
- The **ROC AUC score** for Random Forest (0.89806) significantly surpassed Logistic Regression (0.70182), highlighting its strength in distinguishing between classes.
- Feature importance analysis showed that Random Forest leverages complex, non-linear feature interactions that Logistic Regression cannot fully capture.

## How to Run the Code
1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   ```
2. **Navigate to the project directory**:
   ```bash
   cd your-repo-name
   ```
3. **Install the dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
4. **Run the Jupyter Notebook**:
   Open and execute the notebooks in the `notebooks/` directory to see the data preprocessing, model training, evaluation, and visualizations.

## Dependencies
- Python 3.x
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn

