# Day 8 – ML Evaluation Metrics  
AI/ML QA Engineering Journey

## 🎯 Objective
Today I focused on understanding how to properly evaluate Machine Learning classification models.

As an AI/ML QA Engineer, evaluation metrics are more important than the model itself.

---

## 📊 Why Metrics Matter

A model can show high accuracy but still fail in critical situations.

Evaluation metrics help us understand:

- Are we missing important cases?
- Are we making dangerous false predictions?
- Is the dataset balanced?
- Can this model be trusted in production?

---

## 🔎 Confusion Matrix (Foundation of All Metrics)

|                | Predicted Positive | Predicted Negative |
|---------------|-------------------|-------------------|
| Actual Positive | True Positive (TP) | False Negative (FN) |
| Actual Negative | False Positive (FP) | True Negative (TN) |

Understanding this matrix is essential for QA analysis.

---

## 1️⃣ Accuracy

Formula:
(TP + TN) / Total Predictions

Meaning:
How many total predictions were correct?

Limitation:
- Misleading when dataset is imbalanced
- Does not show type of errors

QA Insight:
Never rely on accuracy alone.

---

## 2️⃣ Precision

Formula:
TP / (TP + FP)

Meaning:
Out of all predicted positives, how many were actually positive?

Focus:
Controls False Positives

Important When:
- False alarms are costly
- Fraud detection
- Spam detection

QA Insight:
High precision means fewer wrong positive predictions.

---

## 3️⃣ Recall (Sensitivity)

Formula:
TP / (TP + FN)

Meaning:
Out of all actual positives, how many did we correctly detect?

Focus:
Controls False Negatives

Important When:
- Missing real cases is dangerous
- Medical diagnosis
- Safety systems

QA Insight:
Low recall means the model is missing important cases.

---

## 4️⃣ F1 Score

Formula:
2 × (Precision × Recall) / (Precision + Recall)

Meaning:
Balanced measure between precision and recall.

Important When:
- Dataset is imbalanced
- Need balance between FP and FN

QA Insight:
F1 Score gives more realistic performance than accuracy.

---

## 🧠 QA Thinking Questions

When evaluating a model, always ask:

- Is the dataset balanced?
- Which error is more dangerous: FP or FN?
- Are we missing important positive cases?
- Are we falsely predicting positives?
- Which metric aligns with business risk?

---

## 💻 Tools Used

- Python
- Pandas
- Scikit-learn
- Jupyter Notebook

---

## 🚀 Learning Outcome

Models do not fail because of algorithms.
They fail because we measure them incorrectly.

As an AI/ML QA Engineer, my responsibility is to evaluate risk — not just numbers.
