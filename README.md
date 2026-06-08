<div align="center">

# 🏠 Global Airbnb Performance Dashboard
### Power BI Dashboard | Marketplace Intelligence | Customer Analytics | Review Insights

<p align="center">

  <!-- Tech Stack -->

  <img src="https://img.shields.io/badge/Technology-Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black"/>
  <img src="https://img.shields.io/badge/DAX-0F6CBD?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Power_Query-217346?style=for-the-badge"/>

  <br>

  <!-- Analytics -->

  <img src="https://img.shields.io/badge/Analytics-Marketplace_Analytics-FF8C00?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Customer_Insights-00A86B?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Review_Intelligence-9370DB?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Behavioral_Analytics-008080?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Trust_Analysis-708090?style=for-the-badge"/>

  <br>

  <!-- Domain -->

  <img src="https://img.shields.io/badge/Domain-Travel_Analytics-success?style=for-the-badge"/>

  <br>

  <!-- Status -->

  <img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge"/>

</p>

### Transforming Airbnb Marketplace Data into Interactive Business Intelligence & Executive Insights

A premium multi-page Power BI dashboard project focused on Airbnb marketplace growth, customer engagement, ratings intelligence, review behavior, and host trust analytics using Power BI, DAX, and Power Query.

⭐ **If you found this project valuable, consider starring the repository!**

</div>

---

## 📖 Executive Summary

The **Global Airbnb Performance Dashboard** is an executive-style business intelligence solution designed to analyze Airbnb’s global marketplace performance across listings, ratings, reviews, customer behavior, and host trust dynamics.

The project combines:
- advanced analytics
- modern dashboard UI/UX
- business storytelling
- semantic modeling
- interactive navigation

to transform raw Airbnb marketplace data into actionable insights.

The dashboard focuses not only on reporting KPIs, but also on uncovering:
- marketplace growth patterns
- customer review behavior
- city-level performance
- seasonal travel trends
- host verification insights
- room type evolution
- marketplace maturity trends

---

## 🎯 Business Problem

Global marketplace platforms like Airbnb generate large volumes of listing, host, and review data.

Without centralized analytics dashboards, it becomes difficult to:
- monitor marketplace growth
- identify high-performing markets
- evaluate customer satisfaction
- understand traveler behavior
- analyze review engagement
- assess trust & verification dynamics

This project addresses these challenges through an interactive end-to-end Power BI analytics solution.

---

## Objectives

The project was designed to answer the following analytical questions:

| Business Question | Objective |
|---|---|
| How has Airbnb grown over time? | Marketplace growth analysis |
| Which cities dominate platform activity? | Market concentration analysis |
| Which room types drive Airbnb inventory? | Listing composition analysis |
| Which cities deliver the best guest experience? | Ratings intelligence |
| How engaged are Airbnb customers? | Review frequency analysis |
| What seasonal travel patterns emerge globally? | Seasonality analysis |
| How trustworthy is the host ecosystem? | Host verification analysis |

---

## 🗂 Dataset Overview

The dataset used in this project was sourced from Maven Analytics Data Playground.

🔗 Dataset Link:  
https://mavenanalytics.io/data-playground/airbnb-listings-reviews

The project uses Airbnb listing and review datasets containing:
- listing information
- pricing
- room types
- host details
- customer reviews
- review scores
- city-level marketplace data

## Core Tables

| Table | Type | Description |
|---|---|---|
| Listings | Fact/Dimension | Core Airbnb listing, pricing, host, and rating data |
| Reviews | Fact | Customer review activity and reviewer behavior |
| _Measures | Measure Table | Centralized DAX calculations and KPIs |
| Airbnb Data | Staging | Hidden source/staging table |

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| Power BI Desktop | Dashboard development & visualization |
| DAX | KPI engineering & analytical calculations |
| Power Query | Data cleaning & transformation |
| Data Modeling | Semantic model & relationships |
| GitHub | Version control & project hosting |

---

## 🏗 Architecture / Workflow

```text
Raw Airbnb Dataset
        │
        ▼
Power Query Data Cleaning & Transformation
        │
        ▼
Semantic Data Modeling
        │
        ▼
Relationship Engineering
        │
        ▼
Advanced DAX Calculations
        │
        ▼
Interactive Multi-Page Power BI Dashboard
```

---

## 📁 Repository Structure

```bash
Global_Airbnb_Performance_Dashboard/
│
├── Docs/
│   └── Images/
│       ├── Home Page.png
│       ├── Overview Page.png
│       ├── Ratings Page - 1.png
│       ├── Ratings Page - 2.png
│       └── Reviews Page.png
│
├── README.md
│
└── LICENSE
```

---

## 📊 Dashboard Pages

## Home Page

Premium landing page with custom navigation experience and Airbnb-inspired dashboard branding.

<img src="Docs/Dashboard Images/01_Home Page.png" width="100%"/>

---

## Overview Dashboard

Analyzes Airbnb marketplace growth, listing trends, and platform evolution.

### Key Analysis
- Marketplace growth lifecycle
- Listings by year
- Room type trends
- Host growth
- Platform maturity analysis

<img src="Docs/Dashboard Images/02_Overview Page.png" width="100%"/>

---

## Ratings Dashboard

Explores customer satisfaction, city performance, and pricing intelligence.

### Key Analysis
- Market concentration analysis
- Room pricing comparison
- City-level ratings
- Customer experience benchmarking
- Review score heatmaps

### Overall Ratings

<img src="Docs/Dashboard Images/03_Ratings Page - 1.png" width="100%"/>

### Detailed Ratings

