# SuperStore Sales Analysis & Forecasting Dashboard | Power BI
An interactive **Power BI Sales Dashboard** built using SuperStore sales data to analyze sales performance, profitability, customer segments, regional performance, product categories, and sales trends.
The project uses **Power Query for data preparation, DAX for calculations, and Power BI visualizations** to transform raw transaction data into an interactive business intelligence dashboard.


## Project Overview
The objective of this project is to analyze SuperStore sales data and create an interactive dashboard that provides a clear view of business performance.

The dashboard helps answer important business questions related to:
* Sales performance
* Profitability
* Quantity sold
* Customer segments
* Regional performance
* Category and sub-category performance
* Monthly sales trends
* Product performance
* Payment methods
* Order and shipping information
* Sales forecasting
The dashboard also includes a **Sales Forecast** view to analyze future sales trends based on historical performance.


## Business Objective
The main goal of this project is to convert raw sales transaction data into meaningful business insights that can support data-driven decision-making.

### Key Business Questions
1. What is the overall sales performance?
2. What is the total profit generated?
3. How many products/units were sold?
4. Which regions generate the highest sales?
5. Which product categories perform the best?
6. Which sub-categories contribute most to sales and profit?
7. How does sales performance change over time?
8. Which customer segments contribute most to revenue?
9. Which products generate higher profit?
10. Which products or categories have lower profitability?
11. What payment methods are commonly used?
12. What are the historical sales trends?
13. What does the sales forecast indicate for upcoming periods?


# Dataset
The project uses a **SuperStore Sales Dataset** containing transaction-level retail sales information.
The repository contains **5,901 transaction records** plus the header row.

### Dataset Columns
| Column        | Description                     |
| ------------- | ------------------------------- |
| Row ID        | Unique row identifier           |
| Order ID      | Unique order identifier         |
| Order Date    | Date when the order was placed  |
| Ship Date     | Date when the order was shipped |
| Ship Mode     | Shipping method used            |
| Customer ID   | Unique customer identifier      |
| Customer Name | Customer name                   |
| Segment       | Customer segment                |
| Country       | Country                         |
| City          | Customer city                   |
| State         | Customer state                  |
| Region        | Sales region                    |
| Product ID    | Product identifier              |
| Category      | Product category                |
| Sub-Category  | Product sub-category            |
| Product Name  | Name of the product             |
| Sales         | Sales/revenue generated         |
| Quantity      | Quantity sold                   |
| Profit        | Profit generated                |
| Returns       | Return indicator                |
| Payment Mode  | Payment method                  |
The dataset also contains additional fields (`ind1`, `ind2`) that are present in the source CSV.


# Tools & Technologies

### Power BI
Used for:
* Interactive dashboard creation
* Data visualization
* KPI reporting
* Filtering
* Trend analysis
* Forecasting

### Power Query
Used for:
* Data import
* Data cleaning
* Data transformation
* Data type management
* Preparing the dataset for analysis

### DAX
Used for:
* Creating calculated measures
* KPI calculations
* Aggregations
* Business metrics
* Analytical calculations

### Data Visualization
Used to communicate:
* Sales trends
* Profitability
* Regional performance
* Category performance
* Customer contribution
* Forecasting results
The repository identifies Power BI, Power Query, DAX, data cleaning, and data visualization as the primary tools used in the project.


# Project Workflow
```text
Raw SuperStore Dataset
        ↓
Data Import
        ↓
Data Cleaning & Transformation
        ↓
Data Modeling
        ↓
DAX Measures
        ↓
KPI Creation
        ↓
Data Visualization
        ↓
Interactive Dashboard
        ↓
Sales Trend Analysis
        ↓
Sales Forecasting
        ↓
Business Insights
```


# Data Preparation & Transformation
The raw SuperStore dataset was prepared in Power BI before building the dashboard.

### Data Preparation Steps
* Imported the SuperStore CSV dataset into Power BI
* Reviewed the available columns
* Checked data types
* Prepared date fields for time-based analysis
* Organized categorical fields
* Prepared numerical fields for aggregation
* Handled data fields required for dashboard analysis
* Prepared the dataset for visualization and DAX calculations
The source data contains transaction-level fields covering orders, customers, geography, products, sales, quantity, profit, returns, and payment mode.


# DAX & Measures
DAX was used to create analytical measures for the dashboard.
Typical measures used in this type of analysis include:

### Total Sales
```DAX
Total Sales = SUM(Sales[Sales])
```

### Total Profit
```DAX
Total Profit = SUM(Sales[Profit])
```

### Total Quantity
```DAX
Total Quantity = SUM(Sales[Quantity])
```

### Total Orders
```DAX
Total Orders = DISTINCTCOUNT(Sales[Order ID])
```

### Profit Margin
```DAX
Profit Margin =
DIVIDE(
    [Total Profit],
    [Total Sales],
    0
)
```


# Dashboard Features
The repository's main dashboard covers **Sales KPI, Profit KPI, Quantity Sold, Regional Analysis, Category Analysis, Monthly Sales Trends, and Interactive Filters**.

