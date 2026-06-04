# Flight_Prediction
Airfare prices fluctuate rapidly due to multiple factors like airline operator, travel route, flight duration, number of stops, and departure schedules. In this project we aim to develop a prediction model capable of estimating ticket prices from historical booking data. 

##The dataset used here contains: 

Airline
Date of Journey
Source Airport
Destination Airport
Route
Departure Time
Arrival Time
Duration
Total Stops
Additional Information
Ticket Price (Target Variable to be Predicted)

#Project Workflow:

1. Data Collection and Cleaning
   Load excel containing fare dataset
   Handle missing values and remove inconsistent records

2. Feature Engineering
   Extracted journey date, departure time, and arrival time features.
   Converted flight duration into numerical attributes.

3. Encoded categorical variables such as airline, source, destination, and total stops.
   Exploratory Data Analysis (EDA)
   Analyzed relationships between flight duration, stops, airlines, and ticket prices.

4. Visualized trends using Matplotlib, Seaborn, and Plotly.
   Outlier Treatment
   Identified extreme fare values using the IQR method.
   Reduced the impact of outliers to improve model performance.

5. Feature Selection
   Evaluated feature importance using Mutual Information Regression.
   Selected the most relevant predictors for price estimation.

6. Model Training
   Split data into training and testing sets.
   Trained machine learning models including Random Forest Regressor and Decision Tree Regressor.

7. Model Evaluation
   Assessed performance using R² Score, MAE, RMSE, MSE, and MAPE.
   Hyperparameter Tuning

8. Optimized model parameters using RandomizedSearchCV.
   Model Serialization

9. Saved the trained model using Pickle for future predictions and deployment.

