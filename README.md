# 🏏 IPL Analysis Dashboard (Power BI)

<p align="center">
  <img src="images/dashboard_overview.png" width="800"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Tool-Power%20BI-yellow?style=for-the-badge&logo=powerbi"/>
  <img src="https://img.shields.io/badge/Language-DAX-blue?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Data-Analytics-green?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Project-Interactive%20Dashboard-orange?style=for-the-badge"/>
</p>

---

## 📌 Project Overview

This project presents an **interactive IPL (Indian Premier League) dashboard** built using Power BI.
It transforms raw cricket datasets into **meaningful insights** about player performance, team analysis, and season trends.

---

## 🎯 Objectives

* Analyze **player performance across IPL seasons**
* Identify **Orange Cap (top scorer)** and **Purple Cap (top wicket-taker)**
* Track **team performance and match outcomes**
* Build a **fully interactive dashboard** with dynamic filtering

---

## 📁 Dataset Used

* 📄 `ball_by_ball_data.csv` → Ball-level match data
* 📄 `ipl_matches_data.csv` → Match results & season info
* 📄 `players_data.csv` → Player details + images
* 📄 `teams_data.csv` → Team information

---

## 🚀 Key Features

### 🔥 KPI Metrics

* Total Runs
* Total Fours & Sixes
* Total 50s & 100s
* Total Dot Balls

### 🏆 Advanced Insights

* 🟠 Orange Cap Holder (Top Run Scorer)
* 🟣 Purple Cap Holder (Top Wicket Taker)
* 💥 Most Sixes by Player
* 📊 Team Performance Analysis
* 📅 Season-wise Trends

### 🎛️ Interactivity

* Dynamic slicers (Season, Team, Player)
* Drill-through for detailed player analysis
* Tooltips with additional insights
* Cross-filtering across visuals

---



## 🧠 Data Modeling

* Designed using **Star Schema**
* Optimized relationships between:

  * Matches ↔ Ball-by-Ball
  * Players ↔ Performance
  * Teams ↔ Results
* Improved performance using **efficient cardinality & filtering**

---

## 📐 DAX Highlights

```DAX
Total Runs = SUM(ball_by_ball_data[batsman_runs])

Total Sixes = CALCULATE(
    COUNTROWS(ball_by_ball_data),
    ball_by_ball_data[batsman_runs] = 6
)

Strike Rate = 
DIVIDE([Total Runs], [Total Balls Faced]) * 100
```

👉 Includes advanced measures like:

* Orange Cap
* Purple Cap
* Fifties & Hundreds
* Top N Players

---

## 🎨 UI/UX Design

* 🎯 Dark Theme Dashboard (Cricket Inspired)
* 🟠 Orange & 🟣 Purple highlight colors
* 📊 Clean layout with KPI cards & charts
* 🔤 Professional typography (Segoe UI)

---

## 🛠 Tools & Technologies

* Power BI
* DAX (Data Analysis Expressions)
* Data Modeling
* CSV Data Processing

---

## 📂 Project Structure

```
IPL-PowerBI-Dashboard/
│
├── IPL_Dashboard.pbix
├── datasets/
├── images/
├── docs/
└── README.md
```

---

## ▶️ How to Use

1. Download the `.pbix` file
2. Open in Power BI Desktop
3. Load datasets if required
4. Interact using slicers & filters

---

## 💡 Key Insights

* Identifies top-performing players across seasons
* Highlights players with most sixes and consistency
* Reveals team dominance trends
* Enables deep drill-down into player statistics

---

## 🚀 Future Enhancements

* Live IPL data integration
* Predictive analytics (Player performance)
* Advanced AI visuals

---

## 🙌 Author

**Madhur Sisodiya**
📊 Aspiring Data Analyst | Power BI Enthusiast

---

## ⭐ Support

If you like this project, give it a ⭐ on GitHub!
