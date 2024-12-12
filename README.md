# Energy Generation Prediction Project

This project predicts daily electricity demand and classifies demand levels (low, medium, high) based on multiple features, such as weather conditions and real estate growth. It uses various regression and classification models to analyze the factors influencing electricity demand and assess their predictive power.

## Objective
- Predict the maximum electricity demand met during a day (in MW).
- Classify electricity demand into three categories: low, medium, and high.
- Evaluate the performance of multiple machine learning models for both regression and classification tasks.

## Dataset Details
- **Source**: Daily electricity generation data.
- **Features**: 
  - Maximum demand met during the day (MW).
  - Shortage during maximum demand (MW).
  - Energy met (MU).
  - Date.
  - Simulated weather data: temperature, humidity, and wind speed.
  - Additional features: holiday flag, real estate growth.
- **Target Variables**:
  - Regression target: Maximum demand met (MW).
  - Classification target: Demand level (low, medium, high).

## Implementation Steps

### 1. Data Preparation
- **Cleaning and Feature Engineering**:
  - Extract relevant columns from the dataset.
  - Simulate weather-related data and additional features like holiday flag and real estate growth.
  - Categorize demand levels using bins for classification.
- **Splitting Data**:
  - 80% for training, 20% for testing.
- **Feature Scaling**:
  - Standardize features for model compatibility using `StandardScaler`.

### 2. Model Evaluation
- **Regression Models**:
  - Random Forest Regressor.
  - Linear Regression.
  - K-Nearest Neighbors Regressor.
  - Decision Tree Regressor.
  - Support Vector Regressor.
- **Classification Models**:
  - Random Forest Classifier.
  - K-Nearest Neighbors Classifier.
  - Decision Tree Classifier.
  - Support Vector Classifier.
- Metrics:
  - Regression: Mean Squared Error (MSE), R² score.
  - Classification: Accuracy, classification report.

### 3. User Interaction
- Allow users to input custom weather and feature data to predict electricity demand.
- Compare predictions with the closest matching record from the dataset.

## Example Output
### Regression Evaluation
For each regression model:
```plaintext
Random Forest Regression Model Performance:
Mean Squared Error (MSE): 12345.67
R² Score: 0.89
```

### Classification Evaluation
For each classification model:
```plaintext
Random Forest Classification Model Performance:
Accuracy Score: 0.85
Classification Report:
               precision    recall  f1-score   support

          low       0.89      0.83      0.86        50
       medium       0.81      0.88      0.85        60
         high       0.86      0.84      0.85        40
```

### User Prediction Example
```plaintext
Predicted Electricity Demand: 4500.00 MW
Actual Electricity Demand from dataset: 4400.00 MW
Difference: 100.00 MW
```

## Instructions
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/energy-generation-prediction.git
   cd energy-generation-prediction
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the script to preprocess data, train models, and generate predictions.