<img src="Docs/Dashboard Images/04_Ratings Page - 2.png" width="100%"/>

---

## Reviews Dashboard

Analyzes customer review behavior, trust indicators, and travel seasonality.

### Key Analysis
- Review frequency analysis
- Customer engagement behavior
- Host trust matrix
- Seasonal travel patterns
- Verification analysis
  
<img src="Docs/Dashboard Images/05_Reviews Page.png" width="100%"/>

---

## 📊 Dashboard Analysis Performed

The project includes advanced analytical workflows across multiple dimensions.

### Analytical Areas Covered

✅ Marketplace growth analysis  
✅ Pareto contribution analysis  
✅ Customer ratings intelligence  
✅ Behavioral review analytics  
✅ Host trust analysis  
✅ Seasonal travel analysis  
✅ Dynamic KPI storytelling  
✅ Comparative city benchmarking  
✅ Review frequency analysis  
✅ Executive dashboard storytelling  
✅ Multi-page interactive navigation  


---

## 🧮 Advanced DAX Measures

### 1️⃣ Cumulative Reviewer Analysis

```DAX
Cumulative Reviewers =
VAR CurentReviews =
    MAXX( Reviews, Reviews[Reviews per Reviewer] )
RETURN
CALCULATE(
    DISTINCTCOUNT( Reviews[reviewer_id] ),
    FILTER(
        ALL( Reviews[Reviews per Reviewer] ),
        Reviews[Reviews per Reviewer] <= CurentReviews
    )
)
```

### 📌 Business Insight

> Calculates the running cumulative count of unique reviewers ordered by review frequency, enabling behavioral Pareto analysis.


### 2️⃣ Cumulative Reviewer Distribution %

```DAX
Cumulative % Rerview Frequency =
DIVIDE( 
    [Cumulative Reviewers], 
    CALCULATE( 
        [Total Reviewers], 
        ALL( Reviews[Reviews per Reviewer] ) 
    ) 
)
```

### 📌 Business Insight

> Measures the cumulative percentage contribution of reviewers based on review frequency to identify customer engagement concentration.


### 3️⃣ Monthly Review Share Analysis

```DAX
Total Reviews =
DISTINCTCOUNT( Reviews[review_id] )
```

```DAX
% of Monthy Reviews =
DIVIDE(
    [Total Reviews],
    CALCULATE(
        [Total Reviews],
        ALLSELECTED( Listings[city] )
    )
)
```

### 📌 Business Insight

> Calculates each city's share of total monthly reviews relative to selected cities, supporting seasonal and comparative review analysis.

---

## Key Business Insights

## Marketplace Growth

- Airbnb experienced rapid listing expansion between 2011–2015.
- Growth slowed during regulatory tightening in 2016–2017.
- Platform activity rebounded before declining sharply during the COVID-19 period.


## Market Concentration

- Paris, New York, and Sydney contribute a disproportionate share of listings and reviews.
- Paris remains the platform’s largest and most engaged marketplace.


## Customer Ratings

- Mexico City and Rio de Janeiro recorded the highest overall guest satisfaction.
- Cleanliness and value-for-money consistently scored lower than communication and location.


## Customer Review Behavior

- Most customers leave only a small number of reviews.
- Nearly all review activity is concentrated among low-frequency reviewers.


## Trust & Verification

- Fully verified hosts dominate the platform ecosystem.
- Anonymous and unverified host profiles represent only a minimal share of the marketplace.

---

## Data Cleaning & Transformation

The project involved extensive preprocessing and transformation:

- Standardized city-level marketplace data
- Engineered review frequency calculations
- Built trust verification matrix
- Created cumulative contribution measures
- Developed review seasonality logic
- Optimized semantic relationships
- Structured centralized DAX measure table
- Built analytical calculated columns
- Designed executive-focused KPI measures
- Implemented interactive storytelling visuals

---

## 📚 Key Learnings

## Technical Learnings

- Advanced Power BI dashboard engineering
- Semantic model design
- DAX KPI development
- Power Query transformation workflows
- Executive dashboard storytelling
- UI/UX dashboard optimization
- Analytical visualization techniques
- Behavioral analytics implementation

## Business Learnings

- Airbnb marketplace activity is highly concentrated in a few major cities
- Customer review behavior is dominated by low-frequency reviewers
- Entire-home listings increasingly dominate the platform
- Trust verification plays a major role in host ecosystem quality
- Seasonal travel behavior differs significantly across regions

---

## Future Improvements

Planned enhancements for the project:

- Drill-through city analysis
- Advanced tooltip pages
- Predictive trend forecasting
- Mobile-responsive dashboard layout
- Dynamic filter panel
- Geospatial city analysis
- Sentiment analysis integration

---

## 🌟 About Me

HHi there! I'm Kaustubh Sutar, a data enthusiast and aspiring Data Analyst & Data Engineer skilled in Power BI, SQL, Python, Excel, PySpark, and Databricks. I enjoy building scalable data pipelines, analyzing datasets, and creating dashboards that transform raw data into actionable business insights.

I also have growing interests in Data Engineering, Machine Learning, and AI, continuously exploring modern technologies to expand my analytical and engineering capabilities. 

Let's stay connected!

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/kaustubh-sutar-814134340/)

---

## ⭐ Support This Project

If you found this project insightful:

- ⭐ Star the repository
- 🍴 Fork the project
- 📢 Share it with others
- 💼 Connect for analytics collaborations

---

## 🛡️ License

This project is licensed under the [MIT License](LICENSE). You are free to use, modify, and share this project with proper attribution.
