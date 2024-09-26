# Bank Marketing Dataset Analysis

## Overview
This repository contains an analysis of the Bank Marketing dataset, which aims to predict client subscriptions to term deposits based on demographic and campaign-related attributes.

## Dataset Description
The Bank Marketing dataset consists of 17 attributes and 45,211 instances. The attributes include:
- **Demographic information**: age, job, marital status, education
- **Campaign-related attributes**: contact, day, month, duration, campaign, pdays, previous
- **Banking information**: default, balance, housing, loan
- **Outcome attribute (y)**: subscription to term deposit (yes/no)

## Analysis Goals
- **Predictive Modeling**: Develop machine learning models to predict client subscriptions.
- **Understanding Customer Behavior**: Analyze relationships between client attributes and subscription likelihood.

## Methodology
1. **Data Preprocessing**: Label encoding for categorical variables.
2. **Data Visualization**: Correlation analysis and heatmap.
3. **Model Building**: Decision Tree, Random Forest, XGBoost, Support Vector Machine, and Multilayer Perceptron.
4. **Model Evaluation**: Accuracy, precision, recall, and F1 score.

## Results
| Model                  | Accuracy | Precision | Recall | F1 Score |
|------------------------|----------|-----------|--------|----------|
| Decision Tree          | 0.87     | 0.45      | 0.49   | 0.47     |
| XGBClassifier          | 0.90     | 0.64      | 0.35   | 0.45     |
| Random Forest          | 0.91     | 0.64      | 0.43   | 0.51     |
| Support Vector Machine  | 0.88     | 0.41      | 0.01   | 0.01     |
| MLP Classifier         | 0.90     | 0.62      | 0.31   | 0.41     |

## Model Deployment
A Random Forest classifier is deployed and saved as `Bank_model.pkl` using Pickle.

### Streamlit Application
You can interact with the model through the deployed Streamlit app: [Bank Marketing Analysis App](https://bankmarketing-8ywvqsax4ak2expdidvpau.streamlit.app/).

## Example Usage
```python
import pickle

model = pickle.load(open('Bank_model.pkl', 'rb'))
print(model.predict([[58, 4, 1, 2, 0, 2143, 1, 0, 2, 5, 8, 261, 1, -1, 0, 3]]))
