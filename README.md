# Bike Sharing Demand Analysis

> This project analyzes the factors influencing daily bike rental demand using multiple linear regression. The analysis identifies key variables that affect the number of bikes rented per day and builds an interpretable predictive model.

---

## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)
* [Contact](#contact)

---

## General Information
- **Background:**  
  The growth of shared mobility systems has led to an increased demand for accurate forecasting of bike rental usage. Understanding which factors most influence daily rentals helps in operational planning, inventory management, and customer satisfaction.

- **Business Problem:**  
  The goal of this project is to predict daily bike rental counts (`cnt`) based on weather conditions, time-related variables, and other factors. Accurate prediction helps the bike-sharing company ensure adequate bike availability and improve resource management.

- **Dataset Used:**  
  The dataset used is **`day.csv`**  
  It includes daily records of bike rentals with variables such as temperature, humidity, season, weather situation, and user counts (casual and registered).  
  - **Dependent Variable:** `cnt` (total number of bikes rented)  
  - **Independent Variables:** season, yr, mnth, holiday, weekday, workingday, weathersit, temp, atemp, hum, windspeed, casual, registered  

- **Objective:**  
  To build a statistically sound regression model that identifies key factors influencing bike rental demand and provides reliable predictions for operational decisions.

---

## Conclusions
- **Conclusion 1:**  
  Categorical variables such as **season, year, and weather situation** significantly impact bike demand. Summer and fall months see higher usage, while demand drops during cold or rainy periods.
  
- **Conclusion 2:**  
  The **temperature (`temp`)** has a strong positive influence on rentals — higher temperatures correspond to higher usage, while **weather_situation**, **windspeed** negatively impacts demand.
  
- **Conclusion 3:**  
  When `registered` and `casual` variables were included, the model achieved a perfect R² due to direct dependence with `cnt`. Excluding these variables produced a more realistic and interpretable model.
  
- **Conclusion 4:**  
  The final model (built using **RFE-based feature selection**) identified **temperature (`temp`)**, **year (`yr`)**, and **weather situation(`weather_sit_3(Light/Show/Rain`))** as the top three features explaining bike rental demand, with an R² ≈ 0.75 on test data — showing good generalization.

---

## Technologies Used
- **Python** - version 3.11  
- **pandas** - version 2.2.2  
- **numpy** - version 1.26.4  
- **matplotlib** - version 3.8.3  
- **seaborn** - version 0.13.2  
- **scikit-learn** - version 1.5.1  
- **statsmodels** - version 0.14.2  

---

## Acknowledgements
- Dataset Source: UPgrad AL/ML  

---

## Contact
Created by [@AnirudhaKundu] — feel free to contact me for collaboration or questions!

