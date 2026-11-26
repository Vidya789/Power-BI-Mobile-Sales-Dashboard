**Mobile Sales Dashboard**

I built this Power BI dashboard to explore mobile sales and make the main figures easy to understand. It lets you look at sales and units sold from different angles, using interactive filters.

**What the dashboard shows**

+ Total sales, quantity sold, transaction count, and average

+ Monthly quantity sold

+ Sales by mobile model and payment method

+ A city sales map

+ Sales and quantity by brand

+ Customer ratings and sales by day of the week

+ Filters for month, mobile model, payment method, brand, and day name

**Project tools**

+ Power BI

+ Power Query

+ DAX

**Key figures**

Total sales: approximately 769.2M

+ Units sold: 19,150

+ Source rows: 3,835

I checked the monthly quantity chart against the overall quantity: the twelve monthly values add up to 19,150 units.

**DAX measures**

These measures use the Sales_Data table.

**Sales Check**

Calculates sales as units sold multiplied by price per unit.

Sales Check =
SUMX(
    'Sales_Data',
    'Sales_Data'[Units Sold] * 'Sales_Data'[Price Per Unit]
)

**Qty Check**

Adds the units sold.

Qty Check =
SUM('Sales_Data'[Units Sold])

**Row Count**

Counts the rows in the data.

Row Count =
COUNTROWS('Sales_Data')

**Transactions**

Counts unique transaction IDs.

Transactions =
DISTINCTCOUNT('Sales_Data'[Transaction ID])

**Files**

Mobile_Sales_Dashboard.pbix — the Power BI report

dashboard.png — a screenshot preview of the dashboard

This is a learning project built to practise data preparation, DAX, and dashboard design.
