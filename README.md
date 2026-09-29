# Week 3 Data Modeling & DAX Practice

## Project Overview
Built a star schema data model in Power BI and wrote DAX measures for the Sales dataset.

## Data Model
- **Fact Table:** Sales (OrderID, OrderDate, CustomerID, ProductID, Quantity, Amount)
- **Dimension Tables:** Products, Customers, Dates
- **Relationships:** 3 (Sales ↔ Products, Sales ↔ Customers, Sales ↔ Dates)
- **Date Table:** Marked as official calendar

## DAX Measures Written
| Measure | Formula |
|---------|---------|
| Total Sales | SUM(Sales[Amount]) |
| Average Order Value | AVERAGE(Sales[Amount]) |
| Order Count | COUNT(Sales[OrderID]) |
| Max Sale | MAX(Sales[Amount]) |
| Total Sales YTD | TOTALYTD(SUM(Sales[Amount]), Dates[Date]) |
| North Region Sales | CALCULATE(SUM(Sales[Amount]), Customer[Region]="North") |

## Testing
- Added Region slicer
- Tested each measure
- Confirmed all measures respond correctly to filter context

## Screenshot
![Data Model](week3_datamodel_screenshot.png)

## How to Use
1. Download the .pbix file
2. Open in Power BI Desktop
3. Explore the data model and measures
