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

## 🧮 DAX Measures (17 Measures)

| # | Measure | Formula |
|---|---------|---------|
| 1 | Total Tickets | `COUNTROWS(Fact_Tickets)` |
| 2 | FCR Rate | `DIVIDE(COUNTROWS(FILTER(Fact_Tickets, Fact_Tickets[is_fcr] = TRUE())), [Total Tickets])` |
| 3 | Avg CSAT | `AVERAGE(Fact_Tickets[csat_score])` |
| 4 | Avg NPS | `AVERAGE(Fact_Tickets[nps_score])` |
| 5 | SLA Breach Rate | `DIVIDE(COUNTROWS(FILTER(Fact_Tickets, Fact_Tickets[is_sla_breached] = TRUE())), [Total Tickets])` |
| 6 | Avg AHT | `AVERAGE(Fact_Tickets[handle_time])` |
| 7 | Avg Wait Time | `AVERAGE(Fact_Tickets[wait_time])` |
| 8 | Escalation Rate | `DIVIDE(COUNTROWS(FILTER(Fact_Tickets, Fact_Tickets[is_escalated] = TRUE())), [Total Tickets])` |
| 9 | Avg Resolution Time | `AVERAGE(Fact_Tickets[resolution_time])` |
| 10 | Reopen Rate | `DIVIDE(COUNTROWS(FILTER(Fact_Tickets, Fact_Tickets[is_reopened] = TRUE())), [Total Tickets])` |
| 11 | Total Cost | `SUM(Fact_Tickets[contact_cost])` |
| 12 | Avg Cost Per Contact | `DIVIDE([Total Cost], [Total Tickets])` |
| 13 | Avg LTV | `AVERAGE(Dim_Customer[lifetime_value])` |
| 14 | Churn Rate | `DIVIDE(COUNTROWS(FILTER(Dim_Customer, Dim_Customer[is_churned] = TRUE())), COUNTROWS(Dim_Customer))` |
| 15 | Avg Tickets Per Customer | `DIVIDE([Total Tickets], COUNTROWS(Dim_Customer))` |
| 16 | Resolved Tickets | `COUNTROWS(FILTER(Fact_Tickets, Fact_Tickets[status] = "Resolved"))` |
| 17 | Top Agent Resolved | `CALCULATE([Resolved Tickets], TOPN(10, Dim_Agent, [Resolved Tickets]))` |

---

## ❓ Business Questions Answered

**Agent Performance**
- Which agents have the highest Average Handle Time (AHT)?
- Which agents resolve the most tickets?
- How does escalation rate vary by agent seniority?

**Channel & Cost**
- Which support channel is most cost-effective per contact?
- Which channel delivers the best First Call Resolution (FCR) rate?
- Which channel has the highest CSAT score?
- What is the cost breakdown by support channel?
- Which channel handles the highest ticket volume?

**Customer Experience**
- How does customer churn vary by segment (SMB, Enterprise, VIP)?
- Which customer tier has the best NPS score?
- What is the average LTV per customer segment?
- Which region has the highest ticket volume?
- What is the average number of tickets per customer?

**Operations & SLA**
- Which teams are breaching SLA the most?
- Which team has the lowest SLA breach rate?
- What is the peak hour for incoming ticket volume?
- Which complaint category takes the longest to resolve?
- What percentage of tickets are reopened per category?

**Trends & Overview**
- How does ticket volume trend month over month?
- How does NPS change over time (2021–2026)?

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


[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://www.linkedin.com/in/mazen-moataz-098223349/)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?logo=github)](https://github.com/MazenMoatz)
[![Email](https://img.shields.io/badge/Email-Contact-red?logo=gmail)](mailto:mazenmotz@gmail.com)
