# 👋 Hi, I'm Naseer Aryobee

Database and Data Engineer with 10+ years of experience working with Microsoft SQL Server, PostgreSQL and MySQL in healthcare systems. I specialize in building scalable data solutions, ETL/ELT pipelines, and analytics platforms that turn raw data into defensible insights.

🌐 **View my full portfolio at [www.nasaryobee.com](https://nasaryobee.com)** — the best place to see my work in context, with live dashboards and project case studies.

---

## 🚀 Featured Projects

### 🧬 Cancer & Environment Lakehouse
An end-to-end Databricks Lakehouse project investigating potential associations between U.S. cancer rates and environmental, lifestyle, and water quality factors. Built on 52.8 million rows across 33 Delta tables from 5 federal agencies (CDC, EPA, USDA).
- Databricks Workflows orchestration (25-task DAG, 16m 35s end-to-end)
- Bronze → Silver → Gold Medallion Architecture with Unity Catalog & managed Volumes
- Multi-factor Pearson correlation matrix across 17 environmental and lifestyle factors
- Random Forest regression (R² = 0.81) and binary classifier (AUC = 1.0) using scikit-learn
- Three Tableau Public dashboards: Cancer Overview, Water Quality Deep Dive, Environmental Risk Profile
- Headline finding: COPD prevalence is the strongest cancer mortality predictor (**r = 0.885**); PM2.5 days emerged as top ML feature despite weak Pearson correlation (r = 0.199)

🔗 [GitHub repo](https://github.com/aryobeen007/cancer-environment-lakehouse) · [Live project page](https://nasaryobee.com/projects/cancer-environment-lakehouse/) · [Tableau dashboards](https://public.tableau.com/app/profile/naseer3899/viz/CancerEnvironmentLakehouse/CancerEnvironmentOverview)


### 🏥 Medicare Provider Spending vs Quality Analysis
An end-to-end Databricks medallion pipeline analyzing whether Medicare actually pays more for better hospital care. Built on 10 million CMS records across 13 Delta tables.

- Databricks Workflows orchestration (4-task DAG, 5m 26s end-to-end)
- Bronze → Silver → Gold medallion architecture with Unity Catalog
- Two dashboards: Databricks AI/BI + Tableau Public (live, public)
- Headline finding: hospital cost-vs-quality correlation **r = 0.033** — essentially zero

🔗 [GitHub repo](https://github.com/aryobeen007/medicare-provider-spending-vs-quality) · [Live project page](https://nasaryobee.com/projects/medicare-pipeline/) · [Tableau dashboard](https://public.tableau.com/app/profile/naseer3899/viz/MedicareProviderSpendingvsQuality/MedicareProviderSpendingvsQuality)

---

### 📊 OBBB Medicaid Medicare Impact
A data-driven dashboard analyzing the projected 10-year impact of the OBBB Act on Medicaid, Medicare, healthcare funding, coverage losses, and state-level outcomes.

- Healthcare policy modeling and forecasting
- Multi-source federal data integration
- Interactive dashboard for state-level exploration

🔗 [GitHub repo](https://github.com/aryobeen007/OBBB-Healthcare-Impact-Analysis) · [Live dashboard](https://nasaryobee.com/OBBB_Impact_Dashboard_final.html)

---

### 🎓 Education Technology Impact Analysis
Analyzing how technology access impacts student outcomes across U.S. public schools using federal datasets.

- Data engineering pipeline (ETL → PostgreSQL)
- Multi-source data integration (CCD, NAEP, CRDC)
- Quarto-based reproducible analysis

🔗 [GitHub repo](https://github.com/aryobeen007/education-tech-impact-analysis) · [Live project page](https://nasaryobee.com/education_tech_impact_pipeline.html)

---

### 🌐 MAPS Assessment (Production Application)
Live platform helping users assess career readiness and career pathways.

- Full-stack web application
- Real-time user interaction
- Deployed and actively used
- iOS & Android Apps

🔗 [mapsassessment.com](https://mapsassessment.com)

---

### 🐘 PostgreSQL DBA End-to-End Project
An end-to-end PostgreSQL database administration project built on 9.6 million CMS Medicare records. Covers the full DBA discipline — schema design, performance baselining, index optimization, backup and recovery, health monitoring, role-based access control, row-level security, and audit logging.

- Normalized schema design with staged bulk loading (9.6M rows, 57-second COPY)
- Baseline diagnostics using pg_stat_statements and EXPLAIN ANALYZE
- 5 targeted indexes with CREATE INDEX CONCURRENTLY — 4,136× improvement on Q2
- Two-tier backup strategy: pg_dump (85% compression) + pg_basebackup with pg_verifybackup
- RBAC with 4 least-privilege roles + Row-Level Security (54,351 of 1.17M rows visible to app user)
- Trigger-based audit logging capturing full before/after data as JSONB

🔗 [GitHub repo](https://github.com/aryobeen007/postgresql-dba-project) · [Live project page](https://nasaryobee.com/projects/postgresql-dba/)

### 🔄 PostgreSQL to SQL Server Migration Project
An end-to-end PostgreSQL to Microsoft SQL Server migration built on a CMS Medicare provider dataset. Covers the full migration discipline — source assessment, schema conversion, custom ETL, multi-layer validation, and honest performance tuning against the original system.
- Full source inventory across 2 schemas, 5 tables, and 20.5M rows, flagging PostgreSQL-specific types (jsonb, inet) before conversion began
- Pivoted from Microsoft's SSMA (discovered mid-project it no longer supports PostgreSQL) to a custom Python ETL — psycopg2 + pyodbc, ~20.5M rows migrated in under 15 minutes
- Rewrote a generic PL/pgSQL audit trigger as native T-SQL using SQL Server 2025's JSON type and FOR JSON PATH, verified against real INSERT/UPDATE/DELETE tests
- Three-layer validation — aggregate checksums, 4/4 constraint-enforcement tests, and query diffing — 100% match against the source
- Baselined 6 representative queries; investigated a 2× regression with 4 separate tuning attempts, concluding a genuine structural bottleneck rather than forcing a fix
- SQL Server faster on 4 of 6 baseline queries, backed by real execution-plan evidence
🔗 [GitHub repo](https://github.com/aryobeen007/sqlserver-postgresql-migration) · [Live project page](https://nasaryobee.com/projects/postgresql-to-sqlserver/)


### 🐬 MySQL DBA End-to-End Project
An end-to-end MySQL database administration project built on publicly available EPA, CDC, and USDA datasets exploring the relationship between cancer rates and environmental factors across the U.S. Covers the full DBA discipline — star schema design, bulk data loading, performance optimization, backup and recovery, and role-based access control.

- Star schema with 4 dimension tables and 10 fact tables — 22.7M rows loaded across 14 tables
- Baseline diagnostics using EXPLAIN — Q4 identified as 9 min 42 sec full table scan on 15.3M rows
- Composite indexes + CTE rewrites — Q4 improved 95.5%, Q5 improved 96.5%
- Index audit via sys.schema_unused_indexes — dropped 11 unused indexes, diagnosed and resolved 2 regressions
- Full backup and recovery with mysqldump --single-transaction — 2.18 GB backup, full restore verified across all 22.7M rows
- RBAC with 3 least-privilege roles (db_readonly, db_analyst, db_etl) — no application user holds global privileges

🔗 [GitHub repo](https://github.com/aryobeen007/mysql-dba-project) · [Live project page](https://nasaryobee.com/projects/mysql-dba/)


## 🧰 Tech Stack

**Databases**
- Microsoft SQL Server
- PostgreSQL
- MySQL

**Data Engineering**
- Databricks (Lakehouse, Workflows, Unity Catalog)
- PySpark & Delta Lake
- ETL/ELT Pipelines
- Medallion Architecture
- Data Modeling & SQL Optimization

**Visualization & BI**
- Tableau / Tableau Public
- Databricks AI/BI Dashboards
- Quarto

**Languages & Tools**
- Python
- SQL
- PowerShell
- Git & GitHub
- Databricks CLI

---

## 📈 Current Focus

- Building reproducible, production-grade data pipelines
- Healthcare data engineering on public CMS datasets
- Translating complex pipeline work into clear portfolio case studies

---

## 📫 Connect With Me

- 🌐 Portfolio: [nasaryobee.com](https://nasaryobee.com)
- 💼 LinkedIn: [linkedin.com/in/naseer-aryobee](https://linkedin.com/in/naseer-aryobee)
- 📧 Email: Info@nasaryobee.com
