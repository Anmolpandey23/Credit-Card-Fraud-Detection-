# Credit-Card-Fraud-Detection-
## Project Description
This project aims to detect fraudulent credit card transactions using machine learning, specifically Logistic Regression. Since credit card fraud is a serious global issue costing billions of dollars each year, having an accurate fraud detection model is critical.

To tackle this, we use a publicly available dataset that contains thousands of real transactions (both legitimate and fraudulent), train a predictive model, and build an interactive web app using Streamlit to test new inputs and identify whether they’re fraud or legit.

## Problem Statement
Credit card fraud often involves rare anomalies in large datasets — only a small fraction of all transactions are fraudulent. This causes class imbalance, making it challenging to train models accurately.

Our objective is to:

- Preprocess the dataset to balance classes

- Train a machine learning model that can accurately classify fraud

- Evaluate the model performance using standard metrics

# How the Model Works
## 📊 Dataset Summary:
**Source**: [Kaggle - Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)

- Samples: 284,807 transactions

- Fraudulent: 492 transactions (~0.17%)

- Features:

  - Time, Amount, and V1 to V28: These V-features are PCA-transformed (Principal Component Analysis) variables to protect customer identity and transaction details.

  - Class: Target label (0 = Legit, 1 = Fraud)

##  ML Pipeline

### Step-by-Step

1. **Load & Explore Data**
   The dataset is loaded and checked for missing values and distribution of classes.
3. **Handle Imbalanced Data**
   - Since fraud cases are rare, we take a balanced sample:

   - 492 fraud cases

   - 492 legitimate cases

This creates a 50:50 balanced dataset for training.
4. **Split Data**
   - Features: All columns except Class

   - Label: Class

   - Use an 80/20 split for train/test sets
5. **Model Training**
   - Use Logistic Regression: a simple and interpretable binary classifier.

   - Trained on the balanced dataset
6. **Model Evaluation**
   - Use Accuracy Score for both training and test data

   - Can be extended to use F1-score, Recall (important for fraud detection)

## Why Logistic Regression?
Logistic Regression is:

- Simple and effective for binary classification

- Works well on linear decision boundaries

- Efficient with smaller datasets

- Interpretable — good for explaining results

## Help me to add:

1. **Location-Based Fraud Detection**
   - Problem: Fraud often happens across geographies.
   - Twist: Use geolocation data (e.g., IP, device location, billing address) and travel speed checks (can the person physically be in two cities 2,000 km apart within 5 minutes?).
     
2. **Real-Time Fraud Feedback Loop**
   - Problem: Fraud labels are often delayed.
   - Twist: Simulate a real-time learning loop where the model updates incrementally using feedback from confirmed frauds/non-frauds (like user "this wasn't me" flags).
