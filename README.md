# Data Analytics Assignment

This project is a **Data Analytics and Exploratory Data Analysis (EDA)** assignment developed using **Python, Pandas, NumPy, Matplotlib, and Seaborn**. The project analyzes multiple real-world datasets related to **Air Quality, Energy Consumption, Traffic Volume, and Citizen Complaints**.

The main objective of this assignment is to demonstrate the complete data analytics workflow, including **data loading, cleaning, preprocessing, feature extraction, outlier handling, exploratory data analysis, visualization, correlation analysis, and pattern identification**.

---

## Project Overview

The project analyzes four different datasets:

1. 🌫️ **Air Quality Data**
2. ⚡ **Energy Consumption Data**
3. 🚗 **Traffic Volume Data**
4. 🏙️ **City Complaints Data**

For each dataset, appropriate preprocessing and exploratory analysis techniques are applied to discover useful patterns and relationships.

---

## Technologies & Libraries

The project is implemented in **Python** using the following libraries:

* **Python**
* **NumPy** – Numerical computations
* **Pandas** – Data manipulation and analysis
* **Matplotlib** – Data visualization
* **Seaborn** – Statistical visualization
* **Google Colab** – Development and execution environment

---

# Datasets

## 1. 🌫️ Air Quality Dataset

**Dataset:** `Air_Quality_Data.csv`

The Air Quality dataset is analyzed to understand changes and patterns in **PM2.5 AQI values over time**.

### Data Processing

The following preprocessing steps are performed:

* Convert the `date` column into datetime format.
* Remove duplicate records.
* Handle missing `aqi_pm2.5` values using the median.
* Extract:

  * Year
  * Month
  * Day
* Create pollution categories based on AQI values.
* Detect and handle outliers using the **IQR (Interquartile Range)** method.

### Pollution Categories

| AQI Range | Category                |
| --------- | ----------------------- |
| 0–50      | Good                    |
| 51–100    | Moderate                |
| 101–150   | Unhealthy for Sensitive |
| 151–200   | Unhealthy               |
| 201–300   | Very Unhealthy          |
| 301+      | Hazardous               |

### Visualizations

The following visualizations are created:

* AQI Trend Over Time
* AQI Distribution
* Seasonal AQI Pattern

---

# 2. Energy Consumption Dataset

**Dataset:** `Energy_Consumption_Data.csv`

This dataset is used to analyze electricity consumption patterns and identify periods of higher energy usage.

### Data Processing

The following operations are performed:

* Convert `Date_Time` into datetime format.
* Sort records chronologically.
* Handle missing values using forward filling.
* Remove duplicate records.
* Extract:

  * Year
  * Month
  * Day
  * Hour

### Analysis

The project analyzes:

* Energy consumption over time.
* Average energy consumption by hour.
* Average energy usage across different areas.

### Areas Analyzed

* AC_DR
* UPS
* LR
* Kitchen
* AC_BR

### Visualizations

* Energy Consumption Over Time
* Average Hourly Energy Consumption
* Average Energy Usage by Area

---

# 3. Traffic Volume Dataset

**Dataset:** `Traffic_Volume_Data.csv`

The Traffic dataset is used to investigate traffic volume, speed, congestion, and peak-hour patterns.

### Data Processing

The following steps are performed:

* Convert `timestamp` into datetime format.
* Extract:

  * Year
  * Month
  * Day
  * Hour
* Handle missing values using forward filling.

### Peak & Off-Peak Analysis

Traffic records are categorized into:

* **Peak Hours**
* **Off-Peak Hours**

This allows traffic patterns to be compared throughout the day.

### Visualizations

* Traffic Volume Trends Over Time
* Peak vs Off-Peak Hours
* Traffic Correlation Heatmap

### Correlation Analysis

The following variables are analyzed:

* `vehicle_count_main`
* `avg_speed_gps`
* `congestion_value`

A correlation matrix and heatmap are used to understand relationships between traffic volume, speed, and congestion.

---

# 4. 🏙️ City Complaints Dataset

**Dataset:** `City_Compaints_Data.csv`

This dataset is used to analyze citizen complaints and identify common complaint types and complaint patterns throughout the day.

### Data Processing

The following preprocessing steps are performed:

* Convert `Created Date` to datetime.
* Convert `Closed Date` to datetime.
* Handle missing values using forward filling.
* Remove duplicate records.
* Remove records with missing:

  * Complaint Type
  * Location
* Extract:

  * Year
  * Month
  * Day
  * Hour

### Complaint Duration

The project calculates the number of days required to close each complaint using:

