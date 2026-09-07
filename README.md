# Pharma-Sales-
This is my first Git Repository.
<br>
Author- Vishal Ram

Pharma Sales Dashboard – Project Documentation 
Client: XYZ Pharmaceutical
Prepared by: Vishal Ram
Date: June 2026


##1. Project Overview
The Pharma Sales Dashboard project was developed for XYZ Pharmaceutical to provide a comprehensive view of sales performance, inventory management, supplier efficiency, and expiry risk monitoring. The goal was to deliver actionable insights that help improve operational efficiency, revenue growth, and decision-making.

##2. Problem Statement
Cipla faced challenges with disconnected data across sales, inventory, and supplier systems. There was no unified view to track real-time stock levels, revenue planning, or product expiry. Manual reporting led to delays, errors, and missed opportunities to optimize stock and improve supplier performance.

##3. Project Objectives
- Build a centralized Pharma Sales Dashboard using Power BI.
- Track stock availability, revenue planning, and sales agent performance.
- Proactively monitor drug expiry.
- Optimize supplier performance tracking.
- Deliver self-service analytics with dynamic filters and drill-downs.
- 
##4. Data Sources
- Sales Transactions (Sales Agent.xlsx)
- Product Master (LinkedDrugs.xlsx)
- Manufacturers (LinkedManufacturers.xlsx)
- Inventory (Inventory.xlsx)
- Supplier Details (Supplier.xlsx)
- Custom Date Table for time-based analysis
  
##5. Data Model Design
• Fact Table: Sales Agent (sales transactions)
• Dimension Tables:
  - LinkedDrugs (product info)
  - LinkedManufacturers (manufacturer details)
  - Inventory (stock levels)
  - Supplier (supplier performance)
  - Date Table (time intelligence)

Relationships:
- Sales ↔ LinkedDrugs (via DrugID)
- LinkedDrugs ↔ LinkedManufacturers (via ManufacturerID)
- Inventory ↔ LinkedDrugs (via DrugID)
- Inventory ↔ Supplier (via SupplierID)
- Sales ↔ Date Table (via SaleDate)
  
##6. Key DAX Measures
• Stock Available = [Total Stock] - [Sold Stock] - [Returned Units]
This metric tracks how much stock is currently available for sale after accounting for sales and returns.

• Revenue Planning = Stock Available * Unit Price
This measure estimates potential future revenue based on the current available stock and unit price.

• Total Sales = SUM('Sales Agent'[Total Sales])
• Gross Profit = Total Sales - SUMX('Sales Agent', UnitsSold * CostPerUnit)
• Net Sales = Total Sales - (Returned Units * Average Unit Price)
• Profit Margin % = Gross Profit / Total Sales
• On-Time Delivery Rate = Average of Supplier’s delivery rate
• Sales by Agent = Aggregates sales performance by individual sales agents, helping track top performers.

##7. Dashboard Design & Insights
• Sales Overview: KPIs for Total Sales, Gross Profit, Net Sales, Revenue Planning, and Returned Units.
• Inventory Snapshot: Tracks Stock Available, Total Stock, Sold Stock, and highlights drugs close to expiry.
• Sales Agent Performance: Sales by agent with regional breakdown, showing contribution to total revenue.
• Supplier Performance: On-time delivery rates and preferred supplier analysis.
• Drug Shelf Life: Lists drugs nearing expiry in 12/18/24 months along with their stock and revenue risk.

##8. Achievements in the Project
• Reduced manual reporting time by 90% by automating dashboards in Power BI.
• Provided real-time visibility into stock levels, leading to a 15% reduction in stockouts.
• Improved revenue recovery by identifying $418K worth of expiring stock for clearance.
• Enhanced supplier accountability with on-time delivery monitoring.
• Delivered a scalable, user-friendly dashboard with drill-through analysis for management.
Usually excel is refreshed every month. Monthly they use to monitor.
After Power BI , client is monitoring every.
• Empowered sales managers with Sales Agent performance data, improving productivity and sales strategies.

##How "Reduced Manual Reporting Time by 90%" Was Achieved:
 Before Power BI (Manual Process):
•	Reports were generated manually using Excel, emails, and CSV files.
•	Data from different sources (Sales, Inventory, Supplier, Product Master) had to be:
o	Downloaded or requested manually.
o	Cleaned (removing extra headers, fixing dates, correcting mismatched entries).
o	Manually merged using VLOOKUPs, Pivot Tables, and Formulas in Excel.
•	Every month or week:
o	Users spent 5–8 hours per report cycle creating sales reports, inventory summaries, supplier performance reports, and stock expiry reports.
•	Any update (e.g., new sales data) required redoing this entire process.
•	THEY ARE ABLE TO SEE THE MONTHLY DATA/monthly update
________________________________________

##After Power BI Automation:
•	Connected Power BI directly to:
o	Excel files / SharePoint / Databases (if any).
•	Applied all data cleaning steps in Power Query:
o	Automated removal of errors, junk rows, formatting, column renaming.
•	Data Modeling connected Sales, Inventory, Suppliers, and Products using relationships (no VLOOKUP needed anymore).
•	Created DAX Measures that calculate KPIs dynamically.
•	Built interactive dashboards that:
o	Auto-refresh when data is updated.
o	Allow users to filter by Region, Product, Sales Agent, etc., without manual intervention.
•	Instead of 8 hours, reports now take 10–15 minutes to refresh and distribute.
•	EVERY DAY THEY ARE ABLE TO SEE UPDATED REPORT/ daily update

##9. Challenges and Solutions
• Challenge: Incorrect totals in matrix reports.
  Solution: Applied SUMX functions for accurate aggregation.

• Challenge: Return handling affecting revenue calculations.
  Solution: Built Net Sales DAX measure that subtracts returned units from total sales.

• Challenge: No expiry tracking mechanism.
  Solution: Implemented expiry calculation using DATEDIFF and conditional measures.

• Challenge: Complex sales trends analysis.
  Solution: Integrated a custom Date table with Year, Quarter, and Month hierarchy.
  
##10. Conclusion
The Pharma Sales Dashboard for XYZ Pharmaceutical delivered key operational improvements by providing a single source of truth for sales, inventory, supplier, and expiry management. The solution empowered business stakeholders with data-driven decision-making, optimized sales strategies, and improved overall supply chain efficiency.


 

