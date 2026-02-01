# Energy Consumption & Prosumer Landscape in Lithuania

## Overview
This project explores electricity consumption patterns in Lithuania with a focus on the **Prosumer (Generating Consumer)** segment and its interaction with meteorological factors.  
The work started as a predictive modeling task but evolved into a **Strategic Business Intelligence analysis** after identifying fundamental data-resolution limitations.

The result is a data-driven assessment of **regional energy distribution, prosumer concentration, and grid efficiency constraints**, delivered through Python analytics and an interactive Power BI dashboard.

---

## Business Context & Objectives
Lithuania’s energy system is undergoing decentralization driven by renewable adoption and prosumer growth.  
Utility providers and grid operators face three key analytical questions:

- **Predictive feasibility**  
  Can semi-annual electricity consumption be reliably forecasted using aggregated weather indicators?
- **Regional concentration**  
  Which regions host the highest prosumer density and installed generation capacity?
- **Segment contribution**  
  How do different consumer types (producing vs. non-producing) impact total grid load?

---

## Data & Architecture

### Data Sources
- **Energy data**
  - Semi-annual electricity consumption (kWh)
  - Installed generation capacity (kW)
  - Region and consumer segment
- **Weather data**
  - Daily temperature (mean/min/max)
  - Wind speed
  - Precipitation
  - Snowfall  
  Aggregated to match energy reporting periods

### Technology Stack
- **Python (Pandas, NumPy)** — data cleaning, feature engineering, aggregation
- **Scikit-learn** — Random Forest Regressor
- **SQL logic** — relational data structuring
- **Power BI (DAX)** — interactive dashboards and regional analysis

---

## Predictive Modeling: Technical Findings

A **Random Forest Regressor** was trained to predict electricity consumption using aggregated weather features.

### Model Results
- **R² score:** 0.00018  
- **MSE:** High relative to the target mean

### Technical Post-Mortem
The model failed to extract meaningful predictive signals due to **temporal smoothing**.

Weather impacts electricity demand on **hourly or daily scales** (e.g. short cold spells or heat waves).  
By aggregating both energy and weather data into **6-month periods**, peak-driven variance was averaged out, eliminating the signal required for forecasting.

**Key takeaway:**  
> Utility-grade consumption forecasting requires high-resolution data (smart meters, hourly loads). Semi-annual aggregation is suitable for strategic BI, not predictive ML.

---

## Business Intelligence Insights

After the predictive pivot, the project focused on **descriptive and strategic insights** using Power BI.

### Key Findings
- **Regional hotspots**  
  Vilnius and Kaunas regions account for the majority of prosumer activity and energy consumption.
- **Growing prosumer capacity**  
  The *Gaminantis vartotojas* segment shows a steady increase in installed generation capacity (kW), indicating accelerating renewable adoption.
- **Efficiency gap**  
  Higher generation capacity does not proportionally reduce semi-annual net consumption in some regions, suggesting:
  - limited self-consumption
  - insufficient storage adoption
  - potential grid inefficiencies

---

## Strategic Recommendations
- **Granular data collection**  
  Transition from semi-annual to hourly consumption data to enable peak-load forecasting.
- **Infrastructure prioritization**  
  Focus smart-grid and modernization investments on high-density regions (Vilnius, Kaunas).
- **Segment-specific programs**  
  Target regions with *high consumption / low generation efficiency* for energy-efficiency and storage incentive programs.

---

## How to Run the Project

### Python Analysis
Run the Jupyter notebook:
```bash
electricity_consumption_analysis.ipynb

