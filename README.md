# 📊 Customer Service Performance & Complaint Analytics

> **A Power BI Business Analytics Dashboard for transforming customer support data into actionable business insights.**

![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=for-the-badge\&logo=powerbi\&logoColor=black)
![Excel](https://img.shields.io/badge/Excel-Data%20Source-217346?style=for-the-badge\&logo=microsoftexcel\&logoColor=white)
![Business Analysis](https://img.shields.io/badge/Business-Analysis-2563EB?style=for-the-badge)
![Data Analytics](https://img.shields.io/badge/Data-Analytics-7C3AED?style=for-the-badge)

---

## 📌 Project Overview

**Customer Service Performance & Complaint Analytics** is an interactive Power BI dashboard designed to analyze customer support operations and identify areas that require business attention.

The dashboard converts raw customer service data into meaningful KPIs, visual insights, and management-level analysis.

The project focuses on:

* 📞 Customer support performance
* ⏱️ Response and resolution times
* 🚨 SLA breach monitoring
* 😡 Complaint analysis
* ⭐ Customer satisfaction
* 👥 Customer segmentation
* 🏢 Department performance
* 📊 Operational trends

---

## 🎯 Business Problem

Customer service teams often deal with large amounts of support data, but raw data alone does not clearly show where operational problems are occurring.

Management needs answers to questions such as:

* How many customer tickets are being received?
* How quickly are customers receiving responses?
* How long does it take to resolve issues?
* Which departments have the highest workload?
* Where are SLA breaches occurring?
* What types of complaints are most common?
* Which customer groups generate the most tickets?
* How satisfied are customers?
* Which areas require operational improvement?

This dashboard was created to provide a **single analytical view** of these business questions.

---

## 💡 Project Objectives

The main objectives are to:

1. Monitor overall customer service performance.
2. Identify complaint patterns and major complaint categories.
3. Analyze response and resolution efficiency.
4. Track SLA compliance.
5. Understand customer satisfaction levels.
6. Compare department and priority performance.
7. Provide management with data-driven insights for decision-making.

---

## 📂 Dataset

The project uses a customer support dataset containing information about service tickets.

### Key Fields

| Field           | Description                        |
| --------------- | ---------------------------------- |
| Ticket ID       | Unique support ticket identifier   |
| Date            | Ticket creation date               |
| Customer Type   | Type of customer                   |
| Category        | Service category                   |
| Priority        | Ticket priority                    |
| Channel         | Customer contact channel           |
| Department      | Responsible department             |
| Assigned Staff  | Staff member handling the ticket   |
| Response Time   | Initial response time              |
| Resolution Time | Time taken to resolve ticket       |
| Status          | Ticket status                      |
| Customer Rating | Customer satisfaction rating       |
| Location        | Customer location                  |
| Complaint Type  | Type of complaint                  |
| SLA Target      | Target response/resolution time    |
| SLA Breach      | Indicates whether SLA was breached |

---

## 🔄 Data Preparation

The dataset was prepared before visualization using Power BI / Power Query.

### Data Cleaning Steps

* Removed duplicate Ticket IDs
* Removed blank records
* Trimmed unnecessary spaces from text fields
* Verified column data types
* Prepared date fields for analysis
* Validated numerical fields
* Prepared categorical fields for filtering and visualization

---

## 📊 Dashboard Pages

### 1️⃣ Executive Overview

Provides a high-level management view of customer service operations.

**Key KPIs:**

* Total Tickets
* Resolved Tickets
* Average Response Time
* Average Resolution Time
* SLA Breach %
* Average Customer Rating

**Visual Analysis:**

* Tickets by Category
* Tickets by Priority
* Tickets by Channel
* Ticket Status
* Interactive Date and operational filters

---

### 2️⃣ Complaint Analysis

Focuses on understanding customer complaints.

**Analysis includes:**

* Complaints by Location
* Complaint Types
* Complaints by Department
* Complaint volume by Priority
* Geographic complaint distribution

The purpose is to identify recurring complaint patterns and areas that may require further investigation.

---

### 3️⃣ Service Performance

Analyzes operational efficiency across departments.

**Key metrics:**

* Average Response Time
* Average Resolution Time
* SLA Breaches
* Department-level performance

This page helps identify differences in service performance between operational teams.

---

### 4️⃣ Customer Insights

Focuses on customer behavior and satisfaction.

**Analysis includes:**

* Tickets by Customer Type
* Customer Rating Distribution
* Channel-level customer activity
* Customer service patterns

---

## 🧮 Key DAX Measures

Example measures created for the dashboard:

```DAX
Total Tickets =
COUNTROWS('Support Tickets')
```

```DAX
Resolved Tickets =
CALCULATE(
    COUNTROWS('Support Tickets'),
    'Support Tickets'[Status] = "Resolved"
)
```

```DAX
Average Response Time =
AVERAGE('Support Tickets'[Response Time (Min)])
```

```DAX
Average Resolution Time =
AVERAGE('Support Tickets'[Resolution Time (Min)])
```

```DAX
SLA Breaches =
CALCULATE(
    COUNTROWS('Support Tickets'),
    'Support Tickets'[SLA Breach] = "Yes"
)
```

```DAX
SLA Breach % =
DIVIDE(
    [SLA Breaches],
    [Total Tickets],
    0
)
```

```DAX
Average Customer Rating =
AVERAGE('Support Tickets'[Customer Rating])
```

---

## 🔍 Business Analysis Approach

This project follows a practical **Business Analysis → Data Analysis → Decision Support** approach.

### Business Problem

⬇️
Customer service performance and complaint patterns are difficult to monitor using raw data.

### Data

⬇️
Customer support ticket records.

### Analysis

⬇️
KPIs, DAX measures, filtering, segmentation and visual analysis.

### Insights

⬇️
Identify performance gaps, complaint patterns and SLA issues.

### Business Decision

⬇️
Use the insights to support operational improvement and customer service decisions.

---

## 📈 Key Business Questions

The dashboard is designed to answer questions such as:

**Performance**

* Which departments handle the highest ticket volume?
* Where are response times high?
* Which areas have longer resolution times?

**SLA**

* How many tickets breached SLA?
* Which departments have more SLA breaches?
* Are SLA issues concentrated around certain priorities?

**Complaints**

* What are the most common complaint types?
* Which locations generate more complaints?
* Which departments receive more complaints?

**Customers**

* Which customer types generate the most tickets?
* What is the overall customer satisfaction level?
* Which service channels are used most frequently?

---

## 🛠️ Tools & Technologies

| Tool                   | Purpose                                   |
| ---------------------- | ----------------------------------------- |
| **Power BI**           | Dashboard development & visualization     |
| **Power Query**        | Data cleaning & transformation            |
| **DAX**                | KPI and analytical calculations           |
| **Microsoft Excel**    | Data source                               |
| **Data Visualization** | Business insight presentation             |
| **Business Analysis**  | Problem identification & decision support |

---

## 🎨 Dashboard Design

The dashboard was designed with a **management-oriented layout** focusing on:

* Clear KPI visibility
* Interactive filters
* Consistent visual hierarchy
* Easy comparison between departments
* Complaint and SLA monitoring
* Decision-oriented insights

The objective is not only to display data, but to make the information **easy for business stakeholders to understand and act upon**.

---

## 🚀 Future Improvements

Potential future enhancements include:

* Automated data refresh
* Real-time customer service monitoring
* Predictive complaint analysis
* Customer churn analysis
* Advanced customer segmentation
* AI-assisted insight generation
* Power BI Service deployment
* Automated management alerts

---

## 👩‍💻 Skills Demonstrated

This project demonstrates practical skills in:

**Business Analysis**

* Business problem identification
* Process-oriented thinking
* KPI identification
* Requirements understanding
* Data-driven decision support

**Data Analytics**

* Data cleaning
* Data transformation
* DAX
* KPI development
* Data visualization
* Dashboard design

**Power BI**

* Interactive dashboards
* Slicers
* Filters
* Cards
* Charts
* Maps
* Performance analysis

---

## 📁 Project Structure

```text
customer-service-performance-analytics/
│
├── 📊 Customer_Service_Performance_Analytics.xlsx
├── 📈 Customer_Service_Performance_Analytics.pbix
├── 🖼️ Dashboard-Screenshots/
│   ├── Executive-Overview.png
│   ├── Complaint-Analysis.png
│   ├── Service-Performance.png
│   └── Customer-Insights.png
│
└── 📄 README.md
```

---

## 👤 Author

**Lakmi Kumanayaka**

HNDIT | Business Analysis | Project Management | Data Analytics

Interested in using **business analysis, technology and data** to understand real-world business problems and develop practical solutions.

---

## ⭐ Project Purpose

This project was developed as a practical portfolio project to demonstrate how raw customer service data can be transformed into a structured analytical dashboard that supports **business understanding, performance monitoring and data-driven decision-making**.

**From Raw Data → Analysis → Insights → Business Decisions.**

---
