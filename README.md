# 🌍 Air Pollution and Respiratory Disease Analytics — Lagos Case Study

## 📌 Project Overview
This project analyzes the relationship between **air pollution and respiratory diseases** in Lagos, Nigeria — Africa’s largest city with 20+ million residents.  
The study was conducted as part of an internship project with **DataVerse Africa**.

Lagos faces severe **air pollution challenges** driven by:
- Traffic congestion
- Diesel generators
- Industrial emissions
- Open waste burning  

The goal was to **understand pollution–health dynamics** and build **predictive models** that can provide early warnings for respiratory disease surges.

---

## 🎯 Objectives
- Derive a **composite pollution index** from pollutants (PM2.5, PM10, NO2, SO2, O3).  
- Monitor air pollution **trends and seasonality** across Lagos districts.  
- Analyze the **relationship between pollution spikes and respiratory hospital cases**.  
- Build **predictive models** to forecast respiratory disease surges **3–7 days in advance**.  
- Identify **high-risk districts** and **vulnerable populations**.  
- Provide **policy and public health recommendations** for Lagos State.  

---

## 🗂️ Data Description
- **Datasets:**  
  - `lagos_air_pollution_health_data.xlsx`  
  - `lagos_air_pollution_health_data_1.xlsx`  

- **Features (16):**
  - City, Date, Hospital ID  
  - Pollutants: pm2_5, pm10, no2, so2, o3  
  - Respiratory cases, Average patient age  
  - Weather: temperature, humidity, wind_speed, rainfall_mm  
  - Socio-environmental: population_density, industrial_activity_index  

- **Records:** ~293,000 after cleaning & merging  

---

## 🔧 Methodology
1. **Data Cleaning & Wrangling**
   - Normalized column names, fixed inconsistencies, dropped duplicates.  
   - Median imputation for missing numeric values, cleaned city names & hospital IDs.  
   - Converted dates, created seasonal features: *Harmattan (Dec–Feb), Rainy (Apr–Oct), Dry (Nov & Mar)*.

2. **Feature Engineering**
   - Composite Pollution Index (raw & standardized).  
   - Time-based features (year, month, quarter, day of year).  
   - Aggregated to **city–day** granularity.  

3. **Exploratory Data Analysis**
   - Seasonal pollution patterns (Harmattan peaks, Rainy relief).  
   - City-level respiratory case distributions.  
   - Correlation analysis between pollutants, weather, and health outcomes.  

4. **Modeling**
   - Baseline: Linear Regression  
   - Main: Random Forest & Tuned Random Forest  
   - Evaluation: R², MAE, RMSE  

---

## 📊 Key Findings
- **Seasonal Pollution Cycles:**  
  - Harmattan (Dec–Feb): Highest pollution (~56–60 index).  
  - Rainy Season (Jun–Sep): Lowest pollution (~42–45 index).  

- **Health Burden:**  
  - **Ikeja & Yaba:** Highest respiratory case burdens (peaks >1,000 cases/day).  
  - **Ajah:** Lowest burden (~50–150 daily).  

- **Pollution–Health Link:**  
  - Weak direct correlations between individual pollutants & cases.  
  - Composite Pollution Index performed slightly better.  
  - **Rainfall emerged as the strongest predictor**, followed by wind speed and humidity.  

- **Model Performance:**  
  - Linear Regression Test R²: 0.71  
  - Random Forest Test R²: 0.74  
  - Tuned RF Test R²: 0.75 (best performance)  

---

## 📝 Recommendations
- **Weather-responsive interventions:** Align hospital surge planning with rainfall & Harmattan forecasts.  
- **Stronger monitoring:** Integrate air pollution + weather data into real-time dashboards.  
- **Targeted health campaigns:** Focus on high-risk groups (children, elderly) and high-density districts.  
- **Pollution source control:** Stricter regulation on traffic emissions, generator use, and open burning.  
- **Policy integration:** Merge predictive models into Lagos State’s urban planning and health response systems.  

---

## 🚀 Repository Contents
- `index.ipynb` → Jupyter Notebook (data cleaning, EDA, modeling, insights).  
- `Air Pollution and Respiratory Disease Analytics.pdf` → Internship presentation slides.  
- `README.md` → Project documentation (this file).  

---

## 👥 Contributors
- **Daniel Muruthi**  
- Don Alvin  
- Mellisa Matindi  

Supervised under **DataVerse Africa Internship**.  

---

## 📌 License
This project is for **educational and research purposes only**.  
Data is anonymized and used solely for public health insights.  

---
