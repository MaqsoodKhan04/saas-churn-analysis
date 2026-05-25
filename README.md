# SaaS Customer Churn Analysis & Health Score Dashboard 

I built this project during my data analyst internship to understand 
why SaaS customers leave and to flag which ones are likely to leave 
before they actually do.

The idea came from a simple question — can we look at how a customer 
behaves and predict if they are going to cancel their subscription? 
Turns out, yes we can.

---

## What this project does

It takes raw customer data, builds a health score for each customer, 
segments them into risk tiers and visualises everything in a 
Power BI dashboard that a business team can actually use.

---

## Dataset

I used the IBM Telco Customer Churn dataset from Kaggle.
It has 7043 customers and 21 columns covering things like 
how long they have been a customer, what plan they are on, 
how they pay, and whether they eventually churned.

---

## Tools I used

- Python and Pandas for cleaning the data and building the scores
- Matplotlib for visualising the findings
- Excel for exporting clean tables
- Power BI for the final interactive dashboard

---

## How I built the health score

I gave each customer a score out of 100 based on 4 things:

- How long they have been a customer (30 points)
- How much they pay monthly (25 points)
- Whether they have tech support (20 points)
- Whether they have online security (25 points)

Then I put every customer into one of 3 buckets:

- Green (70 to 100) — healthy, likely to stay
- Yellow (40 to 69) — needs attention
- Red (0 to 39) — high risk, likely to leave

---

## What I found

The health score actually works. Green customers churn at 8.7%, 
Yellow at 16.3% and Red at 40.1%. That kind of separation tells 
me the scoring logic is picking up real signals.

A few other things stood out:

Month to month customers churn at 42.7% while two year contract 
customers churn at only 2.8%. That is a 15x difference just based 
on contract type.

Customers paying by electronic check churn at 45.3% compared to 
around 15% for people on automatic payments. Every month they 
manually pay is a moment they can decide to stop.

Fiber optic customers churn at 41.9% which surprised me at first. 
They are paying the most but leaving the most. I think the 
expectations are higher and the competition is stronger in 
fiber optic areas.

Customers who churned had an average tenure of 17.98 months. 
Customers who stayed averaged 37.57 months. So the first 
18 months seem to be the most critical window.

---

## Business recommendations I came up with

If I were presenting this to a business team I would say:

Push month to month customers toward annual plans with a small 
discount. Get electronic check users onto auto pay. Put extra 
effort into onboarding new customers in their first 6 months 
since that is when they are most likely to leave. And have the 
sales team prioritise calling Red tier customers before they churn.

---

## Dashboard

I built a 3 page Power BI dashboard:

Page 1 is an executive summary with the overall churn rate, 
total at risk customers and average monthly revenue.

Page 2 breaks down the health tiers with a donut chart, 
churn rate by tier and a table of all Red tier customers.

Page 3 is a deep dive into contract type, payment method, 
internet service and tenure — all filterable by health tier 
using a slicer.

---

## Project files

- saas_churn_analysis.ipynb — the full notebook
- saas_churn_analysis.xlsx — cleaned and scored data
- saas_churn_dashboard.pbix — Power BI dashboard file
- charts folder — all the visualisations I generated

---

## How to run it

Download the dataset from Kaggle (Telco Customer Churn), 
open the notebook in Jupyter and run the cells in order. 
The Excel file gets generated automatically. Then open 
the pbix file in Power BI Desktop.

---

## About me
Mohammed Maqsood Khan
Data Analyst Intern
maqsoodkhan34998@gmail.com
