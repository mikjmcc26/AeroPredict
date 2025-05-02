Breathing Numbers: Air Quality Prediction Using Machine Learning

Overview --
This project explores and predicts air pollution levels using historical sensor data from the UCI Air Quality dataset.
We use Python to clean and analyze the data, then build a machine learning model to forecast carbon monoxide (CO) concentrations based on environmental and chemical sensor features.

Dataset -- 
Source: UCI Machine Learning Repository - Air Quality Data Set

Total samples: ~9,357

Features include:

Chemical sensor readings (PT08.S1(CO), PT08.S2(NMHC), etc.)

Gas concentrations (CO(GT), NOx(GT), NO2(GT))

Weather data (T for temperature, RH for relative humidity, AH for absolute humidity)

Timestamps

Preprocessing --
Missing values encoded as -200 + replaced with NaN and forward-filled

Combined Date and Time columns into a proper DatetimeIndex

Extracted time-based features: Hour, Day, Month, and Weekday

Filtered rows with missing values in key features or target

Exploratory Data Analysis --
Inspected missing data patterns and handled them

Plotted feature distributions and correlation heatmaps

Examined the relationship between features and CO(GT)

Model --
We used Random Forest Regression from scikit-learn:

Input features: A subset of sensor and weather variables (PT08.S1(CO), PT08.S2(NMHC), T, RH, etc.)

Target: CO(GT) 

Performance Metrics --
Mean Squared Error (MSE): ~0.359

R^2 Score: ~0.844

Authors --
(our names)

Project inspired by real-world environmental challenges and a desire to explore machine learning for sustainability.

