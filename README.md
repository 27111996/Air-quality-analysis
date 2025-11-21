# Air Quality Analysis & Prediction Using Random Forest

This project analyzes air pollution data collected from an Italian city between March 2004 and February 2005. The goal is to clean the dataset, explore pollutant trends, build a Random Forest model, and evaluate how adding "season" improves prediction accuracy.

---

## 📌 Project Objectives
- Clean and preprocess raw air quality sensor data
- Handle missing and negative values
- Detect & remove outliers (IQR method)
- Explore time-based pollutant behavior
- Analyze correlations between environmental variables
- Build & evaluate a Random Forest regression model
- Compare models with and without seasonality

---

## 📊 Dataset
- **Source:** Kaggle — Air Quality Dataset  
- **Timeframe:** Mar 2004 – Feb 2005 (Hourly)  
- **Pollutants:** CO, Benzene (C6H6), NOx, NO2  
- **Sensors:** 5 metal-oxide sensors  
- **Environmental Features:** Temperature, RH, Absolute Humidity  

---

## 🛠️ Technologies Used
- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Scikit-learn  
- Jupyter Notebook  

---

## 🧹 Data Cleaning
- Converted comma values (“2,6”) → floats  
- Combined Date + Time  
- Removed >90% missing column (NMHC)  
- Interpolated CO values  
- Replaced negative sensor readings with NaN  
- Removed outliers (IQR, scale = 2)  
- Filtered incomplete rows  

---

## 🔎 Exploratory Data Analysis (EDA)
- Monthly pollutant variation  
- Smoothed normalized pollutant curves  
- Correlation heatmap  
- Pairwise relationships  
- Seasonal patterns  

**Findings**
- Pollution highest in colder months  
- October = peak benzene  
- August = lowest benzene  
- Strong correlation between C6H6 and NMHC  

---

## 🤖 Machine Learning Model

### **Model:** RandomForestRegressor  
### **Target:** PT08.S1(CO)

Two models were compared:

| Model | Features | R² Score |
|-------|----------|----------|
| Without Seasons | Numerical only | **0.92** |
| With Seasons | Numerical + One-Hot Season | **0.93** |

➡ Seasonality improved performance slightly.

---

## 📈 Example Visualizations
(Add your plot images here)

