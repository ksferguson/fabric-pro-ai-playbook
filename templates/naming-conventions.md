# Column Naming Conventions Guide

## Before (Human-Focused) → After (AI-Ready)

### Basic Improvements
- `id` → `customer_unique_identifier_from_crm`
- `amt` → `order_total_amount_usd`
- `qty` → `quantity_ordered_units`
- `dt` → `order_date_timestamp`
- `flag` → `is_premium_customer_boolean`

### Context-Rich Examples
- `revenue` → `monthly_recurring_revenue_usd_excluding_discounts`
- `status` → `order_status_completed_pending_cancelled`
- `score` → `customer_satisfaction_score_1_to_10_scale`
- `rate` → `conversion_rate_percentage_leads_to_customers`

### Relationship-Aware Naming
- `customer_table` → `customers_master_records_from_salesforce_crm`
- `orders` → `sales_orders_completed_transactions_excluding_returns`
- `products` → `product_catalog_active_items_with_pricing`

## Agent-Ready Model Template

### Tables
- `customers_master_records_from_crm`
- `sales_orders_completed_transactions`
- `product_catalog_active_items`
- `calendar_date_dimension_table`

### Key Measures
- `total_revenue_current_month_usd`
- `customer_acquisition_cost_marketing_attributed`
- `average_order_value_excluding_returns_usd`
- `customer_lifetime_value_predicted_36_months`

### Relationships
- All relationships named with business context
- Bridge tables clearly identified
- Many-to-many relationships documented

## Naming Principles

1. **Use Full Words:** No abbreviations that AI might misinterpret
2. **Include Context:** Data source, time period, business rules
3. **Specify Units:** Currency, measurements, scales
4. **Be Descriptive:** Purpose and scope should be clear
5. **Consider Relationships:** How tables connect in business terms