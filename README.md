  #                                   ADVENTURE WORKS SALES DASHBOARD

<summary>Click to expand Table of Contents</summary>

- [Introduction](#introduction)  
- [Product Lifecycle Profitability Analysis](#product-lifecycle-profitability-analysis)  
- [ETL Process](#etl-process)  
- [Dashboard Overview](#dashboard-overview)  
- [Results / Insights](#results--insights)  


---

# Introduction 

Adventure Works is a global company that manufactures and retails bikes and related components. The company sells its products in North America, Europe, and Oceania.  

This project presents an **interactive Power BI dashboard** analyzing Adventure’s sales performance. It provides **real-time insights for strategic decision-making**, tracking profitability across product categories and customer segments over time.  

The analysis is based on the **Adventure Works 2022 database**, combining sales data from 2011 to 2014 across multiple schemas:  
- **Sales**: Orders, Invoices, Customers, Sales Territory  
- **Production**: Product Management  

Key business questions addressed:  
- Which product generates the most revenue?  
- How does sales growth vary over time?  
- What are the forecasted trends for future demand and revenue?  

---

# Product Lifecycle Profitability Analysis

## Product Lifecycle Profitability Analysis
This report dives deep into Adventure’s sales performance, helping decision-makers:  
- Identify growth opportunities  
- Manage seasonal revenue declines  
- Understand customer spending behavior  
- Personalize marketing and retention strategies  

By tracking performance across products, geographies, and customer segments, the dashboard provides **actionable insights into business performance**.

---
## ETL Process
The analysis followed a structured **ETL pipeline**:

### - Data Extraction
- Connected Power BI to SQL Server Management Studio  
- Imported relevant tables: `SalesCustomer`, `SalesOrderDetails`, `SalesOrderHeader`, `SalesTerritory`, `ProductCategory`, `ProductSubcategory`, `Product`  

### -  Data Cleaning
- Handled missing values using complete case analysis  
- Removed duplicates (e.g., product names)  
- Corrected inconsistent values (e.g., negative prices/quantities)  
- Renamed ambiguous columns (e.g., *Group → Sales Region*, *Name → Country*)  

### -  Data Transformation
- Merged tables (`SalesOrderDetail`, `SalesOrderHeader`, `Product`, `Category`, `Subcategory`, `Customer`)  
- Created calculated columns (profit, costs, YoY, MoM, RFM metrics)  
- Built supporting tables (DateTime, Top 6 Products, Bottom 6 Products)  

### -  Data Modeling
- Established **one-to-many relationships** across schemas  
- Ensured relational integrity for analysis  

**Schema Diagram:**  
<img width="695" height="496" alt="Schema" src="https://github.com/user-attachments/assets/cd3c5277-38b2-4be7-8c16-9db87e5e09a9" />

---
##  Dashboard Overview

### -  Sales Performance Dashboard
<img width="865" height="490" alt="Sales Dashboard" src="https://github.com/user-attachments/assets/9acefa34-adec-4ae1-b9fa-f66959db7206" />

### -  Profitability Analysis Dashboard
<img width="768" height="438" alt="Profitability Dashboard" src="https://github.com/user-attachments/assets/af312a7c-07d6-42e0-9df1-35e71cdfa453" />

### -  Geographical Analysis Dashboard
<img width="770" height="436" alt="Geographical Dashboard" src="https://github.com/user-attachments/assets/09d44654-7901-4118-9e0f-1efef6ce1401" />

---

##  Results / Insights

- **Top Revenue Drivers**: Bikes, Clothing, and Accessories (profit margin ~9.06%, ≈ $8.8M)  
- **Regional Performance**: Pacific region leads with ~32.36% profit margin  
- **High Margin Products**: Accessories (>50% return rates)  
- **Most Ordered Product**: Road Bikes  
- **Most Profitable Product**: Mountain Bikes  
- **Least Profitable Product**: Road Frame (loss ≈ $173K from 2011–2014)  

###  Overall Performance (2011–2014)
- Total Sales: ≈ $109.85M  
- Total Profit: ≈ $9.37M  
- Year-over-Year Growth: ≈ 69.41%  

### Underperforming Regions
- Central America: -3.88% margin  
- North America: 1.8% margin  
- Southern America: -1.92% margin  

---

## Recommendations

Based on the insights, the following strategic actions are recommended:

1. **Focus on High-Margin Products**  
   - Increase marketing and production of Accessories and Mountain Bikes.  
   - Bundle high-margin products with popular items to maximize profitability.  

2. **Address Underperforming Regions**  
   - Investigate causes of low profitability in Central, North, and Southern America.  
   - Implement targeted promotions and localized marketing strategies.  
   - Optimize distribution channels to reduce costs.  

3. **Product Lifecycle Management**  
   - Phase out or redesign low-performing products like Road Frames.  
   - Introduce new product lines to sustain growth and meet forecasted demand.  

4. **Customer Segmentation & Retention**  
   - Use RFM (Recency, Frequency, Monetary) analysis to identify loyal customers.  
   - Launch personalized campaigns to improve retention and upselling.  

5. **Seasonal Strategy**  
   - Prepare inventory and marketing campaigns ahead of Q4 peak sales.  
   - Diversify product offerings to mitigate seasonal revenue declines.  

---

![Image](https://github.com/user-attachments/assets/a2957299-6c8f-469a-bcb7-bfd7e3273289)






## Introduction

This report analyzes Adventure’s sales performance to provide real-time insights for strategic decision-making. It tracks profitability across product categories and customer segments over time, helping identify growth opportunities, manage seasonal revenue declines, and understand customer spending behavior.

Adventure Works is a global company that manufacturer and retails bikes and related components. The company sells its products in North America, Europe, and Oceania, among other locations.
This report dives deep into Adventure's sales performance, arming decision-makers with real-time insights for strategic excellence. The present project aimed at tracking Adventure's profitability across product categories and customer segments. By tracking performance over time across product and customer segments, the company will easily identify growth opportunities and efficiently manage seasonal depressions in revenue. It also helps to understand customers' spending behaviour, a contribution to personalised marketing and retention strategies. Meaning that this report is designed to provide actionable insights into business performance across products, geographies, customer segments, and time periods.
Throughout the project, these questions will drive our analysis: which product generates the most revenue, how does the sales growth vary over time, and what is the trend for future demands and revenues (based on forecasted values)?
The analysis is based on the Adventure Works 2022 database, which contains different tables such as product management, HR and sales operations, manufacturing and purchasing and customer orders. The dataset combines sales data from 2011 to 2014.

To conduct the analysis, the key schema included:
- Sales: Orders, Invoices, Customers, Sales Territory.
- Production: Production Product.
  
- [ETL Process](#ETL-Process)
  
This process describes the various steps taken from ETL to analysis.

The path followed was:

- Data extraction
  
The start point was to establish the connection between Power BI and SQL Server Management Studio, facilitating the importation of relevant tables for the analysis (Sales Customer, Sales SalesOrder Details, Sales SalesOrderHeader, Sales SalesTerritory, Production ProductCategory, Production ProductSubcategory and Production Product).
- Data Cleaning

Before analysis, data cleaning was essential, helping to improve the quality of the data and making it consistent, accurate, and trustworthy. During this phase missing values were handled using complete case analysis (removing the row or column containing the missing values), especially if it concerns the primary key. To ensure data uniqueness, duplicates were removed as well before analysis (for the sample in product names). We also check for any instances of incorrect or inconsistent values, such as negative prices or quantities. Finaly we also rename some column/feature to avoid ambiguity (e.g. group to Sales Region, Name to Country in Sales Territory table, Name to Product Name in Product Table, ….).  
- Data transformation

In this phase, before creating extra columns, some tables were merged: Sales SalesOrderDetail with Sales SalesOrderHeader, Product Product, Product Category and Product Subcategory, Customer and Person Person. After merging, extra columns were created or added; this was helpful before we could calculate certain measures like total profit, customer segment, total costs, YoY, MoM, frequency, monetary, recency, etc. To extract more insight from row data, extras tables were as well created: DateTime table was created before preforming some time intelligence function and Top06 and 06 Botton products tables were as well, helping in filtering the most/least performant sub product in the list.
- Data modelling

To ensure that the different schemas were not in silos, relationships were established based on the primary key. One-to-many relationships were the most frequent among tables. The figure below presents the relationship between different tables.


<img width="695" height="496" alt="Image" src="https://github.com/user-attachments/assets/cd3c5277-38b2-4be7-8c16-9db87e5e09a9" />

After ensuring that all the data is safeguarded from messes, developing interactive dashboard follows using KPI, line charts, matrix, gauge, sheep map, and tree map. 

- [Dashboard Overview](#dashboard--overview)
  
<img width="865" height="490" alt="Image" src="https://github.com/user-attachments/assets/9acefa34-adec-4ae1-b9fa-f66959db7206" />

## Profitability Analysis Dashboard
<img width="768" height="438" alt="Image" src="https://github.com/user-attachments/assets/af312a7c-07d6-42e0-9df1-35e71cdfa453" />

## Geographical Analysis Dashboard
<img width="770" height="436" alt="Image" src="https://github.com/user-attachments/assets/09d44654-7901-4118-9e0f-1efef6ce1401" />

- [Results / Insights](#results--insights)

The visual analysis of different metrics leads to the conclusion that Bike, Clothing and accessories drive the most revenue (generating a profit margin of 9.06% approximately m.u 8.8M), and Pacific region (profit of around 32.36%). Accessories have the highest margin profit or return rates (over 50%). Road bikes are the most order sub product and the mountain Bike is topmost profitable. However, the Road frame is least product in term of profitability (generating a loss of 173 K from 2011 to 2014). Generally, from 2011 to 2014: the company generated around m.u $109.85 million in sales and $9.37 million in profit, reflecting a 69.41% year-over-year growth.
The analysis helps to identify underperforming regions like Central, North and Southern America. With respectively a negative margin profit of -3.88%, 1.8%, and -1.92%. These results are essential in guiding future decision making (resources allocation and marketing strategies).
 The whole scene is described as follow:

### Profitability insights:
#### Sales performance
From 2011 to 2014: the company generated around $109.85 million in sales and $9.37 million in profit, reflecting a 69.41% year-over-year growth.
Top product:  accessories, Bikes and Clothing are the most ordered product, generating the highest margin profit.  Accessories lead with 41 000 orders, trailed by bikes at 37000 orders, and clothing at 21 000 orders. These three product categories have impact on Adventure sales landscape. Specially, accessories have the highest margin profit or return rates (over 50%).
Road bikes are the most order sub product and the mountain Bike is topmost profitable. While the Road frame is least product in term of profitability (generating a loss of $173 K from 2011 to 2014).
### Regional insight/Geographical Analysis  
The Business is run in 3 region (Pacific, Europe and North America) and 10 countries with Europe and Pacific generating over half of the total revenue.
-	Europe itself accounted of most of the order (27 000) and profit ($317 millions).
-	As individual country Australia accounted for most orders (15000) and profit ($343 millions).
The analysis helps to identify underperforming regions like Central, North and Southern America. With respectively a negative margin profit of -3.88%, 1.8%, and -1.92%. These results are essential in guiding future decision making (resources allocation and marketing strategies).
### Time-based analysis
A seasonal trend can be seen based on different periods (monthly, quarterly, or yearly). The peak is most often observed in January, June, August, October, and December. In term years, 2014 exhibits the highest overall best performance (margin profit of 17.16% and YoY growth of 32.12%).
### Customer segment and growth analysis
- The company acquired 19000 customers over four years, processing 121000 orders at an average order value of $709.3.
-   The different customers are grouped into three segments: champions (1243 customers), at risk (3876 customers), and loyal customers (488 customers).
### Product Life Cycle
To know how products behave over time, or the adventure process went through from the initial phase until the retirement from the market. These phases were divided into introduction (low sales), growth (increases in sales), maturity (sales slowdown because of competition and saturation of the market) and decline (sales decline and profit).
For the specific case of Adventure, some of its subcategory products were at introduction (cable lock, front brakes, …), maturity (Fender Set-Mountain, HL Mountain Tire, HL Road Tire, Touring Tire Tube, Water Bottle, …), and decline (Hitch Rack-4-Bike, Hydration Pack-70).

- [Recommendations](#recommendations)

- In order to enhance profitability, it is imperative for the organisation to allocate additional resources towards accessories and bikes, as these represent the foremost revenue-generating product categories.
-  Establish promotional strategies for the highest-selling products (accessories, bicycles, and clothes).
-  Concentrate marketing initiatives on regions exhibiting superior performance as determined by data analysis.
- Augment promotional activities to increase the visibility of products that are in the introductory phase.
- In the context of products situated within the maturity phase, it is imperative for the organization to critically evaluate their design or implement a discount strategy during the purchasing process, thereby minimizing inventory holding expenditures.
- Given that the peak sales months are already established (January, June, August, October, and December), Adventure should strategically capitalize on these fluctuations by offering early-bird discounts.
- Furthermore, the company ought to formulate strategies that focus on the retention of both champion and loyal customers; these strategies may encompass rewarding these individuals and inviting them to exclusive events. In relation to customers who are deemed at risk, the organization should systematically gather their feedback and modify their offerings to better align with these customers' needs.



- [License](#license)

</details>
