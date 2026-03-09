# Day 11 — ML Model Training (AI/ML QA Journey)

## Overview

On Day 11 of my AI/ML QA journey, I explored how machine learning models are trained and how QA engineers evaluate them.

The goal was to build a **simple classification model using Scikit-learn** and understand basic **ML QA testing concepts**.

---

# What is Scikit-learn?

Scikit-learn is one of the most popular Python libraries for Machine Learning.

It provides tools for:

- Model training
- Data preprocessing
- Model evaluation
- Dataset loading
- Testing ML pipelines

Because of its simplicity and reliability, it is widely used in both research and industry.

---

# Dataset Used

This project uses the **Iris Dataset**, a classic machine learning dataset used for classification tasks.

Dataset features:

- Sepal Length
- Sepal Width
- Petal Length
- Petal Width

Target classes:

- Iris Setosa
- Iris Versicolor
- Iris Virginica

The task is to predict the flower species based on these measurements.

---

# Model Training Example

python
from sklearn.datasets import load_iris
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression

iris = load_iris()

X = iris.data
y = iris.target

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

model = LogisticRegression()
model.fit(X_train, y_train)


Model Evaluation:

After training, predictions are made on the test dataset.

from sklearn.metrics import accuracy_score

predictions = model.predict(X_test)

accuracy = accuracy_score(y_test, predictions)

print("Model Accuracy:", accuracy)

Example output:

Model Accuracy: 0.97

ML QA Testing Concepts

Machine Learning QA engineers ensure that models behave correctly and reliably.

Important checks include:

1. Accuracy Testing

Ensuring the model meets performance expectations.

2. Edge Case Testing

Testing unusual inputs to confirm the model does not crash.

Example:

edge_case = [[0,0,0,0]]
prediction = model.predict(edge_case)
3. Bias Testing

Ensuring the model does not unfairly favor certain classes or groups.

4. Reliability Testing

Confirming consistent predictions across multiple runs.

Key Takeaways

From this exercise I learned:

How ML models are trained

How datasets are split into training and testing sets

How to evaluate model performance

Basic QA practices for machine learning systems
