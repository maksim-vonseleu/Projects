# 🇫🇷 AirBnB Listing Analysis: Paris

## Project Overview
This repository contains an Exploratory Data Analysis (EDA) of AirBnB listings in **Paris, France**. The primary goal is to uncover key factors influencing pricing, assess the quality of the listings data, and analyze the market dynamics of short-term rentals in the capital city.

---

## 🖼️ Visualizations

The project includes several data visualizations, generated using Matplotlib and Seaborn, to illustrate key findings, such as:
* Price distribution across different neighborhoods.
* The relationship between listing capacity and price.
* Temporal trends of new host entries and average price movements.

A sample visualization is included in the project files (e.g., `image_a03643.png`).

---

## 🎯 Goals

1.  To conduct a comprehensive **investigation of the AirBnB market structure** in Paris.
2.  To **identify the main price predictors** for listings (e.g., neighborhood, accommodation capacity).
3.  To analyze the **temporal dynamics** of the market, including the influx of new hosts and changes in average price over time since 2008.

---

## 📋 Analysis Objectives

The analysis was structured into the following key tasks, detailed step-by-step within the Jupyter Notebook:

1.  **Data Loading and Cleaning:** Import the main `Listings.csv` dataset, handle data types, and initial inspection.
2.  **Data Filtering:** Filter the dataset to include only listings confirmed to be located in **Paris**.
3.  **Quality Assurance (QA):** Check for missing values, calculate descriptive statistics, and handle outliers.
4.  **Neighborhood Analysis:** Group listings by `neighbourhood` to determine the most and least expensive areas based on the average price.
5.  **Accommodation Capacity Analysis:** Investigate the relationship between the average price and the number of guests an apartment can accommodate (`accommodates`).
6.  **Temporal Analysis:** Create a time-series plot to visualize trends in the number of new hosts and the corresponding movement in the average listing price annually.

---

## 💡 Key Insights

The analysis yielded the following significant conclusions about the Parisian AirBnB market:

* **Average Price:** The overall average price per night for a listing in Paris is approximately **€113**.
* **Price Volatility:** The maximum observed price reached **€12,000**, highlighting the presence of ultra-luxury listings.
* **Most Affordable Areas:** The most budget-friendly neighborhoods are **Menilmontant** (with an average price around €75) and **Buttes-Chaumont** (average price around €83).
* **Capacity as a Predictor:** There is a **strong positive correlation** between the apartment's capacity (`accommodates`) and its average price.
* **Market Growth Trend:** The temporal analysis shows the historical growth of the platform and price fluctuations since 2008.

---

## 🛠️ Tech Stack

The analysis was performed using the Python programming language within a Jupyter Notebook environment.

* **Language:** Python
* **Environment:** Jupyter Notebook
* **Libraries:**
    * **Pandas:** For data manipulation and cleaning.
    * **Matplotlib:** For data visualization.
    * **Seaborn:** Used for creating informative and attractive statistical graphics.
    * **NumPy:** For numerical operations.

---

## 🚀 How to View the Analysis

The core of this project is the **`AirBnB Listing Analysis.ipynb`** file.

### Option 1: View Online (Recommended)
You can view the full notebook, including all code, output, and visualizations, directly on GitHub.

### Option 2: Run Locally

1.  **Clone the Repository:**
    ```bash
    git clone [Your Repository URL]
    cd [Your Repository Name]
    ```
2.  **Install Dependencies:**
    ```bash
    pip install pandas matplotlib seaborn jupyter
    ```
3.  **Launch Jupyter:**
    ```bash
    jupyter notebook
    ```
4.  **Open the File:** Navigate to and click on the **`AirBnB Listing Analysis.ipynb`** file to open and execute the code cells.
