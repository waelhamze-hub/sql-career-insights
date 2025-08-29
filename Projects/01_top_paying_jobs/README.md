# Top Paying Jobs

## Project Overview
This project identifies the top-paying **Data Analyst** jobs that are available **remotely (Anywhere)**.  
It demonstrates how to use SQL to join fact and dimension tables, filter records, and sort data to extract meaningful insights from job market datasets.

## Problem Statement
Which Data Analyst jobs offer the highest annual salary for remote positions?

## SQL Query Logic
- **FROM job_postings_fact**: Main fact table containing job postings and salary info.  
- **LEFT JOIN company_dim**: To retrieve the company name associated with each job posting.  
- **WHERE conditions**:  
  - job_title_short = 'Data Analyst' → Focus on Data Analyst roles.  
  - job_location = 'Anywhere' → Select remote jobs.  
  - salary_year_avg IS NOT NULL → Filter out postings without salary info.  
- **ORDER BY salary_year_avg DESC** → Rank jobs from highest to lowest salary.  
- **LIMIT 10** → Retrieve only the top 10 jobs.

## Skills Demonstrated
- SQL SELECT statements  
- Filtering with WHERE clauses  
- LEFT JOINs  
- Ordering and limiting results  
- Analyzing job market data
