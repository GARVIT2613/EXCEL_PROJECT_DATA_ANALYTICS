# Project Analysis: Electric Vehicle Market Intelligence

## Introduction

The electric vehicle (EV) industry has experienced rapid growth in recent years due to technological advancements, environmental concerns, and government policies encouraging sustainable transportation.

To better understand this growing market, I built an **Excel-based analytics project** that examines EV adoption trends, manufacturer market share, battery technology performance, charging infrastructure, and environmental impact.

Using Excel's advanced analytics features such as **Power Query, Power Pivot, PivotTables, DAX measures, and interactive charts**, this project explores the dynamics of the global EV ecosystem.

---

## Questions to Analyze

To understand the EV market, I explored the following questions:

1. **How does EV adoption vary across countries?**
2. **Which EV brand dominates the market?**
3. **How has EV adoption grown over time?**
4. **What is the relationship between battery capacity and vehicle range?**
5. **Is charging infrastructure keeping up with EV growth?**

---

## Excel Skills Used

The following Excel features were used for the analysis:

- 📊 Pivot Tables  
- 📈 Pivot Charts  
- 🧮 DAX (Data Analysis Expressions)  
- 🔍 Power Query (ETL Process)  
- 💪 Power Pivot (Data Modeling)

---

## EV Market Dataset

The dataset used for this project includes information related to electric vehicles and infrastructure.

The dataset contains the following variables:

- 🚗 EV Brand  
- 🌍 Country  
- 🚘 Vehicle Type  
- 📅 Year  
- 🔋 Battery Capacity (kWh)  
- 📏 Vehicle Range (km)  
- 🔌 Charging Stations  
- 💰 Average EV Price  
- 🌱 CO₂ Reduction (Metric Tons)

These variables allow us to analyze **EV adoption trends, infrastructure readiness, and technology performance**.

---

## 1️⃣ How does EV adoption vary across countries?

### 🔍 Skill: Pivot Tables & Map Charts

To analyze EV adoption across countries, I created a PivotTable summarizing **total EV sales by country** and visualized it using an **Excel Map Chart**.

### Pivot Table Setup

Rows: Country  

Values: Total EV Sales

--- 


### Visualization

<img width="1074" height="601" alt="ADOPTION ACROSS COUNTRIES" src="https://github.com/user-attachments/assets/652665f4-8e1d-46cf-b3c8-9168630c245a" />

### 💡 Insights

- Countries like **Canada, India, and France** show strong EV adoption levels.
- Developed markets tend to have higher EV sales due to better infrastructure and supportive policies.

### 🤔 So What

Understanding geographic distribution helps policymakers and companies identify regions where EV adoption is accelerating.

---

## 2️⃣ Which EV brand dominates the market?

### 📊 Skill: Pivot Charts (Pie Chart)

To understand brand dominance, I created a PivotTable calculating **market share of EV manufacturers**.

### Pivot Table Setup

Rows: EV Brand  

Values:EV Market Share %  


### Visualization

<img width="1572" height="559" alt="BRAND DOMINANCE" src="https://github.com/user-attachments/assets/c7bd9df9-72ef-4d65-ada4-719bf8088476" />

### 💡 Insights

- EV sales are distributed among multiple manufacturers.
- Companies such as **Toyota, Tesla, Mercedes, and Nissan** have significant market presence.

### 🤔 So What

Brand competition indicates a rapidly evolving EV market where multiple manufacturers are competing for leadership.

---

## 3️⃣ How has EV adoption grown over time?

### 📈 Skill: PivotTables & Line Charts

To analyze growth trends, I aggregated EV sales by year and plotted them using a line chart.

### Pivot Table Setup

Rows: Year  
Values: Total EV Sales


### Visualization

<img width="1322" height="501" alt="EV GROWTH" src="https://github.com/user-attachments/assets/2a6f1a5d-bcb6-47e1-bf81-3762be912b6e" />

### 💡 Insights

- EV sales have grown steadily since 2010.
- A sharp increase occurs after 2019, indicating accelerated market adoption.

### 🤔 So What

This growth suggests that electric vehicles are becoming mainstream and will likely continue expanding globally.

---

## 4️⃣ What is the relationship between battery capacity and vehicle range?

### 📉 Skill: Scatter Plot Analysis

To understand EV technology efficiency, I analyzed the relationship between battery capacity and driving range.

