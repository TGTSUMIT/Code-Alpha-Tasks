# Code-Alpha-Tasks
📊 3 end-to-end Power BI dashboards — Sales Performance, HR Analytics &amp; Real Estate Market Trends | Power Query data cleaning | DAX measures | Interactive visuals | Full 20–30 page project documentation for each task
# 📊 Power BI Business Intelligence Projects — Task 1, 2 & 3

> A series of three end-to-end Business Intelligence dashboards built with **Microsoft Power BI**, covering Sales Performance Analytics, HR & Employee Analytics, and Real Estate Market Trends — each with full data cleaning, DAX measures, interactive visuals, and professional project documentation.

---

## 🗂️ Repository Structure


📁 main-project/
│
├── 📁 Task-1-Sales-Performance/
│   ├── TASK 1 DASHBOARD.pdf          # Power BI dashboard export
│   └── TASK 1 DOCUMENTATION.pdf      # Full project documentation
│
├── 📁 Task-2-HR-Analytics/
│   ├── TASK 2 DASHBOARD.pdf          # Power BI dashboard export
│   └── TASK 2 DOCUMENTATION.pdf      # Full project documentation
│
├── 📁 Task-3-Real-Estate/
│   ├── TASK 3 DASHBOARD.pdf          # Power BI dashboard export
│   └── TASK 3 DOCUMENTATION.pdf      # Full project documentation
│
└── README.md


---

## 📌 Project Overview

This repository contains three independent Power BI Business Intelligence projects completed as part of a Data Analytics internship/coursework program. Each project follows a full BI development lifecycle:

1. **Dataset sourcing and understanding**
2. **Data cleaning and transformation in Power Query**
3. **Data modeling and DAX measure development**
4. **Interactive dashboard design**
5. **Business insight generation and recommendations**
6. **Professional project documentation (20–30 pages each)**

---

## 🚀 Task 1 — Sales Performance Analytics Dashboard

### Objective
Analyze sales data to uncover revenue trends, product performance, regional sales distribution, and team KPIs to support strategic sales decisions.

### Key Features
| Feature | Detail |
|---|---|
| **KPI Cards** | Total Revenue, Total Orders, Average Order Value, Top Region, Top Product |
| **Visuals** | Revenue Trend (Line Chart), Sales by Region (Map), Product Performance (Bar Chart), Monthly Target vs Actual (Column Chart), Sales Rep Leaderboard |
| **Data Source** | Sales transactions dataset |
| **DAX Measures** | Total Revenue, MoM Growth %, YTD Revenue, Avg Deal Size, Win Rate |

### Business Questions Answered
- Which regions and products generate the most revenue?
- How does actual sales performance compare against monthly targets?
- Which sales representatives are top performers?
- What are the seasonal trends in order volume?

---

## 👥 Task 2 — HR & Employee Analytics Dashboard

### Objective
Provide HR teams and management with data-driven insights into workforce composition, attrition trends, department performance, and employee satisfaction metrics.

### Key Features
| Feature | Detail |
|---|---|
| **KPI Cards** | Total Employees, Attrition Rate, Average Tenure, Avg Salary, Active Headcount |
| **Visuals** | Attrition by Department (Bar Chart), Age Distribution (Histogram), Gender Diversity (Donut), Salary Band Analysis (Box Plot), Tenure vs Performance (Scatter Plot) |
| **Data Source** | HR employee records dataset |
| **DAX Measures** | Attrition Rate %, Avg Tenure, Headcount by Dept, Salary Variance, Performance Score Avg |

### Business Questions Answered
- Which departments have the highest attrition, and why?
- How is the workforce distributed across age groups and salary bands?
- Is there a correlation between tenure and performance ratings?
- What does gender and diversity composition look like across departments?

---

## 🏠 Task 3 — Real Estate Market Trends & Investment Analysis Dashboard

### Objective
Build an interactive real estate market intelligence dashboard to support investment decisions, developer planning, and buyer guidance by analyzing property prices, rental yields, supply-demand conditions, and geographic hotspots.

### Key Features
| Feature | Detail |
|---|---|
| **KPI Cards** | Total Properties, Avg Property Price, Avg Price/SQFT, Avg Area, Total Locations, Avg Bathrooms |
| **Visuals** | Avg Price by Location (Bar), Avg Price/SQFT by Location (Bar), Area vs Price (Scatter Plot), Property Listings Heatmap (Map), Price Category Distribution (Donut), Top Locations by Listings (Pie) |
| **Data Source** | Real Estate Data V21 — India property listings |
| **DAX Measures** | Total Properties, Avg Property Price, Avg Price/SQFT, Avg Area, Total Locations, Avg Bathrooms, Total Market Value |

