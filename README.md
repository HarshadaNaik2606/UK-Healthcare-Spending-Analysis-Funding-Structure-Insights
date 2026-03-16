# UK Healthcare Spending Trends & Funding Structure Analysis

## Project Overview

This project analyses UK healthcare expenditure between **1997 and 2012** to identify long-term spending trends, funding structure, and annual growth patterns. The analysis focuses on understanding how healthcare spending has evolved over time and the relative contribution of **public and private funding**.

The dataset was sourced from the **Office for National Statistics (ONS)** and processed using Python for data cleaning, SQL for analysis, and Power BI for interactive visualisation.

This project demonstrates an **end-to-end analytics workflow**, from raw data preparation to business insights and dashboard reporting.

---

## Objectives

- Analyse long-term trends in UK healthcare expenditure  
- Compare **public vs private healthcare funding**  
- Identify periods of significant spending growth  
- Create an **interactive dashboard** to support data-driven insights  

---

## Dataset

**Source:** Office for National Statistics (ONS)  
**Dataset:** UK Healthcare Expenditure (1997–2012)

The dataset includes:

- Total healthcare expenditure  
- Public sector healthcare expenditure  
- Private sector healthcare expenditure  
- Revision values between reporting years  

All values are reported in **£ billions (current prices)**.

---

## Tools & Technologies

- Excel (VLOOKUP, XLOOKUP, data validation, formulas)
- Python (Pandas, NumPy)
- SQL (SQLite)
- Power BI (dashboard visualisation)  

---

## Data Cleaning

The raw ONS statistical table required several preprocessing steps before analysis:

- Removed unnecessary header rows and formatting artefacts  
- Dropped empty and unnamed columns created by Excel formatting  
- Converted values to numeric data types  
- Created analytical fields including:
  - Public funding share (%)
  - Private funding share (%)
  - Year-on-year spending growth (%)

The cleaned dataset was exported for SQL analysis and dashboard development.

---

## SQL Analysis

SQL queries were used to explore key healthcare spending patterns, including:

- Healthcare spending trend over time  
- Public vs private funding distribution  
- Identification of the **highest year-on-year spending growth**

Example query:

```sql
SELECT
    year,
    total_2015,
    total_yoy_growth_pct_2015
FROM uk_healthcare_expenditure
ORDER BY total_yoy_growth_pct_2015 DESC
LIMIT 1;
```

This query identifies the year with the **highest healthcare spending growth**.

---

## Dashboard

An interactive **Power BI dashboard** was developed to visualise the analysis.
<img width="1167" height="665" alt="Screenshot 2026-03-16 172249" src="https://github.com/user-attachments/assets/0e30fbb3-7aa5-4a51-aabb-05cfb5002e2e" />



The dashboard includes:

- Key financial indicators (KPIs)
- Healthcare expenditure trend analysis
- Public vs private funding structure
- Year-on-year spending growth

The dashboard enables users to quickly understand how healthcare spending has evolved and how funding is distributed.

---

## Key Insights

- UK healthcare expenditure increased from **£54.9bn in 1997 to £146.7bn in 2012**, representing a **167% increase**.
- Public funding accounts for approximately **83% of total healthcare spending**, highlighting strong reliance on government funding.
- The **highest annual spending growth occurred in 2001 (~10%)**, indicating a significant period of healthcare investment.

---

## Repository Structure

```
uk-healthcare-spending-analysis
│
├── data
│   └── cleaned_healthcare_expenditure.csv
│
├── notebooks
│   └── data_cleaning.ipynb
│
├── sql
│   └── healthcare_analysis_queries.sql
│
├── dashboard
│   └── NHS_dashboard.pbix
│
└── README.md
```

---

## Project Outcome

This project demonstrates the ability to:

- Clean and prepare real-world statistical datasets  
- Perform analytical queries using SQL  
- Develop interactive business dashboards  
- Communicate data insights clearly for decision-making  

The workflow reflects the type of analysis performed in **data analyst and business analyst roles**, particularly within healthcare and public sector organisations.
