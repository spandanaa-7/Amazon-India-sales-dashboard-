# Amazon India Sales Dashboard

## Project Overview

This project analyzes Amazon India sales data using Microsoft Power BI. The dashboard provides insights into sales performance, profitability, order status, payment methods, fulfilment methods, and geographical performance.

## Tools Used

- Microsoft Power BI
- Microsoft Excel
- DAX (Data Analysis Expressions)

## Dataset

- Total Records: 10,000
- Total Columns: 13
- Dataset: Amazon Sales Data India

## Dashboard Pages

### 1. Sales Overview

- Total Sales
- Total Profit
- Total Orders
- Total Units Sold
- Average Order Value
- Profit Margin
- Monthly Sales and Profit Trends
- Category-wise Sales and Profit
- Top 10 Products by Sales

### 2. Order and Returns Analysis

- Order Status Distribution
- Return Rate
- Cancellation Rate
- Category-wise Returns and Cancellations

### 3. Payment and Fulfilment Performance

- Sales and Profit by Payment Method
- Sales and Profit by Fulfilment Method

### 4. Geographical Performance

- State-wise Sales
- State-wise Profit
- State-wise Orders

## Key Performance Indicators

| KPI | Result |
|---|---:|
| Total Sales | ₹155.79 Million |
| Total Profit | ₹33.17 Million |
| Total Orders | 10,000 |
| Total Units Sold | 25,000 |
| Profit Margin | 21.29% |
| Return Rate | 4.85% |
| Cancellation Rate | 5.00% |

## DAX Measures

```dax
Total Sales = SUM('Sheet1'[Total_Sales_INR])

Total Profit = SUM('Sheet1'[Profit_INR])

Total Orders = DISTINCTCOUNT('Sheet1'[Order_ID])

Total Units Sold = SUM('Sheet1'[Quantity])

Average Order Value = DIVIDE([Total Sales], [Total Orders], 0)

Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0)

Return Rate % =
DIVIDE(
    CALCULATE([Total Orders], 'Sheet1'[Order_Status] = "Returned"),
    [Total Orders],
    0
)

Cancellation Rate % =
DIVIDE(
    CALCULATE([Total Orders], 'Sheet1'[Order_Status] = "Cancelled"),
    [Total Orders],
    0
)
```

## Project Files

- `data/` – Original sales dataset
- `dashboard/` – Power BI dashboard file
- `screenshots/` – Dashboard screenshots and PDF export

## Conclusion

This project helped me understand retail sales data, create meaningful KPIs, analyze business performance, and build an interactive dashboard using Power BI.
