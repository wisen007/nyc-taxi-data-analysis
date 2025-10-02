# nyc-taxi-data-analysis
Power BI project analyzing NYC taxi trips 2017–2020 to compare pre- and during-pandemic trends

# 🚖 NYC Taxi Trips Dashboard: Pre & During the Pandemic

Do you remember the pandemic — nose masks, no contact, and the economic downturn?  
I wanted to see how the taxi business was affected during 2020, the year of the pandemic.  

This project uses NYC Taxi trip data (2017–2020) to explore **trends in ridership, fares, and distances**, and to build a **Power BI dashboard** that highlights how badly the industry was hit.

---

# 🎯 Project Objectives  

This project analyzes **NYC taxi trip data (2017–2020)** to understand the impact of the COVID-19 pandemic and uncover key insights about rider behavior.  

## Main Goals  
- **Pandemic Impact** → Explore how the pandemic disrupted taxi trip volumes, fares, and distances.  
- **Comparative Trends** → Compare trips, fares, and distances before and during the pandemic years.  
- **Forecasting** → Build *“with pandemic”* vs. *“without pandemic”* forecasting scenarios.  
- **Key Metrics to Answer**:  
  - What is the **average number of trips**?  
  - What is the **average fare per trip**?  
  - What is the **average distance traveled per trip**?  
  - How will **trip volume change relative to last week**?  
- **Demand Patterns**:  
  - Which **days of the week** and **times of day** are busiest?  
  - What are the **most popular pick-up and drop-off locations**?  
- **Dashboard Design** → Deliver a clean, interactive, and **user-friendly Power BI dashboard** that allows filtering and exploration by **location, day of the week, and time of day**.  

---

## 📊 Dataset
- **Source**: NYC Taxi dataset (Maven Analytics Challenge / NYC Open Data).  
- **Period covered**: 2017 – 2020.  
- **Key columns used**:  
  - Pickup location, Drop-off location  
  - Date, Fiscal Week, Day of week, Hour of day  
  - Fare amount, Trip distance  

---

## 🔧 Process

### 1. Data Cleaning (Power Query)
- Removed unused columns.  
- Standardized dates and created Fiscal Weeks.  
- Joined trips with calendar and zone lookup tables.  

### 2. Data Modeling
- Created a  schema:
  - `taxi_trips` fact table  
  - `calendar` dimension  
  - `pickup_zones` and `dropoff_zones` dimensions  
- Relationships ensure correct filtering for time, location, and trips.  

### 3. DAX Measures
- `[Total Trips]` → counts total rides.  
- `[Fare per Trip]` → total fare ÷ total trips.  
- `[Distance per Trip]` → total distance ÷ total trips.  
- **Estimates**:  
  - *With Pandemic* → uses 2017–2020 averages/min.  
  - *Without Pandemic* → uses 2017–2019 averages/max.  
- `[WoW Change]` → compares current week to previous week.  
- **Narrative Text** → generates plain-language summary for users.  

### 4. Visualization
- **Map** → popular pickup/drop-off zones.  
- **Bar Charts** → busiest days of the week & hours of the day.  
- **Table** → fiscal year comparison of trips, fares, distances, WoW.  
- **Narrative Card** → dynamic text summarizing insights.  

---

## 📷 Dashboard Preview

![Dashboard Screenshot](images/nyc-dashboard.png)[http://bit.ly/46QQrLf]

---

## 🔑 Key Insights
- Trips dropped massively in 2020 due to the pandemic.  
- Average fare per trip slightly increased.  
- Distance per trip remained stable.  
- Fridays & Saturdays remained the busiest, even during downturn.
- Between 5pm and 7pm was the busiest times during almost all the weeks and this may be due to people returning home from work and other activities.
- The least busiest times was between 3am to 5 am and after it begins to pickup showing the day had began for most people
- East harlem north and east harlem south are the busiest pickup and drop off locations recording an about 13% of the total trips for the four years

---


---

## 🛠 Tech Stack
- **Power BI** → data modeling, visualization, storytelling.  
- **Power Query** → ETL (cleaning, transformations).  
- **DAX** → measures(WOW), business logic, dynamic text,.  

---

## 📌 About
This project was created as part of the **Maven Analytics Data Challenge** and to showcase my ability to:  
- Transform raw datasets into insights.  
- Apply DAX for calculations and narratives.  
- Build interactive dashboards for decision-making.
- This dashboard is a replica of the one by the winner Zoe Douglas which one the maven challenge in 2021

---
