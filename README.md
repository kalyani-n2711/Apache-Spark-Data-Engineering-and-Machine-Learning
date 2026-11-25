# Apache Spark Data Engineering and Machine Learning

A complete, self-contained **Scala 2.12 + Apache Spark 3.5.3** repository demonstrating distributed RDD processing, DataFrame Business Intelligence with the Catalyst Optimizer, and scalable Machine Learning pipelines using Spark MLlib.

> **Synthetic Data Notice:** All three 10,000-row CSV datasets stored in each assignment's `data/` directory are **synthetic** datasets created for academic Big Data Analytics coursework and benchmarking.

---

## Repository Structure

```text
Apache-Spark-Data-Engineering-and-Machine-Learning/
│
├── Assignment-1-Student-RDD-Analysis/
│   ├── data/
│   │   └── student_academic_performance_synthetic_10000.csv   # 10,000 synthetic student records
│   ├── project/build.properties
│   ├── scripts/generate_charts.py
│   ├── src/main/scala/edu/university/rdd/
│   │   ├── Student.scala
│   │   └── StudentAcademicAnalysis.scala
│   ├── build.sbt
│   ├── pom.xml
│   ├── run.ps1
│   └── README.md
│
├── Assignment-2-Sales-DataFrame-Analysis/
│   ├── data/
│   │   └── sales_transactions_synthetic_10000.csv             # 10,000 synthetic retail records
│   ├── project/build.properties
│   ├── scripts/generate_charts.py
│   ├── src/main/scala/edu/university/df/
│   │   └── SalesDataFrameAnalysis.scala
│   ├── build.sbt
│   ├── pom.xml
│   ├── run.ps1
│   └── README.md
│
├── Assignment-3-Healthcare-MLlib-Prediction/
│   ├── data/
│   │   └── synthetic_diabetes_prediction_10000.csv            # 10,000 synthetic patient records
│   ├── project/build.properties
│   ├── scripts/generate_charts.py
│   ├── src/main/scala/edu/university/mllib/
│   │   └── DiabetesPredictionPipeline.scala
│   ├── build.sbt
│   ├── pom.xml
│   ├── run.ps1
│   └── README.md
│
├── .gitignore
├── LICENSE
└── README.md
```

---

## Assignments Overview

| # | Project | Spark API | Synthetic Dataset (10,000 Rows) | Key Highlights |
|---|---|---|---|---|
| **1** | [Assignment-1-Student-RDD-Analysis](Assignment-1-Student-RDD-Analysis/README.md) | **Spark Core RDDs** | `student_academic_performance_synthetic_10000.csv` | `Student` case class, `parallelize` & `textFile` RDDs, `reduceByKey` & `aggregateByKey`, lazy evaluation (`0` jobs on transformations vs. `2` jobs on `collect`), `toDebugString` DAG inspection |
| **2** | [Assignment-2-Sales-DataFrame-Analysis](Assignment-2-Sales-DataFrame-Analysis/README.md) | **Spark SQL & DataFrames** | `sales_transactions_synthetic_10000.csv` | Explicit `StructType` schema, data-quality audit (`55` invalid/missing rows cleaned), `INR 118.66M` revenue analytics, top-5 products, Catalyst Optimizer plans (`PushedFilters`, Column Pruning), RDD vs. DataFrame benchmark |
| **3** | [Assignment-3-Healthcare-MLlib-Prediction](Assignment-3-Healthcare-MLlib-Prediction/README.md) | **Spark MLlib Pipelines** | `synthetic_diabetes_prediction_10000.csv` | Biologically invalid `0.0` audit & median `Imputer`, `VectorAssembler`, `StandardScaler`, class-weighted Logistic Regression / Decision Tree / Random Forest comparison, unseen patient prediction |

---

## Technology Stack

- **Language:** Scala `2.12.18`
- **Distributed Engine:** Apache Spark `3.5.3` (`spark-core`, `spark-sql`, `spark-mllib`)
- **Runtime:** Java `17` (`--add-opens` module flags preconfigured in `build.sbt`, `pom.xml`, and Scala CLI directives)
- **Build & Execution:** `sbt 1.10.2`, Apache Maven `3.9+`, or Scala CLI `1.15+`
- **Visualization (Optional):** Python `3.10+` with `pandas` and `matplotlib`

---

## Quick Start

Each assignment folder is completely independent and can be built and executed on its own:

### Using `sbt`
```bash
cd Assignment-1-Student-RDD-Analysis
sbt run
```

### Using `scala-cli` (with Java 17)
```powershell
$env:JAVA_HOME = "C:\Program Files\Android\Android Studio\jbr"
$env:PATH = "$env:JAVA_HOME\bin;$env:PATH"
cd Assignment-1-Student-RDD-Analysis
.\run.ps1
```

### Using Apache Maven
```bash
cd Assignment-1-Student-RDD-Analysis
mvn compile exec:java
```

Replace `Assignment-1-Student-RDD-Analysis` with `Assignment-2-Sales-DataFrame-Analysis` or `Assignment-3-Healthcare-MLlib-Prediction` to run Assignments 2 and 3. Each run writes reproducible CSV summaries, execution reports, and Spark UI REST snapshots to an ignored `outputs/` folder inside that assignment directory.

---

## License

This repository is licensed under the [MIT License](LICENSE).
