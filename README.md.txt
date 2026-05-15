# Team Compliance Tracker

## Project Overview
A data analysis project that monitors team productivity and compliance — 
tracking whether agents are completing what they claim, and whether they 
are submitting work on time.

Inspired by real workforce audit workflows from my experience at Amazon.

## Business Problem
Managers need visibility into:
- Are agents completing the number of tasks they report?
- Who is consistently submitting work late?
- Which team has better compliance overall?
- What is each agent's overall compliance rating?

## Tools Used
- **Python** (Pandas, NumPy) — data generation and analysis
- **PostgreSQL** — data storage and SQL querying
- **SQLAlchemy** — Python to PostgreSQL connection
- **Excel** — output and reporting

## Dataset
Dummy dataset of 650 records simulating 10 agents across 2 teams 
over 65 working days, with fields:
- `date` — working date
- `agent_name` — team member
- `tasks_claimed` — productivity reported by agent
- `tasks_actual` — actual verified output
- `submitted_at` — timestamp of work submission
- `team` — Team A or Team B

## Analysis & Key Findings

### 1. Overclaiming Analysis
Rohit Das and Anita Singh showed the highest average gap between 
claimed and actual tasks (avg gap of 4).
Sneha Gupta was the most accurate — zero gap.

### 2. Late Submission Analysis
Karan Mehta had the highest late submission rate at 30.8%.
Anita Singh was most punctual at 13.8% late.

### 3. Team Comparison
Both teams showed similar compliance — avg gap of 2 and ~22% late 
submissions — suggesting the issue is individual behaviour, 
not team culture.

### 4. Compliance Scorecard (Green / Amber / Red)
- **Green:** Arjun Kapoor (Team B)
- **Amber:** Most agents — acceptable performance
- **Red:** Priya Sharma Team A, Karan Mehta, Rahul Verma Team A 
  flagged for high gap or late submission rates

## Files
- `compliance_analysis.ipynb` — full analysis notebook
- `compliance_tracker.csv` — raw dataset
- `compliance_analysis.xlsx` — output with 4 sheets

## How to Run
1. Install dependencies: `pip install pandas sqlalchemy psycopg2-binary`
2. Create a PostgreSQL database called `compliance_tracker`
3. Run all cells in `compliance_analysis.ipynb`