### Data Used

X-Axis: Average Battery Capacity (kWh)  
Y-Axis: Average Vehicle Range (km)


### Visualization

<img width="1208" height="425" alt="BATTERY CAP VS VEHICLE RANGE" src="https://github.com/user-attachments/assets/e45daaed-18db-4745-9873-761662824c85" />

### 💡 Insights

- Higher battery capacity generally leads to longer vehicle range.
- Some brands achieve better efficiency despite smaller battery sizes.

### 🤔 So What

This relationship helps evaluate technological efficiency across EV manufacturers.

---

## 5️⃣ Is charging infrastructure keeping up with EV growth?

### 🧮 Skill: DAX Calculations

To measure infrastructure readiness, I calculated **EV per Charging Station**.

### DAX Measure
```
EV per Charger :=
DIVIDE(
[Total EV Sales],
[Total Charging Stations]
)
```


### 💡 Insights

- A high EV-to-charger ratio may indicate infrastructure shortages.
- Countries investing in charging infrastructure may accelerate EV adoption.

---

## Data Preparation

### 🔍 Power Query (ETL Process)

The dataset was prepared using Power Query.

### Extract

Data was imported from multiple sources:

- EV Market dataset
- Charging Stations dataset
- Global EV Data dataset

### Transform

The following transformations were applied:

- Changed column data types
- Removed blank rows
- Removed duplicate records
- Filtered unnecessary rows
- Cleaned column values
- Created calculated columns

Example transformation steps:

- 📊EV_Market:
  
<img width="277" height="324" alt="STEPS,EV MARKET" src="https://github.com/user-attachments/assets/c5a4438d-e973-4a6a-8282-5d17d42ea8bf" />

- 🛠️ Charging_Stations:

<img width="277" height="267" alt="STEPS,STATIONS" src="https://github.com/user-attachments/assets/09493191-0b17-4ee5-839a-bf9b17d81652" />

  
- 📥 Global_Sales:

<img width="277" height="277" alt="STEPS,GLOBAL SALES" src="https://github.com/user-attachments/assets/a47d08ac-2b91-4d7b-a40d-f0372b55653c" />


### Load

The cleaned data was loaded into the Excel **Data Model** for analysis.

 - 📊EV_Market:

<img width="1720" height="980" alt="EV MARKET DATA LOAD" src="https://github.com/user-attachments/assets/382bd7da-f9f8-46ff-8984-78abb534a4e1" />


 - 🛠️ Charging_Stations:

<img width="1720" height="980" alt="STATIONS" src="https://github.com/user-attachments/assets/84a27f47-f0cf-404a-88d1-ff1230339f70" />


 - 📥 Global_Sales:

<img width="1720" height="980" alt="GLOBAL SALES" src="https://github.com/user-attachments/assets/251c02bc-95bb-4dd1-817d-5bad2c9894ba" />



## Data Model

Using **Power Pivot**, I created a data model connecting multiple tables.

### Tables Used

- EV_Market
- ChargingStations
- Country
- Date_Table

### Relationships

Relationships were created using:  
Country  
Year  


### Data Model Visualization

<img width="1125" height="654" alt="DATA MODEL" src="https://github.com/user-attachments/assets/4e2a6277-dcbe-4745-8601-cf7dc38eee2d" />

---

## Power Pivot

Power Pivot was used to create advanced calculations and manage relationships.

Example interface:

<img width="1621" height="824" alt="POWER PIVOT -1" src="https://github.com/user-attachments/assets/4ddca260-49b8-44b2-8499-45d12cbc9af9" />

---

## Key Insights

From the analysis, several insights emerge:

- EV adoption has increased dramatically over the last decade.
- Multiple manufacturers compete for market leadership.
- Battery capacity strongly influences vehicle range.
- EV adoption varies significantly across countries.
- Infrastructure development is critical for supporting EV growth.

---

## Conclusion

This project demonstrates how Excel can be used as a powerful analytics platform to analyze emerging industries such as electric vehicles.

By leveraging **Power Query for data preparation, Power Pivot for data modeling, DAX for calculations, and PivotCharts for visualization**, the analysis reveals key trends in EV adoption, infrastructure readiness, technological performance, and market competition.

The results highlight the rapid transformation of the global transportation sector toward sustainable mobility.



