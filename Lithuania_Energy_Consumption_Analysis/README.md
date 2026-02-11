# Lithuania Energy Consumption & Prosumer Analysis

## 1. Executive Summary
This project analyzes the relationship between electricity consumption and meteorological factors in Lithuania, with a specific focus on the growing **"Prosumer"** (Generating Consumer) segment. While the initial goal was to build a predictive forecasting model, the technical analysis revealed that semi-annual data aggregation masks critical weather-driven consumption signals. Consequently, the project was pivoted to a **Strategic Business Intelligence** framework to provide actionable insights into regional energy distribution and capacity planning.

---

## 2. Business Problem & Objectives
The Lithuanian energy sector is decentralizing. Utility providers and grid operators need to understand:
* **Predictive Feasibility:** Can semi-annual consumption be forecasted using macro-weather patterns?
* **Regional Density:** Where is the highest concentration of generation capacity?
* **Segment Insights:** How do different prosumer types (Residential vs. Business) contribute to the grid load?

---

## 3. Data Architecture & Methodology

### Data Sources
* **Energy Data:** Semi-annual electricity consumption and generation capacity per region/segment.
* **Weather Data:** Daily metrics (Mean/Min/Max Temperature, Wind Speed, Precipitation, Snowfall) aggregated to match energy periods.

### Tech Stack
* **Python (Pandas/NumPy):** Data cleaning, feature engineering, and period-based aggregation.
* **Scikit-Learn:** Random Forest Regressor implementation.
* **Power BI (DAX):** Interactive reporting and regional trend analysis.

---

## 4. Technical Deep-Dive: The Predictive Challenge
A **Random Forest Regressor** was trained to predict consumption (`value`) based on weather features.

### Results:
* **R² Score:** $0.00018$
* **Mean Squared Error (MSE):** Significantly high relative to the target mean.

### Technical Post-Mortem (Lessons Learned):
The model failed to produce meaningful predictions due to **Temporal Smoothing**. 

Weather influences energy consumption on an hourly/daily basis (e.g., a 3-day cold snap). By aggregating this data into 6-month averages, the "peak signals" were lost in the mean. This proves that for utility-grade forecasting, **high-resolution (Smart Meter) data** is a prerequisite.

---

## 5. Business Intelligence & Regional Insights
Following the predictive pivot, the analysis focused on descriptive business value through Power BI.

### Key Business Findings:
* **Regional Hotspots:** **Vilnius** and **Kaunas** regions account for the vast majority of prosumer activity. Grid modernization efforts should be geographically targeted here.
* **Prosumer Capacity:** The *"Gaminantis vartotojas"* segment shows a steady increase in installed capacity ($kW$), suggesting a growing reliance on solar/wind feed-ins.
* **Efficiency Gap:** Analysis shows that high generation capacity in certain regions does not proportionally lower semi-annual net consumption, indicating potential inefficiencies in self-consumption habits or storage (battery) adoption.

---

## 6. Strategic Recommendations
1.  **Granular Data Collection:** Transition from semi-annual to hourly data collection to enable accurate peak-load forecasting.
2.  **Infrastructure Prioritization:** Use the Regional Capacity Share metrics to guide the rollout of smart-grid technologies in high-density areas (Vilnius/Kaunas).
3.  **Segment-Specific Programs:** Develop targeted energy-efficiency programs for "High Consumption/Low Generation" clusters identified in the regional analysis.

---

## 7. How to Run the Analysis
* **Python:** Run `electricity_consumption_analysis.ipynb` to see the data processing pipeline and ML evaluation.
* **Data:** Ensure `final_energy_weather_data.csv` is in the root directory.
* **Power BI:** Open the provided `.pbix` file to interact with the regional dashboard.

---
**Analyst:** Maksim Vonseleu  
**Stack:** Python | Power BI | SQL | Business Intelligence

