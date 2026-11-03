# Balanced Tree Clothing Co.: Retail Sales SQL Case Study

SQL analysis of a fashion retailer's sales and product hierarchy (category → segment → product), based on Case Study #7 of the [8 Week SQL Challenge](https://8weeksqlchallenge.com/case-study-7/).

## Questions answered
**Sales overview**: total quantity sold, revenue before discounts, total discount given.

**Transactions**
- Unique transactions and average distinct products per basket
- 25th / 50th / 75th percentile revenue per transaction (`PERCENTILE_CONT`)
- Average discount per transaction
- Member vs non-member split of transactions and revenue

**Products**
- Top 3 products by revenue
- Quantity, revenue and discount by segment and by category
- Best-selling product in each segment and each category (`ROW_NUMBER` per group)
- Revenue share of each product within its segment, of each segment within its category, and of each category in the total (window `SUM ... OVER (PARTITION BY ...)`)
- Transaction penetration for each product (share of baskets that contain it)
- Most common product combination in a basket

## SQL used
CTEs · window functions (`ROW_NUMBER`, `SUM() OVER`) · `PERCENTILE_CONT` · subqueries · joins · `STRING_AGG`

## Files
| File | What it is |
|---|---|
| `SQL Code.txt` | All queries, grouped by section |
| `8WEEKSSQLCHALLENGE.COM.pptx` | Findings deck |
