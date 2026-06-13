# Finance Data Engineering Project using Databricks

## Overview

This project demonstrates an end-to-end Data Engineering pipeline built on Databricks using the Medallion Architecture (Bronze, Silver, and Gold layers). The pipeline generates synthetic financial transaction data, processes it through multiple transformation stages, and produces analytics-ready datasets for business reporting.

The project showcases key Data Engineering concepts including data ingestion, data transformation, data quality management, and analytical data modeling.

---
## Project Highlights

- Built an end-to-end Data Engineering pipeline using Databricks
- Implemented Bronze, Silver, and Gold Medallion Architecture
- Generated and processed 100K+ financial transactions
- Built interactive SQL dashboards for business reporting
- Performed fraud detection and risk analysis
- Leveraged Delta Lake for scalable data storage
- Integrated GitHub version control with Databricks
## Architecture

```text
Raw Data Generation
        │
        ▼
   Bronze Layer
 (Raw Ingestion)
        │
        ▼
   Silver Layer
 (Data Cleaning &
  Transformation)
        │
        ▼
    Gold Layer
 (Business Metrics &
  Analytics Tables)
```

---

## Project Structure

```text
Finance_DE_Project
│
├── 01_Data_Generation
│   └── Generate_Finance_Data.ipynb
│
├── 02_Bronze
│   └── Bronze_Layer.ipynb
│
├── 03_Silver
│   └── Silver_Layer.ipynb
│
├── 04_Gold
│   └── Gold_Layer.ipynb
│
└── workflow_design.md
```

---

## Technologies Used

- Databricks
- Apache Spark
- PySpark
- Python
- Delta Lake
- Pandas
- Faker
- GitHub

---

## Medallion Architecture

### Bronze Layer

**Purpose**
- Ingest raw financial data
- Preserve original records
- Store data without transformations

**Operations**
- Data loading
- Schema validation
- Raw data storage

### Silver Layer

**Purpose**
- Clean and standardize data
- Handle missing values
- Improve data quality

**Operations**
- Data cleansing
- Data validation
- Type conversions
- Business rule application

### Gold Layer

**Purpose**
- Create analytics-ready datasets
- Generate business metrics
- Support reporting and dashboards

**Operations**
- Aggregations
- KPI calculations
- Financial summaries
- Reporting datasets

---

## Dataset

Synthetic financial data is generated using the Faker library.

### Sample Fields

| Column | Description |
|----------|------------|
| customer_id | Unique customer identifier |
| name | Customer name |
| email | Customer email |
| city | Customer location |
| transaction_id | Transaction identifier |
| amount | Transaction amount |
| transaction_date | Transaction date |
| payment_method | Payment type |

---

## Pipeline Workflow

### Step 1 – Data Generation

Generate realistic synthetic finance data using Python and Faker.

**Output**

```text
Raw Finance Dataset
```

### Step 2 – Bronze Layer

Load generated data into the Bronze layer.

**Output**

```text
Raw Delta Tables
```

### Step 3 – Silver Layer

Clean, validate, and standardize data.

**Output**

```text
Processed Delta Tables
```

### Step 4 – Gold Layer

Create analytical datasets and business KPIs.

**Output**

```text
Reporting Tables
```

---

## Key Features

- End-to-End Data Pipeline
- Medallion Architecture Implementation
- Delta Lake Storage
- Synthetic Data Generation
- Data Quality Validation
- Scalable Spark Processing
- Analytics-Ready Gold Layer
- Git Integration with Databricks

---

## Sample Business Insights

The Gold Layer can be used to analyze:

- Total Revenue
- Customer Spending Patterns
- Transaction Trends
- Regional Performance
- Payment Method Distribution
- Monthly Financial KPIs

---

## How to Run

### Clone Repository

```bash
git clone https://github.com/FathimaNafra/finance-databricks-data-engineering-project.git
```

### Open in Databricks

1. Import the repository into Databricks.
2. Attach a cluster or use Serverless Compute.
3. Execute notebooks in the following order:

```text
01_Data_Generation
      ↓
02_Bronze
      ↓
03_Silver
      ↓
04_Gold
```

---

## Learning Outcomes

This project demonstrates:

- Data Engineering Fundamentals
- Apache Spark Processing
- Delta Lake Implementation
- ETL/ELT Pipeline Development
- Data Lakehouse Architecture
- Databricks Workflow Development
- Git Version Control Integration

## Dashboard Preview

The Gold Layer data is visualized through an interactive Databricks SQL Dashboard that provides insights into transaction performance, customer activity, and fraud risk analysis.

### Key Metrics

| Metric | Value |
|----------|----------|
| Total Customers | 5,000 |
| Total Transactions | 100,000 |
| Total Transaction Amount | $251.02M |
| Average Transaction Amount | $2,510.25 |
| Fraud Transactions | 16.66K |

### Dashboard Features

#### Revenue Analytics
- Monthly Revenue Trend
- Country Revenue Analysis
- Revenue Performance Monitoring

#### Customer Analytics
- Top 10 Customers by Spending
- Customer Transaction Analysis
- Spending Pattern Identification

#### Transaction Analytics
- Transaction Type Distribution
- Payment Method Analysis
- Transaction Volume Monitoring

#### Fraud Analytics
- Fraud Risk Distribution
- Fraud by Transaction Type
- Risk Category Classification
- Fraud Detection Insights

### Dashboard Insights

- Processed over 100,000 financial transactions
- Generated revenue analytics from $251M+ transaction volume
- Identified 16,000+ potentially fraudulent transactions
- Classified fraud risk into Low, Medium, and High categories
- Analyzed customer spending behavior across multiple transaction channels

### Technologies Used

- Databricks SQL Dashboard
- Apache Spark
- Delta Lake
- PySpark
- SQL Analytics
- Databricks Lakehouse Platform

## Author

**Fathima Nafra**

GitHub: https://github.com/FathimaNafra

---

