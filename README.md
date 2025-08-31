# capstone-portfolio-project

# Everyday Grocery Sales Data Analysis - Capstone Project

## Overview

The objective of this project was to analyze grocery sales data to understand patterns related to product attributes and outlet characteristics that influence total sales. Focus was placed on fat content preferences, product category performance, outlet location and size impact, and sales trends by outlet age. These insights aim to support improved marketing, inventory management, and strategic decisions.

---

## Dataset Overview

The dataset consisted of detailed transactional sales information, including:

- Product features such as Item Fat Content, Item Type, Item Weight, and Rating
- Outlet characteristics such as Outlet Location Tier, Size, Type, and Establishment Year
- Sales data per item and outlet combination

This rich dataset enabled a multi-faceted analysis of sales drivers across customer preferences and store properties.

---

## Data Cleaning and Preprocessing

Cleaning was performed particularly on the `Item_Fat_Content` field to ensure consistency and accuracy. Multiple variations of the same category (e.g., 'LF', 'low fat' vs. 'Low Fat') were standardized to improve data quality and uniformity, critical for reliable analysis and reporting.

For example:

```
update everyday_data
set item_fat_content =
case
  when item_fat_content in ('lf', 'low fat') then 'low fat'
  when item_fat_content = 'reg' then 'regular'
  else item_fat_content
end;
```

Verification queries were run to confirm the cleaning was successful.

---

## Exploratory Data Analysis and Key Metrics

Using SQL queries and Python libraries (Pandas, Matplotlib, Seaborn), key performance indicators and detailed aggregations were generated, including:

- Total Sales (in millions)
- Average Sales per item
- Number of items in the dataset
- Average customer rating

Sales were further analyzed by:

- Fat content categories
- Item types (product categories)
- Fat content distribution across outlet types
- Sales grouped by outlet establishment year
- Outlet size sales distribution percentages
- Sales by outlet location type
- Comprehensive metrics by outlet type including sales, averages, item counts, ratings, and item visibility

These analyses provided granular insights into sales patterns and customer preferences.

---

## Visualization and Reporting

Visual representations of the data were created in Python and Power BI, including:

- Donut chart showing total sales by fat content
- Bar chart depicting total sales by item type
- Stacked column chart illustrating fat content contribution by outlet type
- Line chart showing sales trends over outlet establishment years
- Pie chart for sales distribution by outlet size
- Funnel map visualizing sales by outlet location
- Matrix card summarizing all key metrics by outlet type

These visuals enhanced understanding and communication of complex data insights to stakeholders.

---

## Business Insights

- Total sales volume reached approximately $1 million from over 7,000 items, with an average sale of $141 and strong customer satisfaction (average rating ~3.96).
- Sales contributions from Low Fat and Regular fat content products were nearly equal (~49% and 50%), indicating balanced customer demand for both healthier and classic options.
- Top-performing item categories were Fruits & Vegetables, Snack Foods, and Household products, highlighting key revenue drivers.
- Customer satisfaction was highest in categories like Meat, Canned goods, Household items, Baked Goods, Health products, Dairy, and Frozen Foods.
- Tier 2 outlets and medium-sized stores consistently generated the largest proportions of revenue, guiding future expansion and investment focus.
- Yearly sales by outlet establishment year showed a stable growth trend, with minor variations signaling steady business maturity.
- Grocery Stores, Supermarket Type1, and Supermarket Type2 had similar total and average sales per item, though Grocery Stores excelled in customer loyalty reflected by higher ratings.

---

## Conclusion

This project demonstrates how product and outlet attributes influence sales dynamics in grocery retail. Data cleaning and thorough analysis led to actionable business insights that can support marketing strategy, inventory control, and store management optimization. Practical skills in SQL, Python, and Power BI were strengthened through end-to-end data analysis and visualization.

---
