# Top Paying Job Skills

## Project Overview
This project identifies the **skills associated with the top-paying Data Analyst jobs** available remotely.  
It builds on the previous query for top-paying jobs and joins with skill tables to analyze which skills contribute to high-paying roles.

## Problem Statement
Which skills are associated with the highest-paying Data Analyst jobs for remote positions?

## SQL Query Logic
1. **Common Table Expression (CTE) `top_paying_jobs`**:
   - Selects the top 10 Data Analyst jobs with the highest annual salary and location "Anywhere".  
   - Includes job ID, job title, salary, and company name.  
2. **Join with skill tables**:
   - `skills_job_dim` maps jobs to skill IDs.  
   - `skills_dim` retrieves the skill names.  
3. **Final Output**:
   - Lists each top-paying job along with its associated skills.  
   - Ordered by salary descending.

## Skills Demonstrated
- SQL Common Table Expressions (CTE)  
- INNER JOINs across multiple tables  
- Filtering and ordering data  
- Combining job and skill information for analysis
