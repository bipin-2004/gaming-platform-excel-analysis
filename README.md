# 🎮 Gaming Platform Player & Transaction Analysis

An Excel-based data analytics project focused on understanding gaming player engagement, monetization, platform performance, regional activity, session outcomes, and suspicious activity.

The project uses Microsoft Excel for data cleaning, feature engineering, KPI development, PivotTable analysis, PivotCharts, and interactive dashboard creation.

---

## 📊 Interactive Dashboard

![Gaming Platform Dashboard](images/dashboard.png)

The interactive dashboard provides a consolidated view of player activity, revenue, engagement, platform performance, purchasing behavior, and session outcomes.

### Dashboard Features

- 8 KPI cards
- 8 analytical visualizations
- 6 interactive slicers
- PivotTables and PivotCharts
- Dynamic KPI analysis

### Interactive Filters

- Region
- Platform
- Game Name
- Purchase Type
- Player Type
- Year-Month

---

## 🎯 Project Objectives

The main objectives of this project were to:

- Analyze player engagement and gaming session activity
- Understand purchasing and monetization behavior
- Compare performance across gaming platforms
- Analyze game-level performance
- Identify regional differences in gameplay
- Evaluate session success and failure
- Examine suspicious gaming activity
- Build an interactive business intelligence dashboard
- Generate actionable business insights and recommendations

---

## 📁 Dataset

The dataset contains **500 gaming session records** and **14 original columns**.

### Dataset Fields

| Field | Description |
|---|---|
| Session ID | Unique gaming session identifier |
| Player ID | Player identifier |
| Player Name | Player name |
| Game Name | Name of the game |
| Platform | Gaming platform |
| Region | Player/session region |
| Session Date | Date and time of the session |
| Session Duration (min) | Duration of gameplay |
| In-Game Purchase ($) | Purchase amount |
| Purchase Type | Type of purchase |
| Session Status | Session completion status |
| Player Type | Free/Paid player classification |
| Level Reached | Level reached during the session |
| Is Suspicious | Existing suspicious-session indicator |

### Dataset Overview

- **Total Sessions:** 500
- **Unique Players:** 489
- **Date Range:** 13-Dec-2024 to 13-Jun-2025
- **Total Revenue:** $2,631.27

---

## 🧹 Data Cleaning & Preparation

The dataset was reviewed and prepared for analysis by checking:

- Duplicate Session IDs
- Missing values
- Numerical values
- Date formatting
- Categorical consistency
- Purchase-related values

The `Purchase Type` value `"None"` was standardized to **`No Purchase`** to make the category easier to analyze.

### Numerical Validation

| Field | Minimum | Maximum |
|---|---:|---:|
| Session Duration | 5 min | 180 min |
| In-Game Purchase | $0 | $47.72 |
| Level Reached | 1 | 50 |

No negative values were identified in these numerical fields.

---

## ⚙️ Feature Engineering

Several derived columns were created to support deeper analysis.

### Year-Month

```excel
=TEXT([@[Session Date]],"yyyy-mm")
