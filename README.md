# Airbnb Superhost Prediction 

This project uses Logistic Regression to predict whether an Airbnb host is a **Superhost** based on features such as response rate, review scores, and more.

## 📁 Files

- `airbnbData_train.csv`: Preprocessed dataset used to train the model.
- `logistic_model_best.pkl`: Trained Logistic Regression model (best hyperparameter selected via GridSearchCV).

## 📊 Model Overview

- Classifier: Logistic Regression
- Hyperparameter tuning: GridSearchCV (C values from 1e-5 to 1e4)
- Evaluation: Accuracy, Confusion Matrix, Precision-Recall, ROC-AUC

## 🔄 Usage

To load and use the model:

```python
import pickle
with open('logistic_model_best.pkl', 'rb') as file:
    model = pickle.load(file)

# Then make predictions:
model.predict(X_test)
