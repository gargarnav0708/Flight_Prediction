# Flight_Prediction
Airfare prices fluctuate rapidly due to multiple factors like airline operator, travel route, flight duration, number of stops, and departure schedules. In this project we aim to develop a prediction model capable of estimating ticket prices from historical booking data. 

## The dataset used here contains: 

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

# Project Workflow:

## 1. Data Collection and Cleaning
   
   Load excel containing fare dataset  
   Handle missing values and remove inconsistent records

## 2. Feature Engineering
   
   Extracted journey date, departure time, and arrival time features.  
   Converted flight duration into numerical attributes.

## 3. Encoded categorical variables such as airline, source, destination, and total stops.
   
   Exploratory Data Analysis (EDA)  
   Analyzed relationships between flight duration, stops, airlines, and ticket prices.

## 4. Visualized trends using Matplotlib, Seaborn, and Plotly.
   
   Outlier Treatment  
   Identified extreme fare values using the IQR method.  
   Reduced the impact of outliers to improve model performance.

## 5. Feature Selection
    
   Evaluated feature importance using Mutual Information Regression.  
   Selected the most relevant predictors for price estimation.

## 6. Model Training
    
   Split data into training and testing sets.  
   Trained machine learning models including Random Forest Regressor and Decision Tree Regressor.

## 7. Model Evaluation
    
   Assessed performance using R² Score, MAE, RMSE, MSE, and MAPE.  
   Hyperparameter Tuning

## 8. Optimized model parameters using RandomizedSearchCV.
   Model Serialization

## 9. Saved the trained model using Pickle for future predictions and deployment.

# Results of the Trained Model:

## Model Performance

The final model was trained using a **Random Forest Regressor** after performing data cleaning, feature engineering, categorical encoding, outlier treatment, and feature selection. The model demonstrates strong predictive capability, explaining approximately **81% of the variance** in flight ticket prices on unseen test data.

### Performance Metrics

| Metric                                | Score        |
| ------------------------------------- | ------------ |
| Training R² Score                     | 0.9512       |
| Test R² Score                         | 0.8082       |
| Mean Absolute Error (MAE)             | 1,185.95     |
| Mean Squared Error (MSE)              | 3,734,120.27 |
| Root Mean Squared Error (RMSE)        | 1,932.39     |
| Mean Absolute Percentage Error (MAPE) | 13.26%       |

### Interpretation

* The model achieves an **R² score of 0.808**, indicating that it can explain over **80% of the variation** in flight prices.
* The relatively low **MAPE of 13.26%** suggests that predictions are typically within 13% of the actual ticket price.
* A **training R² score of 0.951** compared to a test R² score of 0.808 indicates good learning performance, though some degree of overfitting is present, which is expected with ensemble models such as Random Forests.
* Overall, the model provides reliable fare predictions and demonstrates the effectiveness of the engineered features in capturing pricing patterns within the airline industry.

