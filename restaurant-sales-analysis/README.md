# Restaurant Sales Data Analysis

## Overview
This project involves an in-depth analysis of restaurant sales data to understand customer behavior, identify popular products, and pinpoint peak revenue periods. The insights derived are used to provide actionable recommendations for optimizing operations and sales strategies.

## Data Source
The data was extracted from a SQLite database (`db.sqlite3`) containing information on restaurant orders, order items, and products. The extracted data was then saved as a CSV file (`combined_restaurant_data.csv`) for further analysis.

## Analysis Performed
1.  **Data Loading and Inspection**: Initial loading of data into a Pandas DataFrame and inspecting its structure and types.
2.  **Top Products by Quantity**: Identification of the top 10 products sold based on the total quantity.
3.  **Top Products by Revenue**: Calculation of revenue per item and identification of the top 10 products contributing the most to total revenue.
4.  **Hourly Revenue Analysis**: Analysis of total revenue generated across different hours of the day to determine peak operating times.
5.  **Daily Revenue Analysis**: Examination of total revenue generated on different days of the week to identify trends and peak days.

## Key Findings
*  **Peak Days**: Friday and Saturday show significantly higher revenue compared to other weekdays.
*  **Peak Hours**: The period between 17:00 (5 PM) and 20:00 (8 PM) is the most profitable time slot, with 18:00 being the peak hour.
*  **Top Selling Products (by Quantity)**: 'Plain Papadum', 'Pilau Rice', and 'Plain Naan' are the most frequently purchased items.
*  **Top Revenue Generating Products**: 'Chicken Tikka Masala' is the highest revenue generator, followed by 'Pilau Rice' and 'Plain Naan'. Despite lower quantity sales, 'Chicken Tikka Masala' drives significant profit due to its higher price.

## Recommendations
*   **Staff Optimization**: Increase staff presence (kitchen and front-of-house) during peak hours (17:00-21:00) on Friday and Saturday to maintain service quality.
*   **Off-Peak Promotions**: Introduce special offers like business lunches or combo meals during weekdays and before 17:00 to boost sales during quieter periods.
*   **Strategic Bundling**: Leverage popular items like 'Plain Papadum' as a 'magnet' by offering them for free with high-revenue dishes like 'Chicken Tikka Masala', or create bundled sets (e.g., Masala + Pilau Rice + Plain Naan) to encourage higher spending per visit.

## Technologies Used
*     Python
* `pandas` for data manipulation and analysis
* `Matplotlib` for data visualization
*  `sqlite3` for database interaction
*  `Google Colab` for the development environment
