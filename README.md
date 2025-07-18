# uber-nyc-data-project
This end-to-end analytics project showcases a scalable data pipeline built on  Google Cloud Platform (GCP) using:  - Cloud Storage for raw CSV ingestion -  Mage AI  on  Compute Engine for ETL orchestration - BigQuery for analytics-ready warehouse design - Looker Studio for interactive BI dashboarding 

## Tools & Technologies

- **Google Cloud Storage** – raw data ingestion
- **Mage AI (ETL)** – transformation & orchestration
- **Google Compute Engine** – ETL execution environment
- **BigQuery** – data warehousing & analytics
- **Looker Studio** – business intelligence visualization
- **Python & SQL** – automation, querying, and pipeline logic

---

## Architecture Diagram

![Architecture](diagrams/architecture.jpg)

---

## Data Model (Star Schema)

The project follows a star schema structure with the `fact_table` at the center and several dimension tables including date, location, payment type, passenger count, distance, and rate codes.

![Data Model](diagrams/data_model.jpeg)

---

## Project Structure

uber-nyc-data-project/
├── ETL/
│ ├── extract.py # Pulls raw CSVs from GCS
│ ├── transform.py # Cleans and reshapes the data
│ ├── load.py # Loads cleaned tables into BigQuery
│ └── data_engineer_uber.py # Main ETL controller
├── analytics/
│ └── analytics_query.sql # Joins and prepares flattened analytics table
├── dashboard/
│ └── dashboard_final.png # Screenshot of Looker Studio dashboard
├── diagrams/
│ ├── architecture.jpg # GCP architecture used
│ └── data_model.jpeg # Entity relationship diagram
└── README.md

yaml
Copy
Edit

---

## Key Analytics & Metrics

The final analytics layer joins fact and dimension tables for BI-ready insights. Some metrics visualized:

- Total Revenue, Gross Margin, and Total Trips
- Average Fare per Trip and Tip %
- Trip Volume by Distance Range
- Avg Fare & Tip by Passenger Count
- Revenue Breakdown by Payment Method & Rate Code
- Credit Card Usage % (Gauge Chart)
- Rate Code to Payment Flow (Sankey Chart)
- Pickup Location Heatmap (Google Maps)

---

## Final Dashboard Preview

![Dashboard](https://lookerstudio.google.com/s/sDzkyan_hB4)

---

## Key Insights

- Majority of rides are 1–2 miles, with highest tip amounts for 3–4 passengers
- Over 66% of all rides were paid by credit card
- Standard rate dominates across both cash and card transactions
- Geospatial pickups are heavily concentrated in Midtown and Downtown Manhattan
- The average trip generates $13.25 in fare with 14.13% average tip

---
