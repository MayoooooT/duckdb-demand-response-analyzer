# Automotive Demand Response Analyzer Using DuckDB

DSCI 551 Final Project — Spring 2026

---

# Project Overview

This project explores how DuckDB’s internal database architecture affects analytical query performance and application behavior through an automotive demand analysis application.

The project focuses on two main internal database concepts:

- Columnar storage
- Vectorized query execution

The application analyzes:
- Regional vehicle demand
- Monthly sales trends
- Pricing incentive behavior
- Demand response across regions

---

# Technologies Used

- Python
- DuckDB
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook / Google Colab

---

# Repository Structure

```text
duckdb-demand-response-analyzer/
│
├── duckdb_project_demo.ipynb
├── README.md
├── requirements.txt
└── Tong, May dsci551 final report.docx
```

---

# Setup Instructions

## Option 1 — Google Colab

1. Open Google Colab
2. Upload `duckdb_project_demo.ipynb`
3. Run all notebook cells from top to bottom

The notebook automatically:
- installs DuckDB
- generates synthetic data
- creates the DuckDB table
- executes analytical queries
- generates visualizations
- displays execution plans


---

## Option 2 — Local Setup

### Install Dependencies

```bash
pip install -r requirements.txt
```

Or manually:

```bash
pip install duckdb pandas numpy matplotlib jupyter
```

### Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
duckdb_project_demo.ipynb
```

Run all notebook cells.

---

# Dataset

This project uses synthetically generated automotive sales data.

The dataset includes:
- `sale_date`
- `region`
- `segment`
- `msrp`
- `incentive`
- `units_sold`
- `revenue`

The final generated dataset contains 300,000 rows.

---

# Synthetic Data Pipeline

This project uses synthetically generated automotive sales data instead of an uploaded external dataset.

The entire data pipeline is automated within the notebook.

The pipeline performs the following steps automatically:

1. Generate synthetic automotive sales data using Python and NumPy
2. Create a Pandas DataFrame
3. Connect to DuckDB
4. Create the `sales` table
5. Load the generated data into DuckDB using:

```python
CREATE TABLE sales AS SELECT * FROM df
```

6. Execute analytical SQL queries
7. Generate visualizations and execution plans


---

# Author

May Tong

DSCI 551 — Spring 2026  
University of Southern California
