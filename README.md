**Project Title**: General Health Services and Disease Data in Kenya  
**Team Members**:  
- Mitchelle – Exploratory Data Analysis  
- Tumaini – Insight and Storytelling  
- Bophine – Data Cleaning and Enrichment  
- Aime – Data Mining  
- Allan – README & Documentation  

## 🎯 Project Objectives & Deliverables

| Role | Responsibilities | Deliverables |
|------|------------------|--------------|
| **Mitchelle** | Conduct EDA: distributions, trends, correlations, outliers | Jupyter notebook with visualizations; summary statistics |
| **Tumaini** | Translate findings into narratives; identify policy implications | Story-driven report; presentation slides |
| **Bophine** | Clean, validate, enrich data; document data quality issues | Cleaned dataset; data dictionary; quality report |
| **Aime** | Apply data mining: clustering, anomaly detection, forecasting | Predictive models; pattern analysis (e.g., disease hotspots) |
| **Allan** | Coordinate documentation; maintain README and project log | This README; project proposal; version control via Git |

---

## 📌 Project Overview

This project explores **general health services and disease burden indicators in Kenya**, using a comprehensive dataset sourced from **Kaggle**. The dataset includes a wide array of health metrics spanning communicable and non-communicable diseases, environmental health risks, health system capacity, universal health coverage (UHC) indices, and demographic health outcomes from as early as 1974 up to projected values for 2025.

Our goal is to:
- Understand the evolution of Kenya’s health landscape over time.
- Identify key disease burdens and health service gaps.
- Evaluate progress toward national and global health targets (e.g., SDGs, UHC).
- Provide actionable insights for policymakers, public health practitioners, and researchers.

---

## 📁 Dataset Description

### Source
- **Primary Source**: [Kaggle – Health Indicators in Kenya](https://www.kaggle.com/datasets/idrissssaaaa/health-indicators-in-kenya)
- **File Name**: `Health_Indicators_In_Kenya.csv`
- **Geographic Scope**: Kenya (KEN), Africa Region (AFR)
- **Temporal Coverage**: 1974 – 2025 (includes historical data and future projections)

### Key Indicator Categories
1. **Non-Communicable Diseases (NCDs)**  
   - Deaths and DALYs (Disability-Adjusted Life Years) from cardiovascular diseases, diabetes, cancers, chronic respiratory diseases.
   - Availability of NCD care (e.g., dialysis, stroke management, national guidelines).

2. **Communicable Diseases & Neglected Tropical Diseases (NTDs)**  
   - Measles, polio, tetanus, cholera, Buruli ulcer, leishmaniasis, onchocerciasis, trachoma.
   - Treatment coverage and case reporting.

3. **Environmental Health**  
   - Population relying on solid fuels for cooking.
   - Ambient and household air pollution attributable DALYs.
   - Water, sanitation, and hygiene (WASH)-related disease burden.

4. **Health System & Service Coverage**  
   - UHC Service Coverage sub-indices (reproductive/maternal/child health, infectious diseases).
   - Mental health infrastructure (beds, facilities, workforce).
   - External and domestic health expenditure.

5. **Risk Factors & Behavioral Indicators**  
   - Alcohol consumption (recorded/unrecorded), alcohol-attributable deaths.
   - Tobacco control policies (smoke-free laws, quitline availability).
   - Road traffic injuries and vehicle data.

6. **Demographic & Life Expectancy Metrics**  
   - Life expectancy at birth and at age 60.
   - Healthy Life Expectancy (HALE).

7. **Governance & Policy**  
   - National strategies for NCDs, eHealth, UHC.
   - IHR (International Health Regulations) core capacities.

### Data Structure
- **Format**: CSV (comma-separated values)
- **Fields** (selected):  
  - Indicator ID (e.g., `SA_0000001418`, `WHS3_62`)
  - Indicator name/description
  - Metadata URL (where applicable)
  - Year(s)
  - Country (Kenya)
  - Sex disaggregation (Male, Female, Both)
  - Disease category (where applicable)
  - Numeric value (point estimate)
  - Confidence intervals (lower/upper bounds, where available)
  - Qualitative responses (e.g., “Yes”, “No”, “No data”)

---

## 🔧 ETL Pipeline Overview

### 1. **Extract**
- Load raw CSV file into a data processing environment (e.g., Python/Pandas, R, or SQL).
- Validate file integrity and encoding.

### 2. **Transform**
- **Standardize column names** and data types.
- **Parse multi-value fields** (e.g., confidence intervals like `15959 [10073-23322]` → separate columns).
- **Handle missing data**:  
  - “No data”, “.”, “missing data” → `NaN`  
  - Impute or flag based on context.
- **Normalize indicator metadata**:  
  - Map indicator IDs to human-readable categories.
  - Extract sex, age group, disease type from structured fields.
- **Create derived metrics**:  
  - % change over time  
  - Disease burden per capita  
  - Gender disparity ratios

### 3. **Load**
- Store cleaned data in analysis-ready format:
  - Long-format table for time-series analysis
  - Wide-format for cross-sectional dashboards
- Export to:
  - Parquet/CSV for sharing
  - Database (e.g., SQLite, PostgreSQL) for querying
  - Visualization tools (e.g., Tableau, Power BI)

---

*Prepared by Allan (README Lead) – October 2025*  
*Team Project – General Health Services and Disease Data in Kenya*