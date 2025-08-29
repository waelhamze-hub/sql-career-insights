# Top Paying Skills

## Project Overview
This project identifies the **skills associated with the highest average salaries for remote Data Analyst jobs**.  
It demonstrates how to aggregate salary data by skill and rank skills by average pay.

## Problem Statement
Which skills lead to the highest-paying remote Data Analyst positions?

## SQL Query Logic
1. **Joins**:
   - skills_job_dim maps jobs to skill IDs.  
   - skills_dim retrieves the skill names.  
2. **Filters**:
   - job_title_short = 'Data Analyst' → Focus on Data Analyst roles.  
   - salary_year_avg IS NOT NULL → Only include jobs with salary information.  
   - job_work_from_home = TRUE → Only remote jobs.  
3. **Aggregation**:
   - AVG(salary_year_avg) calculates the average salary for each skill.  
   - ROUND(..., 0) rounds the salary to the nearest integer.  
   - GROUP BY skills_dim.skills groups salaries by skill.  
4. **Ordering & Limiting**:
   - Ordered by avg_salary descending to identify top-paying skills.  
   - LIMIT 25 retrieves the 25 skills with the highest average salary.

## Skills Demonstrated
- SQL INNER JOINs  
- Filtering data with WHERE clauses  
- Aggregation using AVG and GROUP BY  
- Rounding numerical results  
- Ordering and limiting results  
- Analyzing skill-based salary trends
