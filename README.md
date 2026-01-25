  #                                   ADVENTURE WORKS SALES DASHBOARD

# Product Lifecycle Profitability Analysis
This report analyzes Adventure’s sales performance to provide real-time insights for strategic decision-making. It tracks profitability across product categories and customer segments over time, helping identify growth opportunities, manage seasonal revenue declines, and understand customer spending behavior.

Adventure Works is a global company that manufacturer and retails bikes and related components. The company sells its products in North America, Europe, and Oceania, among other locations.
This report dives deep into Adventure's sales performance, arming decision-makers with real-time insights for strategic excellence. The present project aimed at tracking Adventure's profitability across product categories and customer segments. By tracking performance over time across product and customer segments, the company will easily identify growth opportunities and efficiently manage seasonal depressions in revenue. It also helps to understand customers' spending behaviour, a contribution to personalised marketing and retention strategies. Meaning that this report is designed to provide actionable insights into business performance across products, geographies, customer segments, and time periods.
Throughout the project, these questions will drive our analysis: which product generates the most revenue, how does the sales growth vary over time, and what is the trend for future demands and revenues (based on forecasted values)?
The analysis is based on the Adventure Works 2022 database, which contains different tables such as product management, HR and sales operations, manufacturing and purchasing and customer orders. The dataset combines sales data from 2011 to 2014.
To conduct the analysis, the key schema included:
Sales: Orders, Invoices, Customers, Sales Territory.
Production: Production Product

## ETL Process 
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

## Dashboard overview
<img width="865" height="490" alt="Image" src="https://github.com/user-attachments/assets/9acefa34-adec-4ae1-b9fa-f66959db7206" />

## Profitability Analysis Dashboard
<img width="768" height="438" alt="Image" src="https://github.com/user-attachments/assets/af312a7c-07d6-42e0-9df1-35e71cdfa453" />

## Geographical Analysis Dashboard
<img width="770" height="436" alt="Image" src="https://github.com/user-attachments/assets/09d44654-7901-4118-9e0f-1efef6ce1401" />


## Insights

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
## Recommendations:
- In order to enhance profitability, it is imperative for the organisation to allocate additional resources towards accessories and bikes, as these represent the foremost revenue-generating product categories.
-  Establish promotional strategies for the highest-selling products (accessories, bicycles, and clothes).
-  Concentrate marketing initiatives on regions exhibiting superior performance as determined by data analysis.
- Augment promotional activities to increase the visibility of products that are in the introductory phase.
- In the context of products situated within the maturity phase, it is imperative for the organization to critically evaluate their design or implement a discount strategy during the purchasing process, thereby minimizing inventory holding expenditures.
- Given that the peak sales months are already established (January, June, August, October, and December), Adventure should strategically capitalize on these fluctuations by offering early-bird discounts.
- Furthermore, the company ought to formulate strategies that focus on the retention of both champion and loyal customers; these strategies may encompass rewarding these individuals and inviting them to exclusive events. In relation to customers who are deemed at risk, the organization should systematically gather their feedback and modify their offerings to better align with these customers' needs.

![Image](https://github.com/user-attachments/assets/a2957299-6c8f-469a-bcb7-bfd7e3273289)