### Data Cleaning Performed
- Removed duplicate property records
- Handled missing values in Price, Area, and Bathrooms columns
- Standardized location and city text formatting (Title Case + Trim)
- **Price format conversion:** `₹1.99 Cr → 19,900,000` | `₹48 L → 4,800,000`
- Created `Price_Numeric` column for mathematical operations
- Created `Price_Category` column: Budget / Mid-Range / Premium / Luxury
- Validated `Total_Area` range and removed outliers
- Computed `Price_per_SQFT` as a derived benchmarking column

### Business Questions Answered
- Which locations command the highest average property prices?
- Which areas offer the best value per square foot?
- Where are the property market hotspots geographically?
- How is the market distributed across Budget, Mid-Range, Premium, and Luxury segments?
- What is the relationship between property area and price?

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| **Microsoft Power BI Desktop** | Dashboard development, DAX measures, interactive visuals |
| **Power Query (M Language)** | Data extraction, transformation, and loading (ETL) |
| **DAX (Data Analysis Expressions)** | Custom KPI measures and calculated columns |
| **Microsoft Excel / CSV** | Source data format |
| **Python (future scope)** | ML-based price prediction integration |

---

## 📐 DAX Measures Reference — Task 3


// Total number of property listings
Total Properties = COUNTROWS('RealEstate')

// Average property price across visible rows
Avg Property Price = AVERAGE('RealEstate'[Price_Numeric])

// Average price per square foot
Avg Price per SQFT = AVERAGE('RealEstate'[Price_per_SQFT])

// Average property area in sq ft
Avg Area = AVERAGE('RealEstate'[Total_Area])

// Count of unique locations
Total Locations = DISTINCTCOUNT('RealEstate'[Location])

// Average bathroom count
Avg Bathrooms = AVERAGE('RealEstate'[Bathrooms])

// Total aggregate market value
Total Market Value = SUMX('RealEstate', 'RealEstate'[Price_Numeric])

---

📦 Data Sources

| Task | Dataset | Source |
|---|---|---|
| Task 1 | Sales Transactions | Internal / Kaggle |
| Task 2 | HR Employee Records | Internal / Kaggle |
| Task 3 | Real Estate Data V21 (India) | [Kaggle — India House Price Prediction](https://www.kaggle.com/datasets/ankushpanday1/india-house-price-prediction) |
| Task 3 (Supplementary) | NHB RESIDEX Housing Price Index | [nhb.org.in](https://www.nhb.org.in/data-graphs/) |
| Task 3 (Economic) | RBI Database on Indian Economy | [dbie.rbi.org.in](https://dbie.rbi.org.in/) |

---

📄 Documentation

Each task includes a comprehensive **20–30 page professional project report** covering:

- ✅ Cover Page, Certificate & Acknowledgement
- ✅ Abstract and Introduction
- ✅ Problem Statement and Objectives
- ✅ Dataset Description with column-level data dictionary
- ✅ Data Cleaning and Power Query transformation steps
- ✅ Dashboard design rationale for every visual
- ✅ KPI and DAX measure explanations
- ✅ Business insights (25+ per project)
- ✅ Actionable recommendations for stakeholders
- ✅ Conclusion, Future Scope, IEEE References, Appendix

---

🔮 Future Scope

- 🤖 **AI Price Prediction** — Integrate Python ML models (scikit-learn / XGBoost) via Power BI Python Visual
- 🌐 **Live Data Feed** — Connect to property listing APIs for real-time refresh
- 📱 **Mobile Dashboard** — Optimize layouts for Power BI Mobile app
- 🗺️ **Advanced GIS Mapping** — ArcGIS Maps integration for proximity analysis
- ☁️ **Cloud Deployment** — Publish to Power BI Service for web access and role-based sharing
- 📈 **Predictive Analytics** — Azure Machine Learning integration for demand forecasting

---

👤 Author

SUMIT PAWAR  
B-Tech | JG UNIVERSITY  
📧 sumitazure2039@gmail.com   

---

📃 License

This project is submitted for academic and portfolio purposes. The datasets used are publicly available and are credited to their respective sources. All dashboards, DAX measures, and documentation are original work by the author.

---

*Built with ❤️ using Microsoft Power BI*
