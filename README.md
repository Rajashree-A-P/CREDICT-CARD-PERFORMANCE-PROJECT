# 💳 Credit Card Customer & Transaction Analysis | Power BI Project

# 📌 About The Project
This project analyzes credit card customer behavior, transaction trends, revenue performance, and risk indicators using Power BI.

The dashboard helps understand:
- Customer spending patterns
- Revenue contribution
- Transaction behavior
- Delinquency risk
- Customer segmentation
- Weekly business performance

The goal of this project is to convert raw financial data into meaningful business insights that support smarter decision-making and business growth.

---

# 🚀 Project Highlights
✅ Interactive Power BI Dashboard  
✅ Customer Segmentation Analysis  
✅ Revenue & Transaction Insights  
✅ Weekly Performance Tracking  
✅ Risk & Delinquency Analysis  
✅ Spending Behavior Analysis  
✅ KPI Monitoring Dashboard  

---

# 🛠️ Tools Used
- Power BI
- Power Query
- DAX
- Excel / CSV Dataset

---

# 📊 Key KPIs
| KPI | Value |
|---|---|
| 💰 Total Revenue | $55M |
| 💳 Total Transaction Amount | $45M |
| 📈 Interest Earned | $7.84M |
| 🔄 Transaction Count | 10.1K |

---

# 📈 Key Insights

# 👥 Customer Segment Analysis
- Self-employed customers contribute the highest share of accounts.
- Businessmen and white-collar professionals are strong revenue contributors.
- Retirees contribute the least, showing a growth opportunity.

# Insight:
High-income and working professionals are the primary drivers of revenue.

---

# 💳 Transaction Insights
- Swipe transactions are the most preferred payment method.
- Online transactions are comparatively lower.
- Bills, entertainment, fuel, and grocery categories generate the highest spending.

# Insight:
Digital transaction adoption can be improved through targeted campaigns.

---

# 📉 Revenue & Weekly Trends
- Revenue shows fluctuations across different weeks.
- Strong growth observed during Week 11 and Week 31.
- Some weeks showed negative growth trends.

# Insight:
Business performance is stable overall but requires revenue stabilization strategies during low-performing periods.

---

# ⚠️ Risk Analysis
- 93.93% accounts are non-delinquent.
- Only 6.07% accounts are delinquent.

# Insight:
The business maintains strong credit quality and effective risk management.

---

# 👨‍👩‍👧 Customer Behavior Insights
- Customers aged 30–50 generate the highest revenue.
- High-income customers contribute maximum business value.
- Married customers spend more compared to single customers.
- Revenue is highest in:
  - Texas
  - New York
  - California

---

# 📌 DAX Measures Used

```DAX
CURRENT WEEK REVENUE =
CALCULATE(
    SUM(credit card[Revenue]),
    FILTER(
        ALL('credit card'),
        credit card[WEEK NUMBER] =
        MAX(credit card[WEEK NUMBER])
    )
)

PREVIOUS WEEK REVENUE =
CALCULATE(
    SUM(credit card[Revenue]),
    FILTER(
        ALL('credit card'),
        credit card[WEEK NUMBER] =
        MAX(credit card[WEEK NUMBER]) - 1
    )
)

WEEK_OVER_WEEK REVENUE =
DIVIDE(
    ([CURRENT WEEK REVENUE] -
    [PREVIOUS WEEK REVENUE]),
    [PREVIOUS WEEK REVENUE]
)
