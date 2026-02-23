## Student Performance Prediction – End-to-End ML Pipeline

## OVERVIEW  

## R² Score on test dataset: ~0.87

This project implements a complete end-to-end Machine Learning pipeline to predict a student’s math score based on demographic and academic features such as reading score, writing score, parental education level, lunch type, and test preparation course.

The project demonstrates the full ML lifecycle:

1.Data ingestion

2.Data preprocessing and feature engineering

3.Model training and evaluation

4.Hyperparameter tuning

5.Model serialization

6.Web deployment using Flask

## Problem Statement

Build a regression model that predicts math_score using student demographic and academic features.

The goal is to design a production-ready ML pipeline with modular components and proper separation of concerns.

## Project Architecture
MLproject/
│
├── artifacts/
│   ├── model.pkl
│   ├── preprocessor.pkl
│   ├── train.csv
│   ├── test.csv
│   ├── data.csv
│
├── src/
│   ├── components/
│   │   ├── data_ingestion.py
│   │   ├── data_transformation.py
│   │   ├── model_trainer.py
│   │
│   ├── pipeline/
│   │   ├── predict_pipeline.py
│   │
│   ├── utils.py
│   ├── exception.py
│   ├── logger.py
│
├── templates/
│   ├── index.html
│   ├── home.html
│
├── app.py
├── requirements.txt


## TECH STACK

Programming Language

Python

Data & ML

NumPy

Pandas

Scikit-learn

GridSearchCV

ColumnTransformer

StandardScaler

OneHotEncoder

Visualization

Matplotlib

Seaborn

Deployment

Flask

HTML / CSS

🔄 Machine Learning Pipeline
1️⃣ Data Ingestion

Reads dataset from CSV

Performs train-test split

Saves:

train.csv

test.csv

data.csv

2️⃣ Data Transformation

Numerical Features:

Median Imputation

Standard Scaling

Categorical Features:

Most Frequent Imputation

One Hot Encoding

Scaling (with_mean=False)

Uses ColumnTransformer

Saves preprocessor as:

artifacts/preprocessor.pkl
3️⃣ Model Training

Multiple regression models evaluated

Hyperparameter tuning using GridSearchCV

Best model selected based on R² score

Final trained model saved as:

artifacts/model.pkl
4️⃣ Model Deployment

Flask-based web interface

Accepts user input

Loads:

model.pkl

preprocessor.pkl

Applies preprocessing

Returns prediction

📊 Model Performance

## R² Score on test dataset: ~0.87

This indicates strong predictive performance and proper generalization.

🚀 How to Run the Project
Step 1 — Clone the Repository
git clone <your-repo-link>
cd MLproject
Step 2 — Create Virtual Environment
python -m venv venv
venv\Scripts\activate
Step 3 — Install Dependencies
pip install -r requirements.txt
Step 4 — Train the Model
python src/components/data_ingestion.py

This will generate:

model.pkl

preprocessor.pkl

train.csv

test.csv

Step 5 — Run Flask App
python app.py

Open browser:

http://127.0.0.1:5000
🧠 Key Learnings

Structuring production-grade ML projects

Modular pipeline development

Separation of training and inference logic

Artifact serialization using pickle

Handling preprocessing consistency between training and prediction

Deploying ML models with Flask

📌 Future Improvements

Add Docker containerization

Deploy to cloud (AWS / Render / Railway)

Add CI/CD pipeline

Improve UI/UX

Add model monitoring & logging

Experiment with advanced models (XGBoost, LightGBM)

👨‍💻 Author

Prakhar Sharma
B.Tech CSE Student
Machine Learning & AI Enthusiast
