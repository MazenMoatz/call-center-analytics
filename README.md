# 📞 Call Center Performance & Operations Analytics
> An end-to-end Power BI dashboard analyzing 600K+ support tickets across agent performance, channel efficiency, customer experience, and SLA compliance.

---

## 📊 Dashboard Pages

### 1. Executive Summary
High-level overview of the call center's overall health.
- **600K** Total Tickets | **35.87%** FCR Rate | **3.95** Avg CSAT | **7.11** Avg NPS | **31.65%** SLA Breach Rate
- CSAT breakdown by channel
- SLA Breach Rate by team
- Ticket Volume Trend (monthly)
- NPS Trend over time (2021–2026)

![Executive Summary](Executive%20Summary.png)

---

### 2. Agent Performance
Individual agent-level analysis to identify top performers and bottlenecks.
- **11.43 min** Avg AHT | **0.22** Escalation Rate | **16.63 min** Avg Wait Time
- Top 10 Agents by AHT
- Top 10 Agents by Resolved Tickets
- Detailed table: Avg AHT, Avg CSAT, Escalation Rate, Resolved Tickets per agent
- Filters: Seniority, Team Name, Year

![Agent Performance](Agent%20Performance.png)

---

### 3. Channel & Cost
Cost efficiency and ticket distribution across all support channels.
- **$1.06M** Total Cost | **$1.76** Avg Cost Per Contact | **35.87%** FCR Rate | **600K** Total Tickets
- Total Cost by Channel (Phone dominates at $0.58M)
- FCR Rate by Channel
- Avg CSAT by Channel
- Total Tickets by Channel
- Filters: Channel Name, Year

![Channel & Cost](Channel%20%26%20Cost.png)

---

### 4. Customer Experience
Customer satisfaction, loyalty, and churn insights.
- **15.14%** Churn Rate | **$24.59K** Avg LTV | **7.11** Avg NPS | **25.42** Avg Tickets Per Customer
- LTV by Segment (SMB, Consumer, Enterprise, VIP)
- Customer Churn Rate donut chart
- Total Tickets by Region (Hurghada, Cairo, New York, etc.)
- Avg NPS by Tier (Bronze, Platinum, Gold, Silver)
- Filters: Tier, Year, Region

![Customer Experience](Customer%20Experience.png)

---

### 5. Operations & SLA
Operational efficiency and SLA compliance breakdown.
- **31.65%** SLA Breach Rate | **5.93** Avg Resolution Time | **16.63 min** Avg Wait Time | **12.01%** Reopen Rate
- Avg Resolution Time by Category (Complaint highest at 9.4)
- Tickets by Hour of Day (peak at 10–11 AM)
- SLA Breach by Team (Fraud & Security highest at 78.23%)
- Filters: Team Name, Category, Year

![Operations & SLA](Operations%20%26%20SLA.png)

---

## 🛠️ Tools & Technologies

| Tool | Usage |
|------|-------|
| Power BI Desktop | Dashboard development & visualization |
| Power Query (M) | Data transformation & cleaning |
| DAX | KPI calculations & measures |
| Microsoft Excel | Data source |

---

## 💡 Key Insights

- **Phone** is the most expensive channel ($0.58M) but also handles the highest ticket volume (210K)
- **Fraud & Security** team has the highest SLA breach rate at **78.23%** — critical area for improvement
- **WhatsApp** leads in both Avg CSAT (3.955) and FCR Rate (36.10%) — most efficient channel
- Ticket volume **peaks between 10–11 AM** — staffing should be optimized around this window
- **Churn rate of 15.14%** with NPS of 7.11 suggests moderate customer loyalty with room for improvement

---

## 📁 Repository Structure

```
call-center-analytics/
├── README.md
├── screenshots/
│   ├── Executive_Summary.png
│   ├── Agent_Performance.png
│   ├── Channel___Cost.png
│   ├── Customer_Experience.png
│   └── Operations___SLA.png
└── data/
    └── sample_data.xlsx        # Sample/anonymized dataset
```

---

## 👤 Author

**Hashem** — Data Analyst & BI Developer  
Business Information Systems, Galala University

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://linkedin.com/in/YOUR_LINKEDIN)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?logo=github)](https://github.com/MazenMoatz)
