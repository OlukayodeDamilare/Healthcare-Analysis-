# Healthcare Analysis 
Interactive Power BI dashboard analyzing hospital network revenue, billing, and patient demographics across 55,500 admissions surfacing cost drivers, payer mix, and operational risk indicators to support healthcare decision making.


# Healthcare Analysis Dashboard

## Executive Summary
This project analyzes hospital network performance across revenue, billing, patient demographics, and admission patterns to uncover cost drivers, utilization trends, and operational insights. Using Power BI, the analysis transforms raw hospital and billing data into an interactive two page dashboard (Financials & Patients) that supports data driven healthcare management decisions.

## Business Context
Hospital networks and healthcare administrators rely on analytics to understand where revenue is generated, which conditions drive the highest cost of care, and how patient demographics and admission patterns affect operations. This project simulates a real world healthcare analytics scenario across a 10 hospital network to evaluate financial performance and patient population trends.

## Objectives
The analysis aims to:
- Track total revenue, billing per patient, and year over year growth
- Identify top performing hospitals and revenue-driving medical conditions
- Analyze revenue by admission type and insurance provider
- Understand patient demographics like age, gender, blood type, and condition mix
- Monitor operational indicators like emergency admission rate, abnormal test rate, and length of stay
- Support better staffing, capacity planning, and payer strategy

## Key Business Questions
- What is total revenue, and how has it grown year-over-year?
- Which hospitals and medical conditions generate the most revenue?
- How does revenue break down by admission type and insurance provider?
- What do patient demographics (age, gender, blood type) look like across the network?
- What are the key operational risk indicators like emergency rate, abnormal test rate, length of stay?

