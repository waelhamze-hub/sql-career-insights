# Top Demanded Skills

## Project Overview
This project identifies the **most in-demand skills for remote Data Analyst jobs**.  
It demonstrates how to use SQL to aggregate job postings by skill and rank them by frequency.

## Problem Statement
Which skills are most frequently required in remote Data Analyst job postings?

## SQL Query Logic
1. **Joins**:
   - skills_job_dim maps jobs to skill IDs.  
   - skills_dim retrieves the skill names.  
2. **Filters**:
   - job_title_short = 'Data Analyst' → Focus on Data Analyst roles.  
   - job_work_from_home = TRUE → Only include remote jobs.  
3. **Aggregation**:
   - COUNT(skills_job_dim.job_id) counts how many jobs require each skill.  
   - GROUP BY skills_dim.skills groups jobs by skill.  
4. **Ordering & Limiting**:
   - Ordered by demand_count descending.  
   - LIMIT 5 retrieves the top 5 most demanded skills.

## Skills Demonstrated
- SQL INNER JOINs across multiple tables  
- Filtering with WHERE clauses  
- Aggregation using COUNT and GROUP BY  
- Ordering and limiting results  
- Analyzing skill demand in job market data
