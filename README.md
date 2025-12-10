# Heart Disease Classification

Predicting whether a patient has a low (0) or high (1) chance of heart disease using machine learning classification on clinical features such as age, sex, chest pain type, blood pressure, cholesterol, and more. This project is for learning and educational purposes only and must not be used for real medical diagnosis or clinical decisions.

## Project Goal

Build an end-to-end ML pipeline that:
- Explores and visualizes the heart disease dataset  
- Trains multiple classifiers  
- Selects and saves the best model  
- Can be reused to predict risk for new patients  

## Dataset

The dataset is based on the UCI Heart Disease (Cleveland) data and contains 303 rows and 14 columns.

Main columns (inputs):

- age, sex  
- cp – chest pain type  
- trtbps – resting blood pressure  
- chol – cholesterol  
- fbs – fasting blood sugar (>120 mg/dl)  
- restecg – resting ECG results  
- thalachh – maximum heart rate achieved  
- exng – exercise induced angina  
- oldpeak – ST depression  
- slp – slope of ST segment  
- caa – number of major vessels  
- thall – thalassemia  

Target:

- output – 0 = low chance of heart disease, 1 = high chance  

## Methods

Steps followed in the notebook:

1. Exploratory Data Analysis (EDA): correlations, distributions, class balance.  
2. Data preprocessing: train-test split, feature scaling with StandardScaler.  
3. Model training: Logistic Regression, Random Forest, XGBoost.  
4. Evaluation: accuracy, ROC-AUC, confusion matrix, classification report.  
5. Model selection and saving with joblib.  

## Results

The best model is a Random Forest classifier trained on scaled features.

| Model          | Accuracy | ROC-AUC |
|----------------|----------|---------|
| Logistic       | 0.80     | 0.87    |
| Random Forest  | 0.79     | 0.92    |
| XGBoost        | 0.80     | 0.86    |

Random Forest was selected and saved as heart_disease_model.pkl together with the scaler (scaler.pkl).

## Files in This Repository

- data.csv – heart disease dataset  
- notebook.ipynb – full EDA, preprocessing, modeling  
- heart_disease_model.pkl – trained Random Forest model  
- scaler.pkl – fitted StandardScaler  
- feature_importance.png – feature importance plot  
- requirements.txt – Python dependencies  

## How to Run

1. Clone the repository and open the project folder.  
2. (Optional) Create and activate a virtual environment.  
3. Install dependencies with: pip install -r requirements.txt  
4. Open and run notebook.ipynb with Jupyter Notebook or JupyterLab.  

Again, this project is only for learning; any predictions must not be treated as medical advice.
