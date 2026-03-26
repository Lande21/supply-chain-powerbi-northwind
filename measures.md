## Key DAX Measures

- Total Sales LY = 
CALCULATE(
    [Total Sales],
    SAMEPERIODLASTYEAR('vw_OrdersAnalysis'[OrderDate].[Date])
)

- Total Orders LY = 
CALCULATE(
    [Total Orders],
    SAMEPERIODLASTYEAR(vw_OrdersAnalysis[OrderDate])
)
- On-Time Delivery % = DIVIDE([On-Time Deliveries], COUNTROWS(vw_ShipmentsPerformance))
- On-Time Deliveries = CALCULATE(COUNTROWS(vw_ShipmentsPerformance), vw_ShipmentsPerformance[DeliveryStatus] = "On Time")
- Total Revenue = SUM(OrderDetails[UnitPrice] * OrderDetails[Quantity])
- Average Order Value = [Total Revenue] / DISTINCTCOUNT(Orders[OrderID])
- Orders Count = COUNT(Orders[OrderID])

**KPI Cards (Revenue, YoY Growth %, On-Time Delivery %)**
Questions we considered:
**Sales & Orders Performance Dashboard
Why**:
-	Are sales increasing or declining?
-	Which products drive revenue?
-	What markets and customer regions perform best?
-	Which employees generate the most sales?
Started by creating four KPI cards:
1.	Total Sales
2.	Total orders
3.	Avg Order Value
4.	Order Growth % YoY
-	prioritize investments (sales force, logistics, inventory).
- Alerts leadership early to shifts in revenue, customer satisfaction, or operational performance.

# How the Company Uses It
- Sales managers monitor monthly performance and coach sales reps.
- Marketing identifies high-value customer segments.
-	Leadership aligns promotions, pricing, and product strategy with performance trends.
-	Logistics teams identify which shippers and products cause delays.
-	Operations managers adjust staffing, scheduling, and warehouse processes.
-	Supply chain teams prevent stockouts and reduce excess inventory, improving profitability.
# Why These Dashboards Matter
-	Integrated insights connect sales, customer experience, and operations.
-	Faster decision-making through automated reporting.
-	Improved performance by surfacing problems early, before they affect revenue.
-	Better forecasting by visualizing trends across departments.


  
