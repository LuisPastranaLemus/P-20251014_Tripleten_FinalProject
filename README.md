# 🧭 Project Analysis

A comprehensive data analysis project divided into three independent case studies designed to demonstrate practical skills in data cleaning, transformation, statistical analysis, and storytelling. It includes a full diagnostic analysis for decision-making, an A/B test evaluation using hypothesis testing, and an SQL case focused on database exploration and business insights.

---

## 🔍 Project Overview (P-20251014_Tripleten_FinalProject)

1️⃣ Main Case – Diagnostic Analysis and Communication of Results

Application of data cleansing, transformation, and analysis techniques to obtain actionable insights that support business decision-making.
Includes:

- Task decomposition and definition of the analytical plan.   
- Complete workflow implementation: loading, processing, visualization, and communication of findings.

2️⃣ A/B Testing – Experimental Analysis and Statistical Validation

Evaluation of the impact of an A/B test through the use of conversion funnels, business metrics, and hypothesis testing.
Rigorous analysis of the experiment's performance is performed, supported by statistical inference.

3️⃣ SQL Management – ​​Relational Database Querying and Exploration

Exploration of a multi-table database using advanced SQL queries to obtain relevant information, identify patterns, and answer business questions.

🧠 Applied Skills

- Python (pandas, NumPy, matplotlib, seaborn, SciPy)
- SQL (JOIN queries, CTEs, aggregations, subqueries)
- Descriptive and inferential statistics
- Hypothesis testing and A/B analysis
- Storytelling with data and communicating results

---

1️⃣ Main Case – Telecommunications: Identifying ineffective operators

The virtual phone service CallMeMaybe is developing a new feature that will provide supervisors with insight into the least effective operators. An operator is considered ineffective if it has a high number of missed incoming calls (internal and external) and a long wait time for incoming calls. Furthermore, if an operator is supposed to make outgoing calls, a low number of them will also be a sign of ineffectiveness.

- Conduct exploratory data analysis
- Identify ineffective operators
- Test statistical hypotheses

🧮 Data Dictionary

The datasets contain information on the use of the virtual phone service CallMeMaybe. Its customers are organizations that need to distribute a large number of incoming calls among multiple operators or make outgoing calls through their operators. Operators can also make internal calls to communicate with each other. These calls are made through the CallMeMaybe network.

This project has 2 different tables.

- `telecom_dataset_us.csv` (customers' activities data)
  - `user_id`: Customer account ID
  - `date`: Date statistics were retrieved
  - `direction`: Call direction (`out` for outgoing, `in` for incoming)
  - `internal`: Whether the call was internal (between a customer's operators)
  - `operator_id`: Operator ID
  - `is_missed_call`: Whether the call was missed
  - `calls_count`: Number of calls
  - `call_duration`: Call duration (not including hold time)
  - `total_call_duration`: Call duration (including hold time)

- `telecom_clients_us.csv` (customers' data)
  - `user_id`: User ID
  - `tariff_plan`: Current customer rate
  - `date_start`: Customer registration date


Key questions:

- Call duration
- Call direction
- Call type (internal or external)
- Show the share of internal and external calls
- Number of calls per day

---




---

## 📚 Guided Foundations (Historical Context)

The notebook `00-guided-analysis_foundations.ipynb` reflects an early stage of my data analysis learning journey, guided by TripleTen. It includes data cleaning, basic EDA, and early feature exploration, serving as a foundational block before implementing the improved structure and methodology found in the main analysis.

---

## 📂 Project Structure

```bash
├── data/
│   ├── raw/              # Original dataset(s) in CSV format
│   ├── interim/          # Intermediate cleaned versions
│   └── processed/        # Final, ready-to-analyze dataset
│
├── notebooks/
│   ├── 00-guided-analysis_foundations.ipynb     ← Initial guided project (TripleTen)
│   ├── 01_cleaning.ipynb                        ← Custom cleaning 
│   ├── 02_feature_engineering.ipynb             ← Custom feature engineering
│   ├── 03_eda_and_insights.ipynb                ← Exploratory Data Analysis & visual storytelling
│   └── 04-sda_hypotheses.ipynb                  ← Business insights and hypothesis testing
│
├── src/
│   ├── init.py              # Initialization for reusable functions
│   ├── data_cleaning.py     # Data cleaning and preprocessing functions
│   ├── data_loader.py       # Loader for raw datasets
│   ├── eda.py               # Exploratory data analysis functions
│   ├── features.py          # Creation and transformation functions for new variables to support modeling and EDA
│   └── utils.py             # General utility functions for reusable helpers
│
├── outputs/
│   └── figures/          # Generated plots and visuals
│
├── requirements/
│   └── requirements.txt      # Required Python packages
│
├── .gitignore            # Files and folders to be ignored by Git
└── README.md             # This file
```
---

🛠️ Tools & Libraries

- Python 3.11
- os, pathlib, sys, pandas, NumPy, Matplotlib, seaborn, IPython.display, scipy.stats
- Jupyter Notebook
- Git & GitHub for version control
-

---

## 📌 Notes

This project is part of a personal learning portfolio focused on developing strong skills in data analysis, statistical thinking, and communication of insights. Constructive feedback is welcome.

---

## 👤 Author   
##### Luis Sergio Pastrana Lemus   
##### Engineer pivoting into Data Science | Passionate about insights, structure, and solving real-world problems with data.   
##### [GitHub Profile](https://github.com/LuisPastranaLemus)   
##### 📍 Querétaro, México     
##### 📧 Contact: luis.pastrana.lemus@engineer.com   
---

