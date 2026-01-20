Project Overview

This project focuses on preprocessing the Adult Income Dataset (from Kaggle) to make it ready for Machine Learning models.
The preprocessing pipeline includes feature identification, encoding, scaling, and saving the final processed dataset.

The dataset predicts whether a person earns more than $50K per year based on demographic and employment attributes.
Dataset

Source: Kaggle – Adult Income Dataset

Target Variable: income

Type: Classification Dataset
Objectives

Identify categorical and numerical features

Apply Label Encoding where order exists

Apply One-Hot Encoding where order does not exist

Scale numerical features using StandardScaler

Compare model readiness before and after scaling

Explain the impact of scaling on ML algorithms

Save the processed dataset for ML training
Technologies Used

Python 🐍

Pandas

NumPy

Scikit-Learn

Jupyter Notebook / Google Colab
Feature Classification
🔹 Numerical Features

age

capital-gain

capital-loss

hours-per-week

🔹 Categorical Features

workclass

education

marital-status

occupation

relationship

race

native-country
Preprocessing Steps
1️⃣ Load Dataset

The dataset is loaded using Pandas and inspected for structure and data types.
2️⃣ Feature Identification

Numerical features identified using data types (int, float)

Categorical features identified using object data types
3️⃣ Label Encoding (Ordered Data)

Applied to education feature

Preserves natural ranking (Preschool → Doctorate)
4️⃣ One-Hot Encoding (Unordered Data)

Applied to nominal categorical features

Prevents incorrect ordinal assumptions

Avoids model bias
5️⃣ Feature Scaling

StandardScaler used for numerical features

Converts values to:

Mean ≈ 0

Standard Deviation ≈ 1
6️⃣ Model Readiness Comparison
| Aspect             | Before Scaling | After Scaling |
| ------------------ | -------------- | ------------- |
| Feature Range      | Uneven         | Standardized  |
| Training Stability | Low            | High          |
| Convergence Speed  | Slow           | Faster        |
| Model Accuracy     | Inconsistent   | Improved      |
7️⃣ Impact of Scaling on ML Algorithms
✔ Algorithms that Require Scaling

Logistic Regression

Support Vector Machine (SVM)

K-Nearest Neighbors (KNN)

Neural Networks
8️⃣ Save Processed Dataset
adult_income_processed.csv
Project Structure
Adult-Income-Preprocessing/
│
├── adult.csv
├── adult_income_processed.csv
├── preprocessing.ipynb
├── README.md

pip install pandas numpy scikit-learn

python preprocessing.py
✅ Final Outcome

Dataset transformed into machine-learning-ready format

Proper encoding and scaling applied

Suitable for classification models

Reusable preprocessing pipeline
