# Sales Dashboard - Toy Sales Analysis

## Table of Contents
1. [Project Overview](#project-overview)
2. [Dataset Information](#dataset-information)
3. [Project Objectives](#project-objectives)
4. [Key Questions Answered](#key-questions-answered)
5. [DAX Calculations](#dax-calculations)
6. [Dashboard Process](#dashboard-process)
7. [Insights and Analysis](#insights-and-analysis)
8. [Conclusions and Recommendations](#conclusions-and-recommendations)

---

## Project Overview

This dashboard provides an in-depth analysis of toy sales data from Maven Analytics, covering four locations and five toy categories. It offers insights into key performance metrics, such as sales trends, revenue contributions, and performance by location and category. 

The dashboard is built entirely in Power BI, utilizing various DAX measures and visualizations to track sales performance and uncover actionable insights.

## Dataset Information

The dataset includes:
- Sales data for toys across **4 locations** and **5 toy categories**
- Monthly sales records in CSV format for the period 2022 and 2023, loaded into Power BI for processing and visualization.

---

## Project Objectives

The main objective of this dashboard is to:
- Track sales performance across locations and categories.
- Provide actionable insights into sales trends, revenue contributions, and popular categories.
- Enable quick, visual decision-making for stakeholders.
- To identify the store that holds more stock

---

## Key Questions Answered

The dashboard answers the following questions:

1. **What is the total revenue and the quarterly trend?**
   - Breakdown of revenue across all locations with monthly performance indicators.
   
2. **Which location generates the highest revenue?**
   - Performance analysis for each location, highlighting the top performer.
   
3. **Which toy category is the most popular across all locations?**
   - Revenue and unit sales for each toy category, identifying the most popular categories.
   
4. **What is the year-over-year and month-over-month growth rate?**
   - An analysis of growth trends, showing how sales have progressed over time.
   
5. **What is the average revenue per order and the average unit price per toy category?**
   - Detailed view of average revenue per transaction and category-based pricing insights.
   
6. **How are sales distributed across different categories in each location?**
   - Visualization of category performance within each location, identifying key sales drivers.

---


## DAX Calculations

Several DAX measures were calculated to provide insights into the data. Here are a few key DAX calculations and their purposes:

1. **Total Revenue**  
   - Measure for calculating overall revenue across categories and locations.

 ```DAX
   
1.  Total Revenue = SUM('Sales'[Revenue])

2. **Quartely Revenue Trend**

    Quarterly Revenue = CALCULATE([Total Revenue], DATESMTD('Sales'[Date]))

3. **Year-over-Year Growth Rate**

    YoY Growth = ( [This Year Sales] - [Last Year Sales] ) / [Last Year Sales]

4. **Average Revenue per Order**

     Average Revenue per Order = DIVIDE([Total Revenue], [Order Count])

5. **Revenue by Category**
     Revenue by Category = CALCULATE([Total Revenue], 'Sales'[Category])

6. **Average Unit Price**
     Average Unit Price = DIVIDE([Total Revenue], [Total Units Sold])
```
## Dashboard Process

      - Data Loading and Preparation
        The data was uploaded from CSV files provided by Maven Analytics directly into Power BI.
        Data cleaning and formatting were completed within Power BI, including date formatting and location/category mapping.

      - DAX Measures Creation
        DAX formulas were created to calculate key metrics, such as total revenue, average unit price, growth rates, and more.

      - Visualization and Layout Design
        Various Power BI visuals (e.g., line charts, bar charts, slicers) were used to create an interactive, user-friendly interface.
        Filters and slicers were added to enable deeper analysis by category, location, and date.

      - Dashboard Testing and Refinement
        The dashboard was tested for accuracy and usability.
        Feedback was gathered to ensure the dashboard meets stakeholders' needs.

# Insights and Analysis

This dashboard provides comprehensive insights into the toy sales data. It reveals location-based trends, identifies the best-selling categories, and tracks sales growth. This helps stakeholders make informed decisions on inventory management, promotional strategies, and resource allocation across different locations.
Conclusions and Recommendations

# Conclusions: 
  The dashboard reveals strong performance in specific locations and highlights top-performing categories, providing a clear view of overall 
  sales health.
  
# Recommendations:
  Focus on stocking and promoting high-performing toy categories in the top locations. Consider strategies for boosting growth in 
  underperforming locations based on insights gathered from category preferences and sales trends.













   


