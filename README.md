# End-to-End Movie Ratings Analytics Project

<img width="516" height="296" alt="Movies Dashboard " src="https://github.com/user-attachments/assets/031612b8-ed1b-4842-ab5a-9caf52d2dac2" />


## Overview
This project is an end-to-end data pipeline that extracts raw movie rating data, transforms it using Python, loads it into a Snowflake cloud data warehouse, and visualizes it using an interactive Power BI dashboard.

---

## Tech Stack
- **Data Transformation (ETL):** Python (Pandas)
- **Data Warehouse:** Snowflake
- **Data Visualization:** Power BI
- **Data Modeling:** Star Schema

---

## Project Architecture
The project follows a standard data engineering workflow:
1.  **Data Extraction:** Raw data is sourced from the MovieLens dataset.
2.  **Transformation:** A Python script cleans the data, creates surrogate keys, and structures it into a star schema (1 fact table, 3 dimension tables).
3.  **Loading:** The transformed data is loaded into tables within a Snowflake data warehouse.
4.  **Visualization:** Power BI connects directly to Snowflake to provide an interactive analytics dashboard.
<img width="721" height="501" alt="Movies Schema drawio" src="https://github.com/user-attachments/assets/629b08eb-9127-4161-83ae-abc0325cafb4" />

---

## How to Replicate
1.  Download the [MovieLens 'small' dataset](https://files.grouplens.org/datasets/movielens/ml-latest-small.zip).
2.  Run the Python script `scripts/transform.py` to generate the clean CSV files.
3.  Execute the SQL script `sql/setup.sql` in Snowflake to create the necessary tables and stage.
4.  Load the data into Snowflake and connect your Power BI Desktop to the warehouse.
