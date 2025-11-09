✅ 1. Dataset Acquisition

Downloaded the Flight Data (2018–2024) dataset.

Uploaded the dataset to Google Drive for storage.

Loaded the dataset into Google Colab using Pandas.


✅ Dataset loading completed successfully.


---

✅ 2. Data Exploration

Explored dataset structure using:

df.head()

df.info()

df.describe()


Identified key attributes such as:

Year, Quarter, Month

DayOfMonth, DayOfWeek

CRSDepTime, CRSArrTime

Distance

WeatherDelay

DepDelay (target)



✅ Dataset understood and key variables identified.


---

✅ 3. Data Cleaning

Removed completely empty columns.

Selected only required columns for Week-2 model:

['Year', 'Quarter', 'Month', 'DayOfMonth', 'DayOfWeek', 'CRSDepTime', 'CRSArrTime', 'Distance', 'WeatherDelay', 'DepDelay']


Handled missing values using:

df_small = df_small.fillna(0)

Verified that all missing values were treated.


✅ Clean dataset created.


---

✅ 4. Feature Selection

Created two sets:

Features (X):
Year, Quarter, Month, DayOfMonth, DayOfWeek, CRSDepTime, CRSArrTime, Distance, WeatherDelay

Target (y):
DepDelay (Departure Delay)


✅ Feature/target selection completed.


---

✅ 5. Train-Test Split

Used 80% for training and 20% for testing.

Output shapes:

X_train: (4,659,840 rows, 9 features)

X_test: (1,164,585 rows, 9 features)



✅ Dataset split successfully.


---

✅ 6. Model Training

Model Used: RandomForestRegressor

Parameters:

n_estimators = 50
max_depth = 15
random_state = 42

Successfully trained the model on 4.6 million rows.


✅ Model training completed.


---

✅ 7. Model Evaluation

Evaluated using regression metrics:

Metric	Value

MAE (Mean Absolute Error)	~23.86 minutes
RMSE (Root Mean Squared Error)	~58.70 minutes
R² Score	~0.185


✅ Model performance is realistic for flight delay data.
✅ R² score is reasonable since flight delays are influenced by unpredictable factors.


---

✅ 8. Feature Importance Analysis

Most important predictors:

1. WeatherDelay – 49.75%


2. Distance


3. CRSDepTime


4. CRSArrTime


5. DayOfMonth



Least contributing features:

Year

Quarter

Month


✅ Feature importance generated successfully.


---

✅ Summary of Week 2

All Week 2 tasks have been completed:

✅ Dataset loaded
✅ Cleaning & preprocessing
✅ Feature selection
✅ Train-test split
✅ Model training
✅ Performance evaluation
✅ Feature importance

✔ Project completion so far: ~60%