## 1. Sales KPI
The dashboard provides a high-level view of overall sales performance.
This allows users to quickly understand the revenue generated by the business.


## 2. Profit KPI
Profit is tracked separately from sales to understand the financial performance of the business.
This is important because high sales do not necessarily mean high profitability.


## 3. Quantity Sold
The dashboard tracks total quantity sold to understand product demand and sales volume.


## 4. Regional Analysis
Sales performance can be analyzed across different regions.
This helps identify:
* High-performing regions
* Lower-performing regions
* Regional sales distribution
* Geographic performance patterns


## 5. Category Analysis
Product categories are analyzed to understand their contribution to overall sales and profit.
The major categories in the dataset include:
* Furniture
* Office Supplies
* Technology
The dataset also provides detailed sub-category information such as Phones, Chairs, Bookcases, Binders, Accessories, etc.


## 6. Monthly Sales Trend
The dashboard analyzes sales over time.
This helps identify:
* Sales growth patterns
* Seasonal changes
* High-sales periods
* Low-sales periods
* Monthly fluctuations


## 7. Customer Segment Analysis
The dataset contains customer segment information, allowing performance to be analyzed across different customer groups.
This helps understand:
* Which customer segments generate more sales
* Segment-wise purchasing behavior
* Segment contribution to overall revenue


## 8. Payment Mode Analysis
The dataset includes a `Payment Mode` field.
This allows payment behavior to be analyzed across methods such as:
* Online
* Cards
* COD
The transaction data contains these payment-mode values.


## 9. Shipping Analysis
The dataset contains shipping information including:
* Ship Date
* Ship Mode
This allows the business to analyze shipping patterns and order fulfillment information.


# Sales Forecasting
One of the important features of the project is the **Sales Forecast Dashboard**.
The repository contains a separate `Sales-Forecast-Dashboard.png` visualization in addition to the main dashboard screenshot.

Forecasting can help analyze:

* Historical sales patterns
* Future sales direction
* Expected sales trends
* Business planning opportunities

### Forecasting Workflow
```text
Historical Sales Data
        ↓
Time-Based Sales Trend
        ↓
Forecast Configuration
        ↓
Future Sales Projection
        ↓
Forecast Visualization
```
The forecast should be interpreted as an analytical projection rather than a guaranteed future result.


# Interactive Dashboard
The dashboard includes interactive filters that allow users to dynamically explore the data.
Users can filter the dashboard and analyze different combinations of:
* Region
* Category
* Sub-category
* Customer segment
* Time period
* Product
* Other available dimensions
This allows the dashboard to function as an exploratory analytics tool rather than a static report.


# Key Business Insights
The dashboard can be used to identify insights such as:
### Sales Performance
Understand the overall revenue trend and identify periods of stronger or weaker sales.
### Profitability
Compare revenue with profit to identify areas where high sales may not necessarily translate into high profitability.
### Regional Performance
Identify regions contributing more or less to overall business performance.
### Product Performance
Compare product categories and sub-categories to understand demand and profitability patterns.
### Customer Segments
Analyze which customer segments contribute significantly to overall sales.
### Seasonal Trends
Identify changes in sales over time and recurring sales patterns.
### Forecasting
Use historical trends to support future sales planning.


# Repository Structure
```text
SuperStore-Sales-Dashboard/
│
├── Dashboard1-Screenshot.png
│
├── Sales-Forecast-Dashboard.png
│
├── SuperStore Sales Dataset.pbix
│
├── SuperStore_Sales_Dataset (1).csv
│
└── README.md
```
The current repository contains these five project files on the `main` branch.


# Skills Demonstrated
This project demonstrates practical skills in:
* Microsoft Power BI
* Power Query
* DAX
* Data Cleaning
* Data Transformation
* Data Modeling
* KPI Development
* Data Visualization
* Sales Analysis
* Profit Analysis
* Customer Analysis
* Regional Analysis
* Product Analysis
* Time-Series Analysis
* Forecasting
* Business Intelligence
* Interactive Dashboard Development
* Business Data Storytelling


# Project Outcome
This project demonstrates an end-to-end **Data Analytics and Business Intelligence workflow** using Power BI.

The project converts raw transactional sales data into an interactive dashboard that can be used to:
* Monitor sales performance
* Track profit
* Analyze product performance
* Compare regions
* Understand customer segments
* Analyze sales trends
* Explore payment and shipping information
* Investigate business performance
* Analyze future sales trends through forecasting


# Conclusion
The SuperStore Sales Analysis & Forecasting Dashboard successfully transforms raw sales data into meaningful business insights using Power BI, Power Query, and DAX. The dashboard provides an interactive view of sales, profit, quantity, customer segments, regional performance, product categories, and monthly trends. The forecasting component further helps analyze future sales patterns based on historical data. Overall, this project demonstrates an end-to-end Data Analytics and Business Intelligence workflow, from data preparation and analysis to visualization and business reporting.
