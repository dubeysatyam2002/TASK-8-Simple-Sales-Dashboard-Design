📊 Task 8 — Simple Sales Dashboard Design

This project demonstrates how to create a basic interactive sales dashboard using Tableau, supported by Python (Jupyter Notebook) for light data cleaning.
The dashboard helps visualize sales trends, regional performance, and category-wise sales distribution.

🎯 Objective

Create an interactive dashboard that displays:

Sales over time (Month-Year)

Sales by Region

Sales by Category

Includes filters and basic formatting to highlight key insights

🛠 Tools Used

Tableau Public / Tableau Desktop

Python (Pandas)

Jupyter Notebook

Dataset: Superstore.csv
Columns used: Order Date, Region, Category, Sales, Profit

📁 Files Included in This Repository
File Name	Description

Superstore.csv	Original dataset

Superstore_cleaned.csv	Cleaned dataset (Month-Year added)

Task8_Python_Cleaning.ipynb	Jupyter Notebook used for cleaning

Task8_Dashboard.pdf / Dashboard_Screenshot.png	Exported Tableau dashboard

Task8_Insights.txt	Contains 3–4 business insights

README.md	Project documentation

🧹 Part 1 — Data Cleaning (Python + Jupyter Notebook)
Steps Performed:

Loaded the Superstore dataset in Jupyter Notebook

Converted Order Date to datetime format

Extracted Month_Year using strftime('%b-%Y')

Checked for missing values

Exported cleaned dataset as Superstore_cleaned.csv

Python Code Used
import pandas as pd

df = pd.read_csv("Superstore.csv")

df['Order Date'] = pd.to_datetime(df['Order Date'])
df['Month_Year'] = df['Order Date'].dt.strftime('%b-%Y')

df.to_csv("Superstore_cleaned.csv", index=False)

📊 Part 2 — Dashboard Creation in Tableau
Steps Followed in Tableau
1. Import Dataset

Open Tableau → Connect → Text File

Select: Superstore_cleaned.csv

2. Create Visuals
🟦 Line Chart: Sales Over Months

Drag Month_Year → Columns

Drag Sales → Rows

Select Line Chart from Show Me

🟧 Bar Chart: Sales by Region

Drag Region → Columns

Drag Sales → Rows

Select Horizontal Bar Chart

🟩 Donut Chart: Sales by Category

Drag Category → Color

Drag Sales → Label

Use Pie Chart → Convert to Donut using dual-axis technique

3. Add Filters

Drag Region → Filters

Right-click → Show Filter (acts as slicer)

4. Apply Colors

Used color encoding to highlight top-performing regions & categories

5. Build Final Dashboard

Click New Dashboard

Drag all worksheets onto the canvas

Arrange in tiled layout

Adjust size and formatting

Add titles and legends

6. Export Dashboard

File → Export as Image or Export as PDF

📑 Insights (3–4 Key Observations)

West region recorded the highest sales, with consistent performance across multiple months.

Technology category contributed the largest share to total sales, followed by Office Supplies.

Sales show a noticeable upward trend towards the end of the year, indicating seasonal demand.

Regional sales distribution reveals performance gaps, making the West a primary revenue driver.

✅ Outcome

Successfully built a clean, interactive, and business-ready dashboard that helps stakeholders:

Understand monthly sales trends

Compare regional performance

Identify high-performing product categories

Use filters for dynamic exploration

This project improves skills in Tableau visualization, data cleaning, and business insight generation.

This repository is created as beginer for learning purpous only!
