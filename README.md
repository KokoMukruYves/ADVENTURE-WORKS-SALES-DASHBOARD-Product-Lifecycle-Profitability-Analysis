  #                                   ADVENTURE WORKS SALES DASHBOARD

<img width="175" height="163" alt="Image" src="https://github.com/user-attachments/assets/03f1258a-6c39-491e-9600-9c6f7ae59c26" />


 ## Product Lifecycle Profitability Analysis



<details>
<summary id="introduction"> Introduction</summary>



Adventure Works is a global company that manufactures and retails bikes and related components. The company sells its products in North America, Europe, and Oceania.  

This project presents an **interactive Power BI dashboard** analyzing Adventure’s sales performance. It provides **real-time insights for strategic decision-making**, tracking profitability across product categories and customer segments over time.  

The analysis is based on the **Adventure Works 2022 database**, combining sales data from 2011 to 2014 across multiple schemas:  
- **Sales**: Orders, Invoices, Customers, Sales Territory  
- **Production**: Product Management  

Key business questions addressed:  
- Which product generates the most revenue?  
- How does sales growth vary over time?  
- What are the forecasted trends for future demand and revenue?  


This report dives deep into Adventure’s sales performance, helping decision-makers:  
- Identify growth opportunities  
- Manage seasonal revenue declines  
- Understand customer spending behavior  
- Personalize marketing and retention strategies  

By tracking performance across products, geographies, and customer segments, the dashboard provides **actionable insights into business performance**.

</details>

---

<details>
<summary id="etl-process"> ETL Process</summary>


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

</details>

---
<details>

<summary id="dashboard-overview">Dashboard Overview</summary>


###  Sales Performance Dashboard
<img width="865" height="490" alt="Sales Dashboard" src="https://github.com/user-attachments/assets/9acefa34-adec-4ae1-b9fa-f66959db7206" />

###  Profitability Analysis Dashboard
<img width="768" height="438" alt="Profitability Dashboard" src="https://github.com/user-attachments/assets/af312a7c-07d6-42e0-9df1-35e71cdfa453" />

###  Geographical Analysis Dashboard
<img width="770" height="436" alt="Geographical Dashboard" src="https://github.com/user-attachments/assets/09d44654-7901-4118-9e0f-1efef6ce1401" />

</details>

---
<details>

<summary id="results--insights"> Results / Insights</summary>



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

</details>

---
<details>

<summary id="recommendations"> Recommendations</summary>


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

</details>

---

[![Power BI Dashboard](https://img.shields.io/badge/Click_here_to_access_the_interactive_dashboard-F2C811?style=for-the-badge&logo=microsoftpowerbi&logoColor=black)](https://app.powerbi.com/links/K2dMandbYQ?ctid=941bbf5f-f2c0-4875-a24c-6907865d251a&pbi_source=linkShare)


## 🔗 Connect with me

For questions or collaborations, feel free to reach out!

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/koko-mukuru-yves-98621a14a) 
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:kokomukuruy@gmail.com)

---
<p align="center">
  <i>"Turning data into actionable intelligence, one project at a time."</i>
</p>

**© 2026 Koko Mukuru Yves**. All rights reserved




