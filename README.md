# Analysing-pharmaceutical-sales-data

This project is designed to conduct an in-depth analysis of daily pharmaceutical sales data. Using the Python programming language and various data science libraries, the script processes transaction data to identify top-selling drug categories and map seasonal trends, with a specific focus on respiratory product lines. The project itself is based on a guide from the roadmap.sh platform. This project is from [roadmap.sh] (https://roadmap.sh/projects/pharmaceutical-sales-data).

## Project Overview
The main goal of this analysis is to transform complex raw data sets into insights that are informative and ready to use. This program relies on ATC (Anatomical Therapeutic Chemical) code classification to group various types of drugs.

### Key Features
* **Total Sales Calculation:** Computing the cumulative sales across all major drug categories.
* **Trend Tracking:** Visualizing monthly sales dynamics, specifically for respiratory medications (category R03).
* **Performance Ranking:** Identifying the top-selling pharmaceutical products, both overall and for specific months.
* **Data Visualization:** Generating clean, professional bar charts and line graphs for reporting purposes.

## Technical Stack
* **Programming Language:** Python
* **Libraries:**
  * **Pandas:** Used for data manipulation and processing of CSV-formatted files.
  * **Matplotlib:** Used for designing and producing high-quality graphical visualizations.
  * **OS:** Used for managing directories and system files.

## Code Explanation
The script in the `analisis_obat.py` file is structured according to a systematic data science workflow:
### 1. Data Loading & Cleaning:
The program begins by validating the existence of the `salesdaily.csv` file. Once validated, the data is loaded, and the date column (`datum`) is converted into a datetime format, enabling accurate time-series analysis based on months or years.
### 2. Aggregation Logic:
The script sums the columns representing ATC codes (such as M01AB or N02BE) and sorts them to identify the "best-selling" products. Additionally, a dedicated function called `get_top_3_monthly` filters the data by a specific year and month to display the three most popular medications for that period.
### 3. Visualization Engine:
The program generates two primary types of plots: a bar chart to compare sales volumes across different medication categories, and a line graph that tracks the sales trends of the 'R03' category over time, revealing potential seasonal patterns.

## Visualization and Data Insights
Based on the resulting diagram, the following are the important analysis points found:
### 1.Total Sales Analysis (Bar Chart):
This graph presents the total quantity of products sold in each ATC category.
* Dominant Category: N02BE (generally includes Analgesic/Paracetamol products) recorded the highest sales volume by quite a large margin.
* Insight: The high sales figures for N02BE indicate the high frequency of people's need for over-the-counter pain relievers, when compared with specific drugs such as N05C (Hypnotics/Sedatives).
### 2. Monthly Sales Trends for R03 Category (Line Chart):
This graph monitors the dynamics of sales of respiratory medicines (R03) throughout the month.
* Trend Analysis: There are quite obvious fluctuations in sales. In general, R03 drugs (which are often used to treat asthma or coughs) show a spike in demand in certain seasons (such as winter or allergy season).
* Insight: The rise and fall of this graph suggests that management of respiratory medicine stocks should be adjusted to seasonal patterns, rather than maintaining static supply levels throughout the year.

## Data Dictionary (ATC Codes)
| Code | Category |
| :--- | :---|
| **M01AB/AE** | Anti-inflammatory and antirheumatic products|
| **N02BA/BE** | Analgesics (Pain relievers/painkillers)|
| **N05B/C** | Psycholeptics (Anxiolytics/hypnotics)|
| **R03** | Drugs for obstructive airway diseases (Respiratory)|
| **R06** | Antihistamines for systemic use|