`Closed Date - Created Date`

This produces a new feature:

`Complaint_Duration`

### Visualizations

* Top 10 Citizen Complaints
* Complaints by Hour of the Day

---

# Exploratory Data Analysis

The project performs several EDA techniques to understand the datasets.

### Air Quality

* AQI trends over time
* AQI distribution
* Seasonal pollution patterns

### Energy

* Energy consumption trends
* Hourly consumption patterns
* Consumption by different areas

### Traffic

* Traffic volume trends
* Peak vs off-peak traffic
* Correlation between traffic variables

### Citizen Complaints

* Most common complaint types
* Complaint frequency by hour
* Complaint duration

---

# Relationship & Correlation Analysis

The project also investigates relationships between different datasets and variables.

### Traffic and Air Quality

Traffic volume can be compared with air-quality trends to investigate whether periods of higher traffic correspond with increased AQI levels.

> Higher traffic volumes may coincide with increased AQI levels, potentially indicating the contribution of vehicle emissions to air pollution.

### Energy Consumption

Average consumption is calculated for different areas to identify which areas contribute more significantly to overall energy usage.

### Citizen Complaints

Complaint frequency is analyzed by hour to identify times of day when citizens submit more complaints.

### Seasonal Patterns

AQI values are grouped by month to identify potential seasonal changes in air quality.

---

# Key Visualizations

The assignment generates several charts, including:

* 📈 AQI Trend Over Time
* 📊 AQI Distribution
* ⚡ Energy Consumption Over Time
* 🕐 Average Hourly Energy Consumption
* 🚗 Traffic Volume Trends
* 🚦 Peak vs Off-Peak Traffic
* 🔥 Traffic Correlation Heatmap
* 🏙️ Top 10 Citizen Complaints
* 🕐 Complaints by Hour
* 🌦️ Seasonal AQI Pattern
* ⚡ Average Energy Usage by Area

---

# Data Analytics Workflow

The overall workflow followed in this project is:

```text
Dataset
   ↓
Data Loading
   ↓
Data Understanding
   ↓
Data Cleaning
   ↓
Missing Value Handling
   ↓
Duplicate Removal
   ↓
Feature Extraction
   ↓
Outlier Handling
   ↓
Exploratory Data Analysis
   ↓
Visualization
   ↓
Correlation Analysis
   ↓
Insights & Interpretation
```

---

# Project Structure

```text
Data-Analytics-Assignment/
│
├── Assignment_DataAnalytics.ipynb
│
├── Air_Quality_Data.csv
├── Energy_Consumption_Data.csv
├── Traffic_Volume_Data.csv
├── City_Compaints_Data.csv
│
└── README.md
```

---

# How to Run the Project

## Option 1 — Google Colab

1. Open the notebook in Google Colab.
2. Run the notebook cells sequentially.
3. Upload the required CSV datasets when prompted.
4. Execute the analysis and visualization cells.

The notebook uses:

```python
from google.colab import files
uploaded = files.upload()
```

to upload the datasets.

---

## Option 2 — Local Jupyter Notebook

Install the required dependencies:

```bash
pip install numpy pandas matplotlib seaborn
```

Then open:

```text
Assignment_DataAnalytics.ipynb
```

Make sure all four CSV files are located in the same directory as the notebook.

---

# Objectives

The main objectives of this assignment are to:

* Understand real-world datasets.
* Perform data cleaning and preprocessing.
* Handle missing values.
* Remove duplicate records.
* Detect and handle outliers.
* Extract useful date/time features.
* Perform exploratory data analysis.
* Create meaningful visualizations.
* Analyze correlations between variables.
* Identify trends and patterns.
* Generate data-driven observations.

---

# Conclusion

This assignment demonstrates a complete **data analytics workflow using Python**. Four different datasets were cleaned, transformed, analyzed, and visualized to identify meaningful patterns.

The analysis covers environmental conditions, energy consumption, traffic behavior, and citizen complaints. The resulting visualizations and statistical analysis provide a foundation for understanding trends and identifying areas that may require further investigation or attention.

---

## Author

**Muhammad Moeed Rana**

**BS Software Engineering**

This project was developed as part of a **Data Analytics Assignment** using Python and Google Colab.

---

## Skills Demonstrated

* Python
* NumPy
* Pandas
* Data Cleaning
* Data Preprocessing
* Exploratory Data Analysis (EDA)
* Statistical Analysis
* Outlier Detection
* Feature Engineering
* Data Visualization
* Correlation Analysis
* Matplotlib
* Seaborn
* Google Colab
