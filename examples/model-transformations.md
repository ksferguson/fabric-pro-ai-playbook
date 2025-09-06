# AI-Ready Model Transformations Playbook

## Naming Conventions Guide
To ensure data models are business-friendly and AI-readable, apply these rules consistently:

1. **Title Case with Spaces** – avoid snake_case or camelCase  
   *Good:* `Total Revenue (USD)`  
   *Avoid:* `total_revenue_usd`

2. **Units in Parentheses** – always include currency, percentages, or timeframes  
   *Example:* `Average Order Value (USD)`

3. **Inclusions/Exclusions in Parentheses** – capture business logic clearly  
   *Example:* `Monthly Recurring Revenue (USD, Excluding Discounts & Returns)`

4. **Short, Descriptive, Unambiguous Names** – optimize for business readability and AI clarity  
   *Example:* `Active Customers (Purchased within 90 Days)`

5. **Consistency Across Models** – apply the same structure everywhere so Copilot learns your vocabulary.

---

## Sales Analysis Example

### Before: Traditional Semantic Model
**Tables**
- Customers
- Orders
- Products
- Dates

**Measures**
- Revenue
- Avg Order
- Customer Count

**Relationships**
- Basic foreign key joins

**Documentation**
- Minimal, technical focus

**Agent Query:** *"What's our revenue growth this quarter?"*  
**Response:**  
```
"I found revenue data but I'm not sure which revenue measure to use or what time period constitutes 'this quarter' in your business context."
```

---

### After: AI-Ready Semantic Model
**Tables**
- Customers (Master Records from Salesforce CRM)  
- Sales Orders (Completed, Excluding Returns)  
- Product Catalog (Active Items with Current Pricing)  
- Calendar (Business Periods)

**Measures**
- Monthly Recurring Revenue (USD, Excluding Discounts & Returns)  
- Average Order Value (USD, Completed Transactions)  
- Active Customers (Purchased within 90 Days)  
- Customer Acquisition Cost (USD, Marketing-Attributed)

**Relationships**
- Named, documented, and business-friendly

**Documentation**
- Rich business context, usage scenarios, update schedules

**Agent Query:** *"What's our revenue growth this quarter?"*  
**Response:**  
```
"Monthly Recurring Revenue for Q4 2025 is $2.3M, representing 15% growth compared to Q3 2025 ($2.0M) and 23% growth year-over-year (Q4 2024: $1.87M). Growth is driven primarily by new customer acquisitions in the Enterprise segment."
```

---

## Key Design Principles
- **Descriptive Names:** short, business-friendly, unambiguous  
- **Business Context:** include exclusions/inclusions in parentheses  
- **Consistency:** apply the same conventions across all models  
- **Rich Metadata:** descriptions, synonyms, update schedules  
- **Verified Answers:** lock in consistent results for common queries  

**Career Insight:** Designing AI-ready data models is your new core skill — you are becoming a **Data–AI Translator**.

---

## E-commerce Example

### Before: Generic Model
**Tables**
- Users, Orders, Products, Sessions

**Measures**
- Sales, Visitors, Conversion

---

### After: AI-Ready Model
**Tables**
- Website Users (Registered with Purchase History)  
- E-commerce Orders (Completed with Shipping Details)  
- Product Inventory (Active with Pricing Tiers)  
- Web Sessions (Tracked with Attribution Data)

**Measures**
- Total Online Sales (USD, Completed Orders)  
- Unique Website Visitors (Excluding Bots)  
- E-commerce Conversion Rate (% Sessions to Orders)
