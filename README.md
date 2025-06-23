# Reddit Data Engineering Pipeline 🚀

A full-stack data pipeline to extract, transform, and load Reddit data into Amazon Redshift using Apache Airflow, Celery, PostgreSQL, S3, AWS Glue, and Athena.

---

## 📌 Table of Contents

* [Project Summary](#project-summary)
* [Architecture](#architecture)
* [Prerequisites](#prerequisites)
* [Environment Setup](#environment-setup)
* [Running the Pipeline](#running-the-pipeline)
* [Demo](#demo)

---

## 📄 Project Summary

This end-to-end data pipeline is built to automate the ETL (Extract, Transform, Load) process for Reddit data. The flow involves pulling data from Reddit’s API, staging it in S3, transforming it using AWS Glue and Athena, and loading the final dataset into Amazon Redshift for analytics.

---

## 🏗 Architecture

The pipeline includes the following components:

* **Reddit API** – Acts as the primary data source.
* **Apache Airflow + Celery** – Handles orchestration and distributed task execution.
* **PostgreSQL** – Stores intermediate data and Airflow metadata.
* **Amazon S3** – Stores raw JSON files pulled from Reddit.
* **AWS Glue** – Manages the schema and performs transformation tasks.
* **Amazon Athena** – Runs SQL-based transformations directly on S3.
* **Amazon Redshift** – Final destination for analytics-ready structured data.

Architecture diagram available in `RedditDataEngineering.png`.

---

## ✅ Prerequisites

Ensure you have the following:

* An AWS account with access to S3, Glue, Athena, and Redshift
* Reddit API credentials
* Python 3.9+ installed
* Docker and Docker Compose installed

---

## ⚙️ Environment Setup

Clone the repository:

```bash
git clone https://github.com/airscholar/RedditDataEngineering.git
cd RedditDataEngineering
```

Create and activate a virtual environment:

```bash
python3 -m venv venv
source venv/bin/activate
```

Install Python dependencies:

```bash
pip install -r requirements.txt
```

Configure credentials:

```bash
mv config/config.conf.example config/config.conf
# Edit config.conf with your Reddit and AWS credentials
```

---

## 🚀 Running the Pipeline

Start the services using Docker Compose:

```bash
docker-compose up -d
```

Access the Airflow UI:

```bash
http://localhost:8080
```

Use Airflow to trigger and monitor the ETL DAG that processes Reddit data from extraction to loading in Redshift.

---

## 🎥 Demo

*(Include video walkthrough link or instructions for local testing/demo if applicable)*

---

Let me know if you’d like a `README.md` file generated from this directly or want to push it to your GitHub.
