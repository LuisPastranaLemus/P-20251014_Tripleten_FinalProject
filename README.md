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

2️⃣ A/B Testing – You've received an analytical task from an international online store. Your predecessors failed to complete it: they launched an A/B test and then abandoned it (to start a watermelon farm in Brazil). They left only the technical specifications and test results.

🧮 Technical Description

- Test name: `recommender_system_test`
- Groups: A (control), B (new checkout funnel)
- Launch date: 2020-12-07
- Date new users stopped being accepted: 2020-12-21
- End date: 2021-01-01
- Audience: 15% of new users from the EU region
- Test purpose: To test changes related to the introduction of an improved recommendation system
- Expected outcome: Within 14 days of enrollment, users will show improved conversion rates for product page views (the `product_page` event), adding items to cart (`product_card`), and purchases (`purchase`). At each stage of the `product_page → product_card → purchase` funnel, there will be at least a 10% increase.
- Expected number of test participants: 6,000

Download the test data, check if it was performed correctly, and analyze the results.

🧮 Data Dictionary

- `ab_project_marketing_events_us.csv` (The marketing events calendar for 2020)
  - `name`: The name of the marketing event
  - `regions`: The regions where the advertising campaign will be run
  - `start_dt`: The campaign start date
  - `finish_dt`: Campaign end date
  
- `final_ab_new_users_upd_us.csv` (All users who registered in the online store from December 7 to 21, 2020)
  - `user_id`: user identification
  - `first_date`: Registration date
  - `region`: user location
  - `device`: Device used for registration

- `final_ab_events_upd_us.csv`: All new user events from December 7, 2020, to January 1, 2021
  - `user_id`: user identification
  - `event_dt`: Date and time of the event
  - `event_name`: Name of the event type
  - `details`: Additional information about the event (e.g., the total order in USD for `purchase` events)
  
- `final_ab_participants_upd_us.csv`: Table with test participant data
  - `user_id`: user identification
  - `ab_test`: Test name

Key questions:

- Describe the objectives of the study.
- Explore the data:
  - Is it necessary to convert the rates?
  - Are there any missing or duplicate values? If so, how would you characterize them?
- Conduct exploratory data analysis:
  - Study conversion at the different stages of the funnel.
  - Is the number of events per user evenly distributed across the samples?
  - Are there any users present in both samples?
  - How is the number of events distributed across days?
  - Are there any peculiarities in the data that need to be taken into account before starting the A/B test?
- Evaluate the A/B test results:
  - What can you say about the A/B test results?
  - Use a z-test to test the statistical difference between the proportions.
- Describe your conclusions regarding the EDA stage and the A/B test results.

---

3️⃣ SQL Management – The coronavirus took the entire world by surprise, changing everyone's daily routine. City dwellers were no longer spending their free time outside, going to cafes and shopping malls; instead, more people were staying home, reading books. This attracted the attention of startups, who rushed to develop new apps for book lovers.

You've been given a database from one of the services competing in this market. It contains data on books, publishers, authors, and customer ratings and book reviews. This information will be used to generate a value proposition for a new product.

🧮 Data Dictionary

- `books` (Contains data about books)
  - `book_id`: Book ID
  - `author_id`: Author ID
  - `title`: Title
  - `num_pages`: Number of pages
  - `publication_date`: Date of publication
  - `publisher_id`: Publisher ID

- `authors` (Contains data about authors)
  - `author_id`: Author ID
  - `author`: The author

- `publishers` (Contains data about publishers)
  - `publisher_id`: Publisher ID
  - `publisher`: The publisher

- `ratings` (Contains data about user ratings)
  - `rating_id`: Rating ID
  - `book_id`: Book ID
  - `username`: The name of the user who reviewed the book book
  - `rating`: rating

- `reviews` (Contains data about customer reviews)
  - `review_id`: review ID
  - `book_id`: book ID
  - `username`: the name of the user who reviewed the book
  - `text`: the text of the review

Instructions for Completing the Task

- Describe the objectives of the study.
- Study the tables (print the first rows).
- Write an SQL query for each of the tasks.
- Generate the results of each query in the Notebook.
- Describe your conclusions for each of the tasks.

Key questions:

- Find the number of books published after January 1, 2000.
- Find the number of user reviews and the average rating for each book.
- Identify the publisher that has published the largest number of books with more than 50 pages (this will help you exclude pamphlets and similar publications from your analysis).
- Identify the author with the highest average book rating: look only at books with at least 50 ratings.
- Find the average number of full-text reviews among users who rated more than 50 books.

__NOTES__
- Don't forget about functions! They can make your life and query execution much easier.
- Your results must be obtained with SQL. Use pandas only to print and store query results.
  
---

The project will consist of three components:

- A notebook with your code (.ipynb)
- A presentation (.pdf)
- A link to your dashboard in Tableau Public (`dashboard.txt`) (optional)

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

