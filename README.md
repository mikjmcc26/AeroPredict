# AeroPredict: Air Quality Prediction Using Machine Learning

## Authors
Chase Woodfill and Mikayla McCormack

This project was developed as part of a course project, inspired by real-world environmental concerns and an interest in applying machine learning to public health and sustainability.

## Overview
AeroPredict is a machine learning project to forecast air pollution levels using historical sensor data. We built a predictive model focused on carbon monoxide (CO) concentration using the Air Quality Data Set from the UCI Machine Learning Repository. The goal is to provide early warnings about deteriorating air quality, aiding both individuals and policymakers in making informed, proactive decisions.

Our model leverages chemical sensor responses and meteorological data to accurately forecast pollution trends through time. The project is developed in Python using popular data science libraries including pandas, scikit-learn, seaborn, and matplotlib.

## Usage & Set Up
To use this project, simply run the provided Jupyter notebook (AirPrediction.ipynb). It will walk you through the full process—from loading and cleaning the dataset to training the model and visualizing predictions. The notebook is fully annotated and ready for experimentation or extension.

### Requirements
Running the notebook requires the following libaries:
- `pandas`
- `numpy`
- `scikit-learn`
- `matplotlib`
- `seaborn`

### Script Command 
Open the Jupyter Notebook with the following command, assuming all dependicies are properly installed: `jupyter notebook AirPrediction.ipynb`


## Dataset 
- Source: UCI Machine Learning Repository - Air Quality Data Set
- Kaggle Link: https://www.kaggle.com/datasets/fedesoriano/air-quality-data-set?resource=download
- Total samples: ~9,357
- Time Period: March 2004 – February 2005
- Location: Roadside monitoring station in an Italian city

#### Features include:
- Chemical sensor readings (PT08.S1(CO), PT08.S2(NMHC), etc.)
- Gas concentrations (CO(GT), NOx(GT), NO2(GT))
- Weather data (T for temperature, RH for relative humidity, AH for absolute humidity)
- Timestamps

#### Preprocessing
- Missing values encoded as -200 + replaced with NaN and forward-filled
- Combined Date and Time columns into a proper DatetimeIndex
- Extracted time-based features: Hour, Day, Month, and Weekday
- Filtered rows with missing values in key features or target

## Exploratory Data Analysis
- Inspected missing data patterns and handled them
- Plotted feature distributions and correlation heatmaps
- Examined the relationship between features and CO(GT)

## Model
We used Random Forest Regression from scikit-learn:
- Input features: A subset of sensor and weather variables (PT08.S1(CO), PT08.S2(NMHC), T, RH, etc.)
- Target: CO(GT) 

### Performance Metrics
- **Mean Squared Error (MSE): ~0.359**
- **R^2 Score: ~0.844**

## Acknowledgements
University of Tennessee, Knoxville. CS426/526.
