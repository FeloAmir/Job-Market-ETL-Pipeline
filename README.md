# Automated Job Market ETL & Telegram Alert System

## 📌 Project Overview
This project is an automated end-to-end **Data Engineering pipeline** designed to scrape, process, and deliver real-time job market insights. It automates the collection of tech job postings from **LinkedIn** and **Indeed**, cleans and transforms the data using **Pandas**, and delivers instant alerts via a **Telegram Bot**. The entire workflow is orchestrated on **Databricks** to ensure scalability and daily automation.

The project demonstrates how to:
* Automate web scraping from multiple sources using **JobSpy**.
* Implement a **Medallion Architecture** on a cloud-based environment (Databricks).
* Orchestrate Python scripts to run on a daily schedule.
* Integrate a **Telegram Bot** for real-time business/user notifications.
* Visualize job market trends through a high-end **Power BI Dashboard**.

---

##  Medallion Architecture
The pipeline follows the **Medallion Architecture** to ensure data integrity:

| Layer | Schema | Description |
| :--- | :--- | :--- |
| **Bronze** | `bronze_raw` | Raw job data extracted directly from LinkedIn & Indeed using JobSpy. |
| **Silver** | `silver_cleaned` | Cleaned data using Pandas: removed duplicates, handled NULLs, and standardized dates. |
| **Gold** | `gold_insights` | Refined dataset with job highlights and links, ready for Telegram alerts and Power BI. |

---

##  Tools & Technologies Used
* **Databricks:** Cloud orchestration and execution of Python notebooks.
* **JobSpy Library:** For concurrent scraping of job postings from LinkedIn and Indeed.
* **Pandas:** Data cleaning and transformation (Silver Layer).
* **Telegram Bot API:** Automated delivery of daily job alerts to a dedicated channel.
* **Power BI:** Professional interactive dashboard for market trend analysis.

---

##  Requirements & Analysis Goals
### Key Features & Questions:
1.  **Market Coverage:** Extracting tech jobs from 10+ countries with a single click.
2.  **Platform Comparison:** Which platform (LinkedIn vs Indeed) has more opportunities?
3.  **Role Popularity:** What are the top 10 most demanded job titles?
4.  **Hiring Leaders:** Which companies are currently dominating the hiring market?

### Dashboard Visuals Summary:
| Visual Type | Name | Purpose |
| :--- | :--- | :--- |
| **Cards (3)** | `Job Metrics` | Total Jobs, Active Countries, and Top Sources |
| **Treemap** | `Job Distribution` | Visualizing market density by country |
| **Donut Chart** | `Source Analysis` | Comparing LinkedIn vs Indeed job volume |
| **Line Chart** | `Posting Trend` | Tracking job posting velocity over time |
| **Table View** | `Gold Listings` | Searchable table with direct job URLs and company details |

---

## ⚙️ Automation Flow (Databricks Workflow)
1.  **Ingestion:** Python script triggers JobSpy to fetch new records.
2.  **Transformation:** Data is cleaned and filtered for specific tech keywords.
3.  **Telegram Alert:** A bot sends a summary of the "Gold" jobs to the user.
4.  **BI Update:** Power BI connects to the processed CSV/Parquet for the latest visuals.

---
*Developed as part of a Data Engineering Portfolio focusing on Cloud Automation, Web Scraping, and Real-time Notification Systems.*
