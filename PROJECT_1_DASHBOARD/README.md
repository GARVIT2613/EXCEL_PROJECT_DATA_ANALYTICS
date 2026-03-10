# ⚡ Electric Vehicle Market Intelligence & Infrastructure Analytics Dashboard

<img width="1472" height="749" alt="P-1,DASHBOARD" src="https://github.com/user-attachments/assets/b4a32923-33af-4107-8c9c-7004584b26d6" />

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
- [Project Structure](#project-structure)
- [Conclusion](#conclusion)

---

# Introduction

The **Electric Vehicle Market Intelligence & Infrastructure Analytics Dashboard** was built to analyze the rapidly growing EV industry using Microsoft Excel as a business intelligence tool.

This dashboard provides insights into:

- EV adoption trends
- Manufacturer market share
- Charging infrastructure availability
- Battery technology efficiency
- Environmental impact

The dashboard combines **Power Query, Power Pivot, DAX calculations, PivotTables, PivotCharts, and interactive slicers** to create a dynamic analytics tool.

---

# Project Objectives

The primary objectives of this project are:

1. Analyze EV market growth over time
2. Identify leading EV manufacturers
3. Compare EV adoption across countries
4. Evaluate EV battery efficiency
5. Assess charging infrastructure readiness
6. Measure environmental impact from EV adoption

---

# Tools & Technologies Used

| Tool | Purpose |
|-----|-------|
| Microsoft Excel | Dashboard development |
| Power Query | Data cleaning and transformation |
| Power Pivot | Data modeling |
| DAX | KPI calculations |
| Pivot Tables | Data aggregation |
| Pivot Charts | Data visualization |
| Slicers | Interactive filtering |

---

# Dataset Description

The dataset contains EV market and infrastructure data including:

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

---

## Average EV Price

```
Total Charging Stations :=
SUM(EV_Market[charging_stations])
```

Purpose:  
Calculates average selling price of EVs.

---

## Total Charging Stations

```
Total Charging Stations :=
SUM(EV_Market[charging_stations])
```

Purpose:    
Calculates total charging infrastructure availability.

---

## Total Connectors

```
Total Connectors :=
SUM(ChargingStations[num_connectors])
```

Purpose:    
Measures total charging connectors available.

---

## Total CO2 Reduction

```
Total CO2 Reduction :=
SUM(EV_Market[co2_reduction_mt])
```