## Dataset Overview
*Source:* Hospital admissions and billing dataset (Excel / CSV format)
[HOSPITAL ANALYSIS DATASETS.xlsx](https://github.com/user-attachments/files/30789812/HOSPITAL.ANALYSIS.DATASETS.xlsx)

*Records:* 55,500 patient admissions across 10 hospitals

*Key Fields:*
- Patient ID
- Hospital
- Admission Date
- Admission Type (Elective / Urgent / Emergency)
- Medical Condition
- Age Group
- Gender
- Blood Type
- Billing Amount
- Insurance Provider
- Test Results

> *Note on data:* This dataset is synthetic/simulated for portfolio purposes only. No real patient, hospital, or billing records were used or exposed.

## Tools & Technologies
- *Power BI*: dashboard design and interactivity
- *Data modeling*:  relational structure connecting patients, hospitals, and billing tables
- *DAX measures & calculated columns*:  for YoY billing comparisons and KPI logic
- *Power Query*:  data cleaning and transformation
  - Data type validation and formatting
  - Removing duplicates and handling nulls

## Data Preparation & Modeling
- Cleaned and standardized raw admissions/billing data using Power Query
- Created a Date table to support monthly and YoY trend analysis
- Built a relational data model to:
  - Connect patient, hospital, condition, and insurance data accurately
  - Avoid duplication across the 55,500-record dataset
  - Support DAX driven YoY and share-of-total calculations

## Power BI Concepts Applied
- DAX measures and calculated columns
- Calendar (Date) table
- KPI cards with trend sparklines
- Page-level navigation (Patients / Financials toggle)
- Year and Age Group slicers
- Comparative visuals (bar, line, donut)

## Skills Demonstrated
- Data cleaning & transformation (Power Query)
- Relational data modeling
- DAX (measures, calculated columns, YoY/share of total logic)
- KPI design and dashboard storytelling
- Multi-page dashboard navigation & UX
- Insight generation and business recommendation writing

## Key Metrics
| Metric | Value |
|---|---|
| Total Revenue | $1,417,432,043 |
| Total Admissions | 55,500 |
| Avg Billing per Patient | $25,539 (max $52,764) |
| Billing YoY Growth | +22.98% ($1.42B vs $1.15B PY) |
| Top Hospital Revenue Share | 36.76% — $521M |
| Emergency Admission Rate |33% (18,269 of 55,500) |
| Abnormal Test Rate | 55% (30,525 of 55,500) |
| Average Length of Stay | 16 days (max 30) |

## Dashboard Preview
Below are snapshots of the interactive Power BI dashboard:

*Financials View*
<img width="1546" height="880" alt="Financial Page Dashboard Image" src="https://github.com/user-attachments/assets/9a577400-cfb2-46c3-9220-997128f26593" />


*Patients View*
<img width="1542" height="882" alt="Patients Distribution Dashboard Image" src="https://github.com/user-attachments/assets/d7cc7c83-e639-44cc-ad5d-45c74b984357" />


## Key Insights
- The network generated *$1.42B in total revenue* across 55,500 admissions, up *22.98%* year-over-year.
- *Chronic conditions dominate revenue* :  Hypertension, Diabetes, and Obesity together account for roughly *74%* of total revenue.
- *Medicare is the dominant payer*, covering $707M : more than the next three insurers combined.
- *1 in 3 admissions is an emergency, and **55% of patients recorded an abnormal test result*  two operational signals worth monitoring closely.

## Key Findings
*Financial Performance:*
- Johns Hopkins Hospital led hospital level revenue at $288M, nearly double the next hospital (UCLA Medical Center, $176M)
- A steep drop-off exists between the top 2 hospitals and the remaining 5 (each in the $59M–$64M range)  indicating concentrated revenue in a small number of facilities
- Revenue by month follows a seasonal pattern: a sharp February dip, a mid-year peak (Jul–Aug), and a smaller October bump

*Condition-Level Cost Drivers:*
- Hypertension and Diabetes are tied as the top revenue-generating conditions at $0.35bn each
- Obesity follows closely at $0.33bn
- Cancer and Arthritis generate significantly less ($0.14bn each) despite being higher-acuity conditions suggesting volume, not severity, is the primary revenue driver

*Patient Population:*
- Diabetes and Hypertension are also the most common conditions by patient count (14K each), consistent with their revenue lead
- O+ is by far the most common blood type (13.9K patients), nearly double O (8.3K)
- The 70+ age group has the highest patient count (13K), followed closely by 55–69, 40–54, and 25–39 all clustered around 12K

*Operational Risk Indicators:*
- 1 in 3 admissions (33%) come through Emergency : a meaningful share to plan staffing and capacity around
- 55% of patients recorded an abnormal test result, a notably high rate worth flagging for quality of care review
- Average length of stay is 16 days, with some patients staying as long as 30 a potential driver of the high average billing per patient ($25,539)

## Recommendations
- Launch proactive chronic-disease management programs targeting Hypertension, Diabetes, and Obesity the 74% revenue concentration means small efficiency gains here have outsized financial and clinical impact
- Audit the 55% abnormal test rate against testing protocol and data entry practices to rule out a data-quality issue before treating it as a clinical trend
- Pre-allocate staffing and bed capacity ahead of the recurring Jul–Aug and October demand peaks
- Negotiate or review Medicare billing terms given it represents 50% of network revenue  even small rate changes have network wide impact
- Benchmark the 16-day average length of stay against clinical standards and flag outlier cases for discharge planning review

## Assumptions & Limitations
- Data reflects a simulated/sample healthcare scenario and may not reflect real patient or hospital figures
- Analysis does not include clinical outcomes, readmission rates, or staffing/cost data
- External factors (regional health trends, policy changes, insurance shifts) are inferred from patterns, not directly measured

## Future Improvements
With access to more data, this analysis could be extended by:
- Linking billing data to clinical outcomes and readmission rates
- Adding cost-per-admission and margin analysis by condition and hospital
- Incorporating staffing and capacity data to correlate with length of stay
- Building predictive models to flag high-risk (abnormal test, long-stay) patients earlier

## Call to Action
Feedback and suggestions are welcome. I'm continuously improving my data analytics and dashboard design skills and I'm open to collaboration or discussion.

---
## Author
*Olukayode Oluwadamilare*
[http://linkedin.com/in/olukayode-oluwadamilare-698b53337(#) •
