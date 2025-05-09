# Customer Complaint Classification & Resolution Time Prediction

This project is focused on developing a dual-machine learning solution to streamline customer support operations by:

1. Automatically classifying unstructured customer complaints into one of five predefined issue categories.
2. Predicting the expected resolution time for each issue based on structured metadata.

---

## Folder Structure

CustomerComplaintML/
│
├── data/
│ └── Project Data.csv
├── notebooks/
│ ├── CustomerComplaint_IssueClassification.ipynb
│ └── CustomerComplaint_ResolutionTimePrediction.ipynb
├── .gitignore
└── README.md


---

## Problem Statement

Customer support teams face delays due to manual processing of large volumes of customer complaints. This project tackles the challenge by building two intelligent ML models:

- **Classification Model** to identify the type of issue.
- **Regression Model** to estimate the time needed to resolve the complaint.

This improves ticket routing, prioritization, and overall customer experience.

---

## Project Objectives

- Classify complaints into one of the following categories:
  - Technical Issue
  - Account & Login Issue
  - Billing & Payment Issue
  - Connectivity Issue
  - Software Issue

- Predict **Resolution Time (in minutes)** using features such as:
  - Message Length
  - Submission Channel
  - Platform Type
  - Response Time

---

## Dataset Description

The dataset consists of 150 synthetically generated customer complaints with realistic structure and variety.

| Feature            | Type         | Description |
|--------------------|--------------|-------------|
| Customer Statement | Text         | Free-text complaint from the user |
| Issue Category     | Categorical  | Classification target variable |
| Resolution Time    | Continuous   | Regression target variable (in minutes) |
| Response Time      | Continuous   | Time before first response (in seconds) |
| Message Length     | Continuous   | Word count of the complaint |
| Submission Channel | Categorical  | Email, Phone, or Live Chat |
| Platform Type      | Categorical  | Web, Mobile App, or Desktop |

---

## Models Used

### Classification (`CustomerComplaint_IssueClassification.ipynb`)
- Vectorizer: TF-IDF
- Models:
  - Logistic Regression
  - Multinomial Naive Bayes
  - Random Forest Classifier
- Evaluation:
  - Accuracy Score
  - Precision, Recall, F1-Score (via classification report)
  - Confusion Matrix (with heatmap)


### Regression (`CustomerComplaint_ResolutionTimePrediction.ipynb`)
- Preprocessing: Feature Scaling
- Models:
  - Linear Regression
  - Ridge & Lasso Regression
  - Decision Tree Regressor
- Evaluation: MAE, RMSE, R² Score



