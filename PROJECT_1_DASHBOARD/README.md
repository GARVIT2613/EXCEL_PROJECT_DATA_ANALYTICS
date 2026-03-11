# Electric Vehicle Market Intelligence & Infrastructure Analytics Dashboard  
<img width="1472" height="749" alt="P-1,DASHBOARD" src="https://github.com/user-attachments/assets/b4a32923-33af-4107-8c9c-7004584b26d6" />
=======
# ⚡ Electric Vehicle Market Intelligence & Infrastructure Analytics Dashboard

![Excel](https://img.shields.io/badge/Tool-Microsoft%20Excel-green)
![PowerQuery](https://img.shields.io/badge/ETL-Power%20Query-blue)
![PowerPivot](https://img.shields.io/badge/Data%20Model-Power%20Pivot-orange)
![DAX](https://img.shields.io/badge/Language-DAX-red)
![Status](https://img.shields.io/badge/Project-Completed-success)

---

# 📊 Dashboard Preview

<img width="1472" height="749" alt="P-1,DASHBOARD" src="https://github.com/user-attachments/assets/b4a32923-33af-4107-8c9c-7004584b26d6" />


## Dashboard File
The Excel dashboard file can be found here:  
[PROJECT-1_DASHBOARD.xlsx](https://github.com/user-attachments/files/25883496/PROJECT-1_DASHBOARD.xlsx)

---

# 📑 Table of Contents

- [Introduction](#introduction)
- [Project Objectives](#project-objectives)
- [Tools & Technologies Used](#tools--technologies-used)
- [Dataset Description](#dataset-description)
- [Data Preparation](#data-preparation)
- [Data Model](#data-model)
- [DAX Measures](#dax-measures)
- [Dashboard Components](#dashboard-components)
- [Charts & Visualizations](#charts--visualizations)
- [Interactive Filters](#interactive-filters)
- [Key Insights](#key-insights)
- [Conclusion](#conclusion)

---

# Introduction

The **Electric Vehicle Market Intelligence & Infrastructure Analytics Dashboard** analyzes global EV adoption trends, charging infrastructure availability, technological performance, and environmental impact.

This project demonstrates how **Microsoft Excel can be used as a Business Intelligence tool** by combining Power Query, Power Pivot, DAX measures, PivotTables, PivotCharts, and interactive slicers.

The dashboard enables users to explore key EV industry insights such as:

- Global EV adoption trends
- Manufacturer market share
- Battery technology efficiency
- Charging infrastructure readiness
- Environmental impact of EV adoption

---

# Project Objectives

The primary objectives of this project are:

1. Analyze EV adoption trends across years
2. Identify leading EV manufacturers
3. Compare EV adoption across countries
4. Evaluate EV battery efficiency
5. Assess charging infrastructure readiness
6. Measure environmental impact of EV adoption

---

# Tools & Technologies Used

| Tool | Purpose |
|-----|------|
| Microsoft Excel | Dashboard development |
| Power Query | Data cleaning and transformation |
| Power Pivot | Data modeling |
| DAX | KPI calculations |
| PivotTables | Data aggregation |
| PivotCharts | Data visualization |
| Slicers | Interactive filtering |

---

# Dataset Description

The dataset contains electric vehicle market data including:

- EV Brand
- Country
- Vehicle Type
- Year
- EV Sales Units
- Average EV Price
- Battery Capacity (kWh)
- Vehicle Range (km)
- Charging Stations
- CO₂ Reduction (Metric Tons)

This dataset allows analysis of EV market growth, technology efficiency, infrastructure readiness, and sustainability impact.

---

# Data Preparation

### Power Query (ETL Process)

Data preparation was performed using **Power Query**.

### Extract
Imported dataset containing EV market data.

### Transform
Performed the following transformations:

- Changed column data types
- Removed null values
- Cleaned text values
- Created calculated columns

### Load
Loaded transformed data into **Power Pivot Data Model**.

---

# Data Model

The dashboard uses a **Power Pivot data model** with relationships between the following tables:  
- EV_Market
- ChargingStations
- Country
- Date_Table


Relationships were created using:

- Country
- Year
- Brand

This structure enables efficient DAX calculations.

---

# DAX Measures

Below are all the **DAX measures used in the dashboard**.

---

## Total EV Sales

```
Total EV Sales :=
SUM(EV_Market[ev_sales_units])
```
Purpose:    
Calculates total EV units sold.

## Average EV Price

```
Total Charging Stations :=
SUM(EV_Market[charging_stations])
```

Purpose:  
Calculates average selling price of EVs.

## Total Charging Stations

```
Total Charging Stations :=
SUM(EV_Market[charging_stations])
```

Purpose:    
Calculates total charging infrastructure availability.

## Total Connectors

```
Total Connectors :=
SUM(ChargingStations[num_connectors])
```

Purpose:    
Measures total charging connectors available.

## Total CO2 Reduction

```
Total CO2 Reduction :=
SUM(EV_Market[co2_reduction_mt])
```

Purpose:  
Measures environmental impact from EV adoption.

## EV per Charging Station

```
EV per Charger :=
DIVIDE(
    [Total EV Sales],
    [Total Charging Stations]
)
```

Purpose:  
Measures charging infrastructure adequacy.

## EV Market Share %

```
EV Market Share % :=
DIVIDE(
    [Total EV Sales],
    CALCULATE([Total EV Sales], ALL(EV_Market))
)
```

Purpose:  
Calculates manufacturer market share.

## Average Battery Capacity

```
Avg Battery Capacity :=
AVERAGE(EV_Market[battery_capacity_kwh])
```

Purpose:  
Analyzes EV battery technology.

## Average Vehicle Range

```
Avg Vehicle Range :=
AVERAGE(EV_Market[vehicle_range_km])
```

Purpose:  
Analyzes EV driving range capability.

# Dashboard Components

The dashboard consists of several interactive components that provide insights into the electric vehicle ecosystem.

The main sections of the dashboard include:

1️⃣ **KPI Summary Cards**  
2️⃣ **Brand Wise Market Share Analysis**  
3️⃣ **EV Usage Across Countries**  
4️⃣ **EV Sales Trend Over Time**  
5️⃣ **Battery Capacity vs Vehicle Range Analysis**  
6️⃣ **Interactive Filters (Slicers)**

These elements work together to provide a comprehensive overview of EV market performance.

---

# Charts & Visualizations

## Brand Wise Market Share

<img width="670" height="345" alt="P-1,PIE" src="https://github.com/user-attachments/assets/91283a2f-61f7-4aef-860e-4b1a8aca4ff3" />

This **pie chart** visualizes the market share of different EV manufacturers.

### Excel Features
- PivotTable
- PivotChart (Pie Chart)

### Data Used
- EV Brand
- Total EV Sales

### Insights
This chart highlights the competitive distribution of EV manufacturers in the market and helps identify dominant brands.

---

## EV Usage by Country

<img width="870" height="401" alt="P-1,MAP CHART" src="https://github.com/user-attachments/assets/cc8f3a73-1304-4702-a381-a5f187acf3b1" />

This **map chart** shows the geographic distribution of EV usage across different countries.

### Excel Features
- Excel Map Chart
- PivotTable aggregation

### Data Used
- Country
- Total EV Sales

### Insights
The map allows users to quickly identify regions with high EV adoption and compare EV penetration globally.

---

## Number of EVs Purchased by Year

<img width="769" height="405" alt="P-1,LINE" src="https://github.com/user-attachments/assets/ddf62468-8e38-4221-9d0a-99d61fe7f965" />

This **line chart** represents EV adoption growth over time.

### Excel Features
- PivotTable
- PivotChart (Line Chart)

### Data Used
- Year
- Total EV Sales

### Background Data

<img width="248" height="420" alt="P-1,LINE TABLE" src="https://github.com/user-attachments/assets/d8d91bf0-6731-41ec-8b9f-9431c40cf452" />

### Insights
The chart clearly shows a steady increase in EV purchases from **2010 to 2026**, indicating strong market growth.

---

## Battery Capacity Impact on Vehicle Range

<img width="771" height="375" alt="P-1,SCATTER" src="https://github.com/user-attachments/assets/bc6d1f20-cd10-436a-9b1d-fbf5d4b158a9" />

This **scatter plot** analyzes the relationship between battery capacity and driving range for different EV brands.

### Excel Features
- Scatter Plot Chart
- PivotTable aggregation

### Axes

X-Axis:
- Average Battery Capacity (kWh)

Y-Axis:
- Average Vehicle Range (km)

### Background Data
  
<img width="551" height="301" alt="P-1,SCATTER TABLE" src="https://github.com/user-attachments/assets/8478c541-aa07-4143-b236-23ed9304ce70" />

### Insights
Brands with larger battery capacity generally achieve higher vehicle range, although efficiency varies across manufacturers.

---

# Interactive Filters

The dashboard includes **interactive slicers** that allow users to dynamically filter the data.

---

## Brand Filter

<img width="150" height="357" alt="P-1,BRAND SLICER" src="https://github.com/user-attachments/assets/e5fd7b3d-c3cf-4099-b75b-4fbc117e51ac" />

This slicer allows users to filter dashboard metrics by EV manufacturer.

Available brands include:

- BMW
- BYD
- Ford
- Hyundai
- Kia
- Mercedes
- Nissan
- Tesla
- Toyota
- Volkswagen

All visualizations update dynamically when a brand is selected.

---

## Vehicle Type Filter

<img width="135" height="202" alt="P-1,VEHICLE SLICER" src="https://github.com/user-attachments/assets/82154aba-ea20-43c3-bae0-662bd82a2a5e" />

This slicer filters the dashboard based on vehicle category.

Available vehicle types:

- Bus
- Car
- SUV
- Truck

This allows users to analyze EV trends across different vehicle segments.

---

# Key Insights

From the dashboard analysis, several important insights emerge:

- EV adoption has **steadily increased over time**, indicating strong market growth.
- Multiple EV manufacturers compete for market share, showing a diverse and competitive industry.
- EV adoption varies significantly across countries.
- Higher battery capacity generally results in greater vehicle range.
- The transition to electric vehicles contributes significantly to **reducing carbon emissions globally**.

---

# Conclusion

This project demonstrates how Microsoft Excel can be used as a powerful **data analytics and business intelligence tool**.

By combining **Power Query for data preparation, Power Pivot for data modeling, DAX measures for calculations, and PivotCharts for visualization**, the dashboard provides a comprehensive analysis of the electric vehicle industry.

The dashboard highlights important aspects of the EV ecosystem including:

- Market growth trends
- Manufacturer competition
- Infrastructure readiness
- Technological performance
- Environmental sustainability

This analysis emphasizes the growing importance of electric vehicles and the role of data-driven insights in understanding the future of sustainable transportation.
