📌 Project Overview

This project predicts flight departure delays (DepDelay) using machine learning.
The dataset contains US domestic flight information from 2018–2024, including schedule times, distances, weekdays, and weather delays.

The goal is to build a predictive ML model that can estimate expected departure delay using historical patterns.


---

📂 Dataset

The dataset contains over 5 million rows and 120 columns.
Important selected columns used for model training:

Year

Quarter

Month

DayOfMonth

DayOfWeek

CRSDepTime

CRSArrTime

Distance

WeatherDelay

DepDelay (Target)


After preprocessing, we reduced the dataset to 9 features + the target.


---

🧹 Data Cleaning & Preprocessing

Steps done:

1. Loaded dataset from Google Drive


2. Removed irrelevant and fully empty columns


3. Filled missing values using fillna(0)


4. Selected only useful numerical features


5. Created a smaller DataFrame for faster training


6. Split into Train (80%) and Test (20%)




---

🔍 Exploratory Data Analysis

Performed:

✔ Correlation Heatmap
✔ Feature Importance Graph
✔ Delay distribution plot

Top 3 most important features:

1. WeatherDelay


2. Distance


3. CRSDepTime
---

🤖 Machine Learning Models Used

We tested 3 regression models:

Model	MAE	RMSE	R² Score

Linear Regression	~24.76	~49.76	~0.17
Decision Tree	~23.97	~48.90	~0.16
Random Forest	~23.86	~48.85	~0.18


✅ Best Model: RandomForestRegressor

It gave the best accuracy and lowest error, so we saved it as the final model.


---

💾 Model Saving

Final model saved as:

final_flight_delay_model.pkl

This file can be used later for deployment.


---

🚀 How to Use This Project

1️⃣ Clone the Repo

git clone https://github.com/KalakondaBhavani/Flight-delay-ml-project.git

2️⃣ Install Dependencies

pip install pandas numpy scikit-learn matplotlib seaborn

3️⃣ Load and Use the Model

import pickle

with open("final_flight_delay_model.pkl", "rb") as f:
    model = pickle.load(f)

prediction = model.predict([[2024, 1, 1, 14, 7, 1540, 1656, 738, 0]])
print(prediction)


---

📈 Project Completion

✔ Dataset loading
✔ Data cleaning
✔ Feature engineering
✔ Train-test split
✔ Model building
✔ Multiple model comparison
✔ Final model saved
✔ Final README prepared

Total Completion: 100%


---

🏁 Final Summary

This project successfully builds a prediction model for flight delays using 6 years of data.
The final RandomForest model achieves ~18% R² accuracy, which is acceptable for Week-4 final submission considering noise in delay data.
