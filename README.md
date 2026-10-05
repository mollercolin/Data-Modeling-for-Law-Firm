# Data-Modeling-for-Law-Firm
A unified relational database (MySQL) with a Python analytics layer and a Neo4j graph extension, built for a fictional boutique law firm: Data Management Spring 2026

# Fifty, Fifty & Moore, LLP: Divorce Law Firm Database

A unified relational database (MySQL) with a Python analytics layer and a Neo4j graph extension, built for a fictional boutique law firm that handles high-asset divorce cases.

**Author:** Colin Moller · DADS 6700 · Spring 2026

---

## Overview

Fifty, Fifty & Moore, LLP is a hypothetical firm whose data lives in siloed, redundant, disconnected systems. This project replaces that setup with a single relational database that brings together:

- **Case management:** cases, courts, docket numbers, and case types (Divorce, Post-Judgment, Pre-Nup)
- **Parties and families:** both the client and the opposing side, plus shared children
- **Financial data:** assets, liabilities, and monthly expenses, including jointly owned items and ownership percentages, for building financial affidavits and asset division schedules
- **Scheduling:** hearings, depositions, and meetings tied to each case
- **Billing:** time entries logged by attorneys, paralegals, and secretaries against a case

The project moves through the full design process: conceptual modeling (EER and UML), logical modeling (relational schema), implementation in MySQL, analysis in a Jupyter notebook, and a NoSQL graph version of the financial data in Neo4j.

## Tech Stack

| Layer | Tools |
|---|---|
| Modeling | EER and UML diagrams |
| Relational DB | MySQL 8, MySQL Workbench |
| Analysis | Python, pandas, SQLAlchemy, mysql-connector, matplotlib, seaborn, Jupyter |
| Graph DB | Neo4j Desktop, Cypher |
| Sample data | Synthetic data generated with Gemini, cleaned up with Claude |

## Repository Structure

```
.
├── Create_DB.sql            # Creates the database and all 17 tables
├── Populate_DB.sql          # Inserts synthetic sample data (~1,000 lines)
├── Divorce_db_notebook.ipynb  # Python app: queries + visualizations
├── neo4j/
│   ├── Assets.csv
│   ├── Liabilities.csv
│   ├── Expenses.csv
│   ├── PARTY.csv
│   └── PF.csv               # Party–Financial links (become graph edges)
└── docs/
    └── Moller_Final_Project_Summary.pdf
```

## Disclaimer

This is an academic project. All people, cases, and financial records are fictional.
