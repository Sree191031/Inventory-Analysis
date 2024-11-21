# Inventory Management Analysis

**Project Overview**

The fictional company is a medium-sized manufacturer focused on producing electronic components. It offers a diverse range of products and oversees an inventory that includes raw materials, work-in-progress (WIP) items, and finished goods. The company has been facing several inventory management issues, such as stockouts, excess inventory, and increasing carrying costs

The business requirements aim to optimize inventory levels, reduce stockouts, minimize excess inventory, and improve efficiency, ultimately lowering carrying costs and enhancing operational performance.

### Business Strategy Insights

**1. ABC Analysis**
Prioritize high-value items (A-class) to maximize revenue and optimize inventory management.

**2. Economic Order Quantity (EOQ) Analysis**
Optimize order quantities to minimize total inventory costs, balancing ordering and holding expenses.

**3. Reorder Point Analysis**

Ensure timely restocking by calculating accurate reorder points based on sales velocity and lead time.**

**4. Lead Time Analysis**

Minimize stockouts and overstocking by analyzing and reducing lead times across suppliers and products.**

- The dataset is sourced from the Kaggle Inventory Case Study and consists of 1,048,575 rows and 15 columns.
---
### Business Analysis and Insights

#### ABC Analysis

We executed an ABC analysis by binning 7000+ brands into three categories [A, B, C] based on their total sales distribution:

- **A-Class** contributed to 80% of total revenue.
- **B-Class** contributed to 15% of total revenue.
- **C-Class** contributed to 5% of total revenue.


<div align="center">
  <img src="https://github.com/Sree191031/Inventory-Analysis/blob/main/Images/ABC%20Analysis.png" width="640" height="360" />
</div>
Further analysis showed that the top 50 brands in the A-Class contributed to 25% of the total revenue. 
<div align="center">
  <img src="https://github.com/Sree191031/Inventory-Analysis/blob/main/Images/Top%2050%20brands.png" width="640" height="360" />
</div>

#### Sales Store Analysis

Sales store analysis revealed that high-volume products, predominantly in Class A, contributed the most to sales, whereas Class C had the least contribution. The highest sales were seen in stores 34, 15, 38, 76, and 10.

<div align="center">
  <img src="https://github.com/Sree191031/Inventory-Analysis/blob/main/Images/Store%20Sales.png" width="640" height="360" />
</div>

#### Supplier Analysis

DIAGEO North American Inc. is the highest contributing supplier for our business.

<div align="center">
  <img src="https://github.com/Sree191031/Inventory-Analysis/blob/main/Images/Vendor%20Sales.png" width="640" height="360" />
</div>

#### Economic Order Quantity (EOQ) Analysis

There is a significant correlation between sales quantity demand and EOQ values at **0.87**, which suggests a strong relationship between demand and ordering needs.

<div align="center">
  <img src="https://github.com/Sree191031/Inventory-Analysis/blob/main/Images/EOQ%20-Sales%20Qty.png" width="640" height="360" />
</div>

We performed an EOQ analysis with holding cost as **30 %** the following results:

- **A-Class Products**:
  - Mean EOQ: 8.7 units
  - Standard Deviation: 13.59 units (indicating higher variability in ordering needs)
  - Maximum EOQ: 261 units (indicating outliers or exceptionally high-demand products)
  - Count: 3300 items (largest group, emphasizing their critical importance)

- **B-Class Products**:
  - Mean EOQ: 9.29 units (slightly higher than A-Class)
  - Standard Deviation: 13.41 units (similar variability to A-Class)
  - Maximum EOQ: 164 units
  - Count: 2405 items (moderate-sized group)

- **C-Class Products**:
  - Mean EOQ: 8.9 units (close to A and B)
  - Standard Deviation: 15.76 units (highest variability, indicating unpredictable demand patterns)
  - Maximum EOQ: 243 units (surprising for low-priority products, likely due to outliers)
  - Count: 1441 items (smallest group)


