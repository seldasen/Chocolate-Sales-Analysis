<div style='background-color:#714737; padding: 15px; border-radius: 5px;'>
<h2 style='color:#FEFEFE; text-align:center;'> CHOCOLATE SALES ANALYSIS</h2>
</div>


<h2 style='color:#714737;'>Chocolate Sales Analysis</h2>is a comprehensive data analysis project designed to explore, analyze, and visualize chocolate sales data across multiple countries. Built using Python and various data analysis libraries, this project provides insights into sales trends, product performance, and regional demand through intuitive visualizations and statistical analysis. The dataset is sourced from Kaggle (link provided below) and is of a reasonable size, well under the 100GB repository limit.


<h2 style='color:#714737;'>Dataset Content</h2>
The dataset used in this project is the **Chocolate Sales Dataset** from Kaggle:  
[https://www.kaggle.com/datasets/atharvasoundankar/chocolate-sales](https://www.kaggle.com/datasets/atharvasoundankar/chocolate-sales)  

It contains detailed records of chocolate sales transactions, including:  
- **Dataset**: 1094 rows × 5 columns
- **Amount**: Sales revenue in dollars  
- **Boxes Shipped**: Number of chocolate boxes shipped per transaction  
- **Country**: Six countries (Australia, Canada, India, New Zealand, UK, USA)  
- **Product**: Specific chocolate products (e.g., Smooth Silky Salty, 50% Dark Bites)  
- **Date**: Transaction dates spanning from Jan - Aug 2022 
- **Salesperson**: Names of salespeople (removed during cleaning)  
The dataset is relatively clean with no missing, empty, or duplicate values, making it suitable for analysis after minor preprocessing. 

**PowerBi Dasboard**

![PowerBi Dasboard](<Output/PowerBi Dashboard.png>)


**Tableau Dashboard**

![Tableau Dashboard](<Output/Tableau Dashboard.png>)

<h2 style='color:#714737;'>Business Requirements</h2>

1. **Understand Sales Distribution**: Identify total sales and percentage contributions by country and product category.  
2. **Identify Top Performers**: Determine the top-selling products and countries driving revenue.  
3. **Analyze Efficiency**: Calculate revenue per box shipped to assess profitability across products and categories.  
4. **Explore Trends**: Investigate sales trends over time, focusing on seasonality and holiday impacts.  
5. **Visualize Insights**: Provide clear, actionable visualizations for stakeholders to understand key findings.

<h2 style='color:#714737;'>Dashboard Users</h2>

Marketing Professionals, Sales Managers, Product Managers, Retail Partners, Data Analysts,  Executives and Business Owners.


**Business KPIs (Key Performance Indicators)**

• Total Sales Revenue– Measure of overall performance.
Average Revenue per Box Shipped – Indicates profitability per shipment.
• Sales Growth Over Time – Month-over-month or year-over-year comparison.
• Sales Performance by Country – Identifies high-performing regions.
• Product Performance Analysis – Determines best-selling and most profitable products.

**Expected Outcome**

Sales Trends Analysis Report – Identifying peak sales periods and seasonality effects.
Product Performance Dashboard – Highlighting top-selling and high-revenue products.
Revenue Optimization Strategy – Recommendations for improving profitability.

<h2 style='color:#714737;'>Hypotheses and Validation</h2>

1. **H1: Sales follow seasonal trends, with higher revenue during peak holiday months.**

   - **Validation**: Analyze monthly sales trends (e.g., January vs. February) using line charts and heatmaps.  
   - **Key Insight**: Holiday-driven sales spikes (e.g., January peak at $896,105).  

2. **H2: Certain countries have higher chocolate sales, and sales amount correlates with boxes shipped.**
   - **Validation**: Compare total sales and boxes shipped per country using choropleth maps and bubble charts.  
   - **Key Insight**: Australia leads with $1,137,367, but correlation between sales and boxes shipped is weak (-0.0188).  

3. **H3: Premium chocolate products generate higher revenue per box shipped.**
   - **Validation**: Calculate revenue per box shipped and visualize with box plots and stacked bar charts.  
   - **Key Insight**: Premium products like Smooth Silky Salty show higher efficiency.  

4. **H4: Some chocolate products drive revenue more efficiently than others, making them more profitable.**  
   - **Validation**: Assess sales and revenue per box shipped per product using bar and bubble charts.  
   - **Key Insight**: Smooth Silky Salty ($349,692) outperforms others in revenue and efficiency.
---

<h2 style='color:#714737;'>Project Plan</h2>

1. **Data Collection**: Downloaded the dataset from Kaggle. 

2. **Data Processing**:  
   - Removed the "Salesperson" column (irrelevant to analysis).  
   - Converted "Amount" from string (with "$") to numeric data type.  
   - Standardized "Date" to YYYY-MM-DD format.  
   - Added columns: Day, Month Number, Month Name, Revenue per Box Shipped (Amount / Boxes Shipped).  

3. **Analysis**: Calculated total sales, percentages, trends, and efficiency metrics.  

4. **Visualization**: Created charts (e.g., bar, line, stacked bar) using Python libraries.  

5. **Interpretation**: Summarized key findings and validated hypotheses.
The data was managed using pandas for cleaning and analysis, ensuring consistency throughout the process. We chose these methodologies for their simplicity and effectiveness in handling structured data.

 <h2 style='color:#714737;'>Rationale for Mapping Business Requirements to Advance Data Visualizations</h2>

- **Sales Distribution**: Tree map for percentage by country, bar chart for product category sales.  
  - *Rationale*: Highlights relative contributions clearly for stakeholders.  
- **Top Performers**: Bar chart for top 5 products and countries.  
  - *Rationale*: Simple and effective for ranking comparisons.  
- **Efficiency**: Stacked bar chart for revenue per box shipped by category.  
  - *Rationale*: Shows efficiency across dimensions.  
- **Trends**: Line chart for monthly sales trends.  
  - *Rationale*: Reveals temporal patterns intuitively.

<h2 style='color:#714737;'>Analysis Techniques Used</h2>

- **Descriptive Statistics**: Calculated mean ($5,652.31), median ($4,868.50), min ($7), and max ($22,050) for sales.  
- **Correlation Analysis**: Computed Sales vs. Boxes Shipped correlation (-0.0188).  
- **Aggregation**: Summed sales by country, product, and category.  
- **Time Series Analysis**: Analyzed monthly sales trends.  
**Limitations**: The weak correlation limited insights into shipment efficiency. An alternative could be regression analysis to explore other variables (not present in the dataset). The data’s simplicity (no missing values) didn’t require advanced imputation techniques.
**Structure**: Techniques were applied sequentially—cleaning first, then descriptive stats, followed by visualizations—to build a logical flow. The dataset’s size and quality posed no significant limitations.
**Generative AI**: Used for ideation (e.g., suggesting visualization types) and code optimization (e.g., efficient pandas operations).

 <h2 style='color:#714737;'>Ethical Considerations</h2>

- **Data Privacy**: Salesperson names were removed to anonymize data, avoiding personal identification.  
- **Bias**: No evident bias in country or product data, though India’s high sales might reflect sampling bias (not explored further due to dataset limitations).  
- **Legal**: Dataset is publicly available on Kaggle under an open license, ensuring compliance.
---
<h2 style='color:#714737;'>Dashboard Design</h2>

### Pages and Content
1. **Main page**: Summary statistics (average sales, boxes shipped), key findings text block.  
2. **Sales by Country**: Choropleth map, treemap, top 5 countries bar chart.  
3. **Product Performance**: Bar charts (total revenue by product/product category), stacked bar (revenue per box).  
4. **Trends**: Line chart (monthly sales).  
5. **Communication**:  
- **Technical Audience**: Detailed stats and correlation insights in tables.  
- **Non-Technical Audience**: Simplified charts with annotations (e.g., "Total Revenue by Country"). 

<h2 style='color:#714737;'>Unfixed Bugs</h2>

- **Minor Rounding Error**: Revenue per box shipped occasionally shows slight discrepancies due to floating-point precision in Python. Left unfixed as it doesn’t impact insights significantly.  
- **Knowledge Gaps**: Initially unfamiliar with heatmap creation; resolved by studying Matplotlib/Seaborn documentation.
---
<h2 style='color:#714737;'>Development Roadmap</h2>

- **Challenges**: Standardizing dates and handling weak correlations. Overcome by using pandas’ `to_datetime` and focusing on descriptive stats instead of predictive models.  
- **Next Steps**: Practice advanced visualization tools (e.g., Tableau) and learn time series sales forecasting techniques.
---

<h2 style='color:#714737;'>Deployment:</h2>

* Deployed with Tableau file Chocolate_sales_analysis.twbx and Chocolate Sales Analysis Dashboard.pbix in output folder.
* Steps:
1. Processed and cleaned the data using Python (pandas).
2. Exported the cleaned dataset as a CSV file.
3. Imported the CSV into Tableau Public and PowerBi.
4. Designed interactive dashboards with charts and filters as outlined in the Dashboard Design section.
Initially Tableau was chosen for deployment due to its powerful map visualization capabilities and ability to share interactive dashboards with a broad audience but theb it was also created in PowerBi due to its advance filtering and interactive dashboarding.
---

<h2 style='color:#714737;'> Main Data Analysis Libraries</h2>

- **pandas**: Data cleaning, aggregation (e.g., `df.groupby('Country')['Amount'].sum()`).  
- **NumPy**: Statistical calculations (e.g., mean, std).  
- **Matplotlib/Seaborn**: Visualizations (e.g., bar charts, line plots).  
---

<h2 style='color:#714737;'>Credits</h2>

### Content
- Dataset sourced from: [Kaggle Chocolate Sales Dataset](https://www.kaggle.com/datasets/atharvasoundankar/chocolate-sales).  
- Visualization ideas inspired by Seaborn documentation.  
### Media
- Icons for dashboard footer from [Font Awesome](https://fontawesome.com/).  
---
<h2 style='color:#714737;'>Acknowledgements</h>

_ Recording and screenshots taken from dashboards and jupyter notebook

Thanks to the team for their collaborative efforts in data cleaning, analysis, and visualization design. Special thanks to AI for providing Team 3 with ideas which significantly contributed to ideation, structuring, and enhancing the quality of this README.  
