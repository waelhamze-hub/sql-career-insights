# Optimal Skills

## Project Overview
This project identifies **optimal skills for remote Data Analyst roles**, combining both **demand** (how frequently a skill is required) and **average salary**.  
It demonstrates how to use SQL to combine multiple metrics and rank skills for career optimization.

## Problem Statement
Which skills are most in-demand and also offer the highest average salaries for remote Data Analyst positions?

## SQL Query Logic
1. **CTE skills_demand**:
   - Counts how many jobs require each skill (demand_count).  
   - Filters for Data Analyst roles, remote jobs, and jobs with salary info.  
2. **CTE average_salary**:
   - Calculates the average salary for each skill.  
   - Same filters applied as above.  
3. **Final Selection**:
   - Join skills_demand and average_salary on skill_id.  
   - Filter out skills with low demand (demand_count > 10).  
   - Order by avg_salary DESC and demand_count DESC.  
   - Limit results to top 25 skills.

## Skills Demonstrated
- SQL Common Table Expressions (CTE)  
- Aggregation with COUNT and AVG  
- INNER JOIN between aggregated results  
- Filtering and ordering results based on multiple metrics  
- Combining demand and salary insights to identify optimal skills
