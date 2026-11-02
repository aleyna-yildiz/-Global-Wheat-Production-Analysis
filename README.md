
Global Wheat Production Analysis (2010–2024)

1. Project Overview

This project explores global wheat production patterns across countries from 2010 to 2024 using data from FAOSTAT, the Food and Agriculture Organization of the United Nations.

The analysis focuses on global production trends, leading wheat-producing countries, country-level comparisons, and changes in production rankings over time.

The project applies data cleaning, exploratory data analysis (EDA), SQL querying, and data visualization to identify meaningful patterns in global wheat production.

2. Research Questions

* How has global wheat production changed between 2010 and 2024?
* Which countries are the leading wheat producers?
* How concentrated is global wheat production among the leading countries?
* How have country production rankings changed over time?
* Which years recorded the highest production growth and the largest decline?

3. Dataset

Attribute	Description
Source	FAOSTAT – Crops and Livestock Products
Crop	Wheat
Period	2010–2024
Measurement Unit	Tonnes (t)
Final Analytical Records	1,858

The original dataset contains country-level wheat production records reported by FAOSTAT.

Data Preparation

The following preparation steps were performed:

* Inspected dataset structure and data types.
* Assessed missing values and data quality.
* Checked duplicate records and invalid production values.
* Standardized column names and data types.
* Excluded overlapping China reporting subregions to avoid double-counting.

The final analytical dataset contains 1,858 records.

4. Tools & Technologies

Tool	Purpose
Python	Data analysis
Pandas	Data cleaning and manipulation
NumPy	Numerical operations
Matplotlib	Data visualization
Jupyter Notebook	Analysis environment
SQL	Data querying and aggregation
Google BigQuery	SQL analysis
Tableau	Data visualization and dashboard development
Git & GitHub	Version control and project documentation

5. Analysis Workflow

1. Data collection and inspection
2. Data quality assessment
3. Data cleaning and preparation
4. Exploratory Data Analysis (EDA)
5. Global production trend analysis
6. Country-level production analysis
7. Production ranking comparison
8. Key findings and insights
9. Dashboard development

6. Key Findings & Insights

Global Production Growth

Global wheat production increased from approximately 653.7 million tonnes in 2010 to 798.5 million tonnes in 2024.

This represents an increase of approximately 22.1% over the analyzed period.

Peak Production

* Highest production year: 2022
* Production in 2022: approximately 808.0 million tonnes

Annual Production Changes

* Highest annual growth: 2013 (+8.13%)
* Largest annual decline: 2012 (-5.44%)

Production Concentration

The ten leading wheat-producing countries accounted for approximately 69.73% of cumulative reported production during the analyzed period.

The top three producers accounted for approximately 40.19%.

Changes in Country Rankings

Comparing country rankings in 2010 and 2024:

* Canada improved from 9th to 5th place.
* Russian Federation improved from 4th to 3rd place.
* France declined from 5th to 8th place.
* Germany moved from 7th to 10th place.
* Ukraine entered the top ten, reaching 9th place in 2024.

7. Dashboard

The project includes visual analyses covering:

* Global Wheat Production Trend
* Global Production Map
* Top 10 Wheat-Producing Countries
* Annual Wheat Production Trends – Top 5 Producers
* Wheat Production Ranking: 2010 vs 2024
* Key Ranking Changes

8. Project Structure

Global-Wheat-Production-Analysis/
│
├── data/
│   ├── raw/
│   │   └── FAOSTAT_data_en_8-24-2026-2.csv
│   │
│   └── processed/
│       └── global_wheat_production_clean.csv
│
├── notebooks/
│   └── Global_Wheat_Production_Analysis.ipynb
│
├── README.md
└── .gitignore

9. How to Explore the Project

The main analysis is available in the Jupyter Notebook:

notebooks/Global_Wheat_Production_Analysis.ipynb

The processed dataset is available in:

data/processed/global_wheat_production_clean.csv

The original FAOSTAT dataset is stored in:

data/raw/

10. Data Source

Food and Agriculture Organization of the United Nations (FAO)

Dataset: FAOSTAT – Crops and Livestock Products

⁠FAOSTAT Official Website

⸻

Project: Global Wheat Production Analysis
Analysis Period: 2010–2024
Author: Aleyna Yildiz