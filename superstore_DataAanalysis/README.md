# Superstore End-to-End Data Analytics Project

## Project Overview

This project demonstrates a complete end-to-end data analytics workflow using the Superstore dataset. The goal was to simulate a real-world analytics pipeline by integrating SQL, Python, and Power BI to transform raw transactional data into meaningful business insights and an interactive dashboard.

The project covers the full lifecycle of data analytics including data ingestion, cleaning, exploratory analysis, KPI creation, and visualization.

---

## Objectives

The key objectives of this project were:

* Build a practical analytics workflow integrating SQL, Python, and Power BI
* Perform data cleaning and transformation using SQL and pandas
* Conduct exploratory data analysis to uncover business insights
* Design meaningful KPIs for business performance tracking
* Create an interactive Power BI dashboard for decision-making

---

## Dataset

The project uses the Superstore dataset containing transactional sales data with fields such as:

* Order details
* Customer information
* Product categories
* Sales, profit, quantity, and discount
* Geographic information

The raw dataset was provided in CSV format and imported into a MySQL database for further processing.

---

## Tools and Technologies Used

| Purpose                 | Tool                       |
| ----------------------- | -------------------------- |
| Database Management     | MySQL                      |
| Data Processing         | Python (pandas)            |
| Querying                | SQL                        |
| Visualization           | Power BI                   |
| Development Environment | VS Code / Jupyter Notebook |

---

## Project Workflow

### 1. Data Ingestion

* Imported the CSV dataset into Python
* Loaded data into a MySQL database
* Created an initial raw table in MySQL

### 2. Data Cleaning

* Renamed columns to SQL-friendly format
* Removed duplicate records
* Verified data types
* Checked for missing values
* Stored the cleaned data as a new table named `superstore_clean`

### 3. Exploratory Data Analysis

Using Python and SQL, several analyses were performed:

* Understanding data structure and distributions
* Correlation analysis between discount and profit
* Identifying impact of discount on profitability
* Aggregations by category, region, and time

Key insight discovered:

* Average profit turns negative when discount exceeds 20 percent

### 4. KPI Creation

Core business KPIs were designed and implemented:

* Total Sales
* Total Profit
* Profit Margin
* Total Orders
* Average Order Value
* Repeat Customers
* New Customers per Year

Some KPIs were calculated dynamically in Power BI using DAX, while others were precomputed in SQL and imported as summary tables.

### 5. Power BI Dashboard

A fully interactive Power BI dashboard was built featuring:

* KPI cards
* Sales and profit trends over time
* Orders by region
* Category and sub-category analysis
* Impact of discount on profitability
* Geographic visualization using maps
* Dynamic year and category slicers

The dashboard connects directly to the MySQL database to simulate a real analytics reporting environment.

---

## Key Business Insights

* Higher discounts generally reduce profitability
* Profit becomes negative beyond approximately 20 percent discount
* Significant variation in performance across product categories
* Regional differences in sales and customer behavior
* Clear trends in new customer acquisition over years

---

## Database Structure

Main tables used in the project:

* `superstore` – raw imported data
* `superstore_clean` – cleaned and analysis-ready data
* `category_summary` – aggregated category metrics
* `kpi_new_customers` – yearly new customer KPI

---

## How to Reproduce the Project

1. Load the Superstore CSV dataset
2. Import it into MySQL
3. Run Python scripts for cleaning and EDA
4. Create required SQL summary tables
5. Connect Power BI to MySQL
6. Build visuals using provided logic



## Author

Data Analytics Project by Srujith
