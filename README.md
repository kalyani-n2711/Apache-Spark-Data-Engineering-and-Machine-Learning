# Apache Spark: Data Engineering and Machine Learning

A collection of three practical projects developed using **Apache Spark and Scala**, exploring distributed data processing, big data analytics, and machine learning through the Spark ecosystem.

The repository demonstrates the implementation of Spark RDDs, DataFrames, and MLlib through three independent assignments using synthetic datasets containing 10,000 records each.

## Projects Overview

### 1. Student Academic Performance Analysis Using Spark RDDs

**Objective:** Analyze student academic records using Apache Spark's Resilient Distributed Datasets (RDDs).

**Key Implementations:**
- Create and manipulate Student objects using Scala.
- Convert collections into Spark RDDs.
- Display student records.
- Filter students scoring above 75 marks.
- Calculate department-wise student counts.
- Compute average marks.
- Identify the highest-scoring student.
- Demonstrate RDD transformations and actions.
- Understand lazy evaluation and DAG execution.
- Explore distributed data processing.

**Core Concepts:** RDDs, Transformations, Actions, Pair RDDs, Lazy Evaluation, DAG.

### 2. Sales Data Processing and Business Intelligence Using Spark DataFrames

**Objective:** Process sales transaction data and extract business insights using Spark DataFrames.

**Key Implementations:**
- Load CSV datasets into Spark DataFrames.
- Inspect schema and dataset structure.
- Identify missing and invalid values.
- Calculate transaction-wise sales revenue.
- Perform category-wise revenue analysis.
- Identify the top five best-selling products.
- Calculate location-wise revenue.
- Filter transactions with sales above ₹10,000.
- Perform grouping, aggregation, sorting, and filtering.
- Compare RDDs and DataFrames.
- Examine execution plans and query optimization.

**Core Concepts:** Spark SQL, DataFrames, Aggregations, GroupBy, Filtering, Catalyst Optimizer, Execution Plans.

### 3. Healthcare Disease Prediction Using Apache Spark MLlib

**Objective:** Develop a machine learning pipeline for diabetes outcome prediction using Spark MLlib.

**Key Implementations:**
- Load and preprocess healthcare-style tabular data.
- Handle missing and invalid values.
- Identify input features and target variables.
- Apply VectorAssembler for feature transformation.
- Perform feature scaling.
- Split data into training and testing sets.
- Train three classification models:
  - Logistic Regression
  - Decision Tree Classifier
  - Random Forest Classifier
- Evaluate models using:
  - Accuracy
  - Precision
  - Recall
  - F1-score
- Compare models and select the best-performing classifier.
- Generate predictions for a new patient record.

**Core Concepts:** Spark MLlib, Machine Learning Pipelines, Feature Engineering, Classification, Model Evaluation.

> **Dataset Note:** The datasets used in these projects are synthetically generated for academic and experimental purposes. The healthcare dataset does not contain real patient records and is not intended for clinical diagnosis.

## Technology Stack

| Technology | Purpose |
|---|---|
| Apache Spark 3.5.3 | Distributed data processing |
| Scala 2.12.18 | Application development |
| Spark Core | RDD operations |
| Spark SQL | DataFrame processing |
| Spark MLlib | Machine learning |
| SBT | Build and dependency management |
| CSV | Dataset storage |

## Repository Structure

```text
Apache-Spark-Data-Engineering-and-Machine-Learning/
│
├── Assignment-1-Student-RDD-Analysis/
│   ├── data/
│   ├── src/
│   └── README.md
│
├── Assignment-2-Sales-DataFrame-Analysis/
│   ├── data/
│   ├── src/
│   └── README.md
│
├── Assignment-3-Healthcare-MLlib-Prediction/
│   ├── data/
│   ├── src/
│   └── README.md
│
├── README.md
├── build.sbt
└── .gitignore
```

*The directory structure may be adjusted to match the final project organization.*

## Getting Started

### Prerequisites

Install the following:

- Java JDK (compatible with your Spark installation)
- Scala 2.12
- Apache Spark 3.5.3
- SBT
- Git

### Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/Apache-Spark-Data-Engineering-and-Machine-Learning.git

cd Apache-Spark-Data-Engineering-and-Machine-Learning
```

### Build the Projects

Navigate to the relevant assignment directory and execute:

```bash
sbt clean compile
```

### Run an Assignment

```bash
sbt run
```

Select or configure the relevant main class if the project contains multiple Scala application entry points.

## Learning Outcomes

Through these assignments, the repository explores:

- Distributed computing with Apache Spark.
- RDD-based data transformations and actions.
- Structured data processing using Spark SQL.
- Data cleaning and exploratory analysis.
- Query optimization and execution planning.
- Machine learning pipeline development.
- Classification algorithms and performance evaluation.
- Understanding Spark's distributed execution architecture.

## Author

**Kalyani Agarwal**

B.Tech — Artificial Intelligence and Data Science

## License

This repository is intended for educational and academic purposes. Add a suitable open-source license if you intend to permit reuse and redistribution.

---

If you find this repository useful for learning Apache Spark, feel free to explore the projects and contribute.
