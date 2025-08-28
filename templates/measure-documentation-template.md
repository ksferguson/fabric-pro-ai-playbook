# Measure Documentation Template

## DAX Measure Example

```dax
// BUSINESS CONTEXT: Revenue from completed subscription orders only
// CALCULATION LOGIC: Sum net amounts minus discounts and returns for current quarter
// EXCLUSIONS: One-time purchases, pending orders, cancelled subscriptions
// USAGE: Executive reporting, growth analysis, forecasting models
// DEPENDENCIES: Orders table, Customer table relationships
// UPDATED: Daily at 6 AM CT via automated ETL pipeline
QuarterlyRecurringRevenue_ExcludingReturns_USD = 
CALCULATE(
    SUM(Orders[NetAmount]) - SUM(Orders[Discounts]) - SUM(Orders[Returns]),
    Orders[OrderType] = "Subscription",
    Orders[Status] = "Completed", 
    Orders[OrderDate] >= STARTOFQUARTER(TODAY())
)
```

## Power BI Properties Panel Template

```
Display Name: Quarterly Recurring Revenue (Excl. Returns)
Description: Subscription revenue for current quarter, excluding discounts, returns, and pending orders. Business Rule: Only completed subscription transactions included. Used for: Growth analysis, executive reporting, financial forecasting. Updated: Daily at 6AM CT via automated ETL pipeline.
Display Folder: Revenue\Recurring\Quarterly
Format: Currency (USD)
```

## Documentation Checklist
- [ ] Business context clearly explained
- [ ] Calculation logic documented
- [ ] Exclusions and limitations noted
- [ ] Usage scenarios identified
- [ ] Dependencies mapped
- [ ] Update schedule specified
- [ ] Display name is business-friendly
- [ ] Description includes all key details