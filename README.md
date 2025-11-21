Air Quality Analysis & Prediction Using Random Forest

This project analyzes air pollution data collected from an Italian city between March 2004 – February 2005. It includes full data cleaning, exploratory analysis, feature engineering, and a Random Forest regression model to predict pollutant levels.

Project Goals

Clean and preprocess raw sensor data
Handle missing values and negative sensor readings
Detect and remove outliers
Explore pollutant trends over time
Analyze correlations between pollutants
Build a Random Forest regression model
Assess the impact of adding season as a feature

 Dataset

Source: Kaggle (Air Quality Dataset)
Timeframe: March 2004 – February 2005
Frequency: Hourly
Sensors: 5 chemical oxide sensors
Pollutants: CO, NOx, Benzene, NMHC, NO2
Environmental: Temperature, Humidity, Absolute Humidity

Data Cleaning Steps

Dropped empty columns
Converted comma numbers (“2,6”) into float values
Converted all object numerical columns to float
Combined Date + Time into a single datetime column
Removed extremely missing sensors (NMHC > 90%)
Interpolated missing CO values
Removed negative readings
Applied IQR outlier filtering
Removed remaining rows with missing data

Exploratory Data Analysis (EDA)

Time-series plots of pollutants
Normalized and smoothed pollutant signals
Monthly boxplots showing seasonal patterns
Correlation heatmap
Pairplots for multivariate patterns

Key findings:

Benzene peaks in colder months
Lowest pollutant period: August
Highest pollutant period: October
Strong multicollinearity between C6H6(GT) and NMHC

Machine Learning Model
Model: RandomForestRegressor
Target Variable: PT08.S1(CO)
Two models were trained:

Model 1 — Without Seasons
Train/test split: 80/20
R² = 0.92

Model 2 — With Season Category
Added: spring, summer, autumn, winter
One-hot encoding applied
R² improved to 0.93

➡️ Seasonality improves prediction accuracy


##  Technologies Used

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Scikit-learn  
- Jupyter Notebook  