#### Stock Risk Evaluation

Using the EOQ values for each class, further analysis revealed the following:

- **Class B** has the highest risk of stockouts, followed by **Class A** and **Class C**. This indicates that Class B products are more prone to running out of stock.
<div align="center">
  <img src="https://github.com/Sree191031/Inventory-Analysis/blob/main/Images/Stockout%20Risk.png" width="640" height="360" />
</div>
  
#### Reorder Point Analysis

We analyzed reorder points based on sales velocity per day for each brand:

- **88% of brands** have reorder points below 100 units.
- **A-Class brands** need higher reorder points due to faster sales and consistent demand.

<div align="center">
  <img src="https://github.com/Sree191031/Inventory-Analysis/blob/main/Images/Reorder%20Points%20Analysis.png" width="640" height="360" />
</div>
    
#### Lead Time Analysis

Lead time analysis showed that:

- **70% of brands** had an average lead time of **7.25 to 8.25 days**.
- The shortest lead time observed was **2.75 to 3.25 days**

<div align="center">
  <img src="https://github.com/Sree191031/Inventory-Analysis/blob/main/Images/Reorder%20Points.png" width="640" height="360" />
</div>

#### Demand Forecasting

Due to data constraints, demand forecasting was conducted using time series analysis for a 2-month duration.
<div align="center">
  <img src="https://github.com/Sree191031/Inventory-Analysis/blob/main/Images/Sales%20Forecast.png" width="640" height="360" />
</div>

---
### Recommendations

1. **Optimize EOQ for B-Class Products:** Refine B-Class EOQ models to account for demand variability.
2. **Improve Replenishment Strategy:** Increase replenishment frequency for A-Class products to avoid stockouts.
3. **Refine Stock Levels for High-Risk Products:** Review reorder points for B-Class products to reduce stockout risk.
4. **Enhance Supplier Relationships:** Strengthen ties with top suppliers like DIAGEO for reliable stock.
5. **Focus on High-Volume Stores:** Prioritize stock management in top-performing stores to drive sales.
6. **Lead Time Reduction:** Work with suppliers to reduce lead time below 7 days for critical items.
7. **Time Series Forecasting Improvements:** Refine time series models to improve demand accuracy for the next 2 months.
8. **Monitor and Adjust Based on Performance:** Continuously track KPIs and adjust strategies to optimize supply chain efficiency.
---
**Future Analysis**

All mentioned KPIs can be used in developing a Power BI Dasboard. 

### KPI Metrics

1. **Revenue Distribution by Class:** Track the percentage of total revenue contributed by each class (A: 80%, B: 15%, C: 5%).
2. **EOQ Performance:** Monitor mean EOQ and standard deviation to balance ordering and minimize stockouts.
3. **Top Brands Contribution:** Ensure top 50 A-Class brands contribute 25% of total revenue.
4. **Sales by Store:** Identify and optimize sales in top-performing stores (34, 15, 38, 76, 10).
5. **Risk of Stockouts:** Monitor stockout risk, particularly for B-Class products.
6. **Reorder Points:** Adjust reorder points based on sales velocity, especially for A-Class brands.
7. **Lead Time:** Aim for an average lead time of 7.25–8.25 days for 70% of brands.
8. **Stockout Risk by EOQ Class:** Minimize stockout risk, especially in B-Class, through EOQ and reorder point adjustments.
9. **Demand Forecasting Accuracy:** Ensure demand forecasting accuracy for 2-month periods, focusing on A-Class.

---
### Conclusion

By implementing these KPIs and recommendations, we can enhance inventory management, optimize stock levels, and minimize risks associated with stockouts. This strategic approach will improve operational efficiency, drive sales, and support more accurate demand forecasting. Monitoring these KPIs will help us identify areas for improvement and ensure that we maintain a responsive, cost-effective supply chain, ultimately contributing to business growth and customer satisfaction.


