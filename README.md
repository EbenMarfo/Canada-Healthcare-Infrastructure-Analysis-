# Canada-Healthcare-Infrastructure-Analysis-
An analysis of Canada's Healthcare Facilities using the StatCan ODHF dataset to audit regional infrastructure gaps in Google Sheets


# Canadian Healthcare Infrastructure & Data Quality Analysis

## Project Overview
This project delivers a comprehensive, data-driven audit of Canada's healthcare facility distribution using the **Open Database of Healthcare Facilities (ODHF)** dataset published by Statistics Canada. 

As an aspiring Data Analyst, I built this project entirely within **Google Sheets** to demonstrate advanced spreadsheet data modeling, structural data cleaning, categorical normalization, and executive-level stakeholder reporting.

📊 **[Access the Interactive Google Sheet Here **[(https://docs.google.com/spreadsheets/d/1lC_cAuoCADaZ5Dsnbifvu67QLpppSG77myqFA4jG8mQ/edit?usp=sharing)]**

---

## Key Business Insights
* **Infrastructure Dominance:** Long-term nursing and residential care facilities comprise the absolute majority of Canada's health infrastructure ecosystem, accounting for **52.1%** of all monitored facilities nationwide.
* **Critical Data Quality Warning:** A systematic audit of geographic data integrity revealed that **Alberta (AB)** has a severe reporting gap—**59.26%** of its listed facilities completely lack GPS coordinates, introducing high friction for spatial planning models.

---

## Core Data Pipeline & Methodology

### 1. Data Cleaning & Deduplication
* **Anomalies Corrected:** Removed multi-case formatting bugs in categorical data (e.g., lowercase vs proper case strings in facility types and city descriptions).
* **Entity Resolution:** Eliminated duplicate facility entries by running a multi-column uniqueness check against `facility_name` and `postal_code`.

### 2. Data Transformation Schema (Formulas Used)
To make the raw data analysis-ready, I engineered five dynamic tracking and lookup columns:

* **Standardized Facility Type (`Clean_Facility_Type`):** Formats mixed text inputs cleanly into Proper casing.
  ```excel
  =PROPER(D2)
