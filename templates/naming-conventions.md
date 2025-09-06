# Column Naming Conventions Guide

## Before (Human-Focused) → After (AI-Ready)

### Basic Improvements
- ID → Customer Identifier (from CRM)
- Amt → Order Total Amount (USD)
- Qty → Quantity Ordered (Units)
- Dt → Order Date (Timestamp)
- Flag → Premium Customer (Yes/No)

### Context-Rich Examples
- Revenue → Monthly Recurring Revenue (USD, Excluding Discounts)
- Status → Order Status (Completed / Pending / Cancelled)
- Score → Customer Satisfaction Score (1–10 Scale)
- Rate → Conversion Rate (% Leads to Customers)

### Relationship-Aware Naming
- Customer Table → Customers (Master Records from Salesforce CRM)
- Orders → Sales Orders (Completed Transactions, Excluding Returns)
- Products → Product Catalog (Active Items with Pricing)

---

## Agent-Ready Model Template

### Tables
- Customers (Master Records from CRM)
- Sales Orders (Completed Transactions)
- Product Catalog (Active Items)
- Calendar (Date Dimension with Business Periods)

### Key Measures
- Total Revenue (USD, Current Month)
- Customer Acquisition Cost (USD, Marketing-Attributed)
- Average Order Value (USD, Excluding Returns)
- Customer Lifetime Value (Predicted, 36 Months)

### Relationships
- All relationships named with business context  
- Bridge tables clearly identified  
- Many-to-many relationships documented  

---

## Naming Principles
- **Use Full Words:** Avoid abbreviations that AI or business users might misinterpret  
- **Include Context:** Add data source, time period, or business rules in parentheses  
- **Specify Units:** Always indicate currency, measurements, or scales  
- **Be Descriptive:** Purpose and scope should be clear and business-readable  
- **Consider Relationships:** Reflect how tables connect in business terms  

**Career Insight:** Clear, AI-ready names are not cosmetic — they are the foundation of trust in Copilot and conversational analytics.
