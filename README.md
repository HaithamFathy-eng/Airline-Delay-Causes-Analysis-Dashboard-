# The File was too large, so it is splitted into 6 zip files

# ✈️ Power BI – Airline Delay Causes Dashboard

This project was developed as part of my **ITI Scholarship** to analyze and visualize airline delay patterns using **Microsoft Power BI** and real-world data from **Kaggle**.

---

## 📊 Project Overview

The goal of this project is to identify trends, causes, and performance patterns related to flight delays across various airlines and airports in the United States.

**Data Source:**
[Airline Delay Causes – Kaggle Dataset](https://www.kaggle.com/datasets/giovamata/airlinedelaycauses)

---

## 🧠 Key Objectives

1. Connect and clean raw flight delay data in Power BI
2. Create a **Date Table** using DAX for time intelligence functions
3. Build **DAX Measures** for performance analysis
4. Design a **multi-page interactive dashboard** with meaningful insights
5. Apply creative visuals and drillthrough navigation for user-friendly exploration

---

## ⚙️ DAX Measures

Example measures used in the dashboard:

```DAX
-- Total Delay Minutes
Total Delay Minutes =
SUM('Airline_Delay_Causes'[CarrierDelay]) +
SUM('Airline_Delay_Causes'[WeatherDelay]) +
SUM('Airline_Delay_Causes'[NASDelay]) +
SUM('Airline_Delay_Causes'[SecurityDelay]) +
SUM('Airline_Delay_Causes'[LateAircraftDelay])

-- Average Delay Minutes
Average Delay Minutes =
DIVIDE([Total Delay Minutes], COUNTROWS('Airline_Delay_Causes'))

-- Total Delayed Flights
Total Delayed Flights =
CALCULATE(COUNTROWS('Airline_Delay_Causes'),
    'Airline_Delay_Causes'[Total Delay Minutes] > 0
)
```

---

## 🖥️ Dashboard Pages

### 1️⃣ **Overview Page**

* High-level KPIs (Total Flights, Delayed Flights, Average Delay Minutes)
* Trends over time using line and area charts
* Slicers for Year, Airline, and Airport

### 2️⃣ **Delay Cause Analysis**

* **Bar Chart** for delay minutes by cause
* **Decomposition Tree** to explore delay reasons interactively
* **Treemap** showing the proportion of each delay cause

### 3️⃣ **Carrier & Airport Performance**

* Compare airlines and airports by delay frequency and duration
* Performance rankings and heatmaps for visual clarity

---

## 🧩 Bonus Features

* **Time Dimension Table** for advanced DAX date intelligence
* **Drillthrough Pages** for in-depth performance details
* **Creative and consistent design theme** for professional storytelling

---

## 📁 Repository Structure

```
📦 PowerBI-Airline-Delay-Causes
 ┣ 📄 README.md
 ┣ 📊 AirlineDelay.pbix
 ┣ 📑 Data/
 ┃ ┗ airline_delay_causes.csv
 ┗ 📸 Screenshots/
   ┣ Overview_Page.png
   ┣ Delay_Cause_Page.png
   ┗ Carrier_Performance_Page.png
```

---

## 🏆 Outcome

Delivered an interactive Power BI dashboard providing insights into:

* Top causes of flight delays
* Seasonal delay trends
* Airline and airport performance benchmarks

---
