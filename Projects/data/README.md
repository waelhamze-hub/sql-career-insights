# Data Folder Overview

The /data folder contains all dataset files used in this SQL project. These files include **dimension tables, fact tables, and bridge tables** that together form a simplified data warehouse schema for analyzing job postings, companies, and required skills.  

Each dataset is documented with a short description, schema, and sample rows to provide quick reference and facilitate integration in SQL queries.  

### Included Data Files  

- company_dim.csv – Dimension table containing company information.  
- job_postings_fact.csv – Fact table with detailed job posting data.  
- skills_dim.csv – Dimension table containing standardized skill information.  
- skills_job_dim.csv – Bridge table linking job postings with required skills.  

This README provides an overview and sample data for each file, helping users understand how the datasets relate to one another and can be used in analysis.

---

## Data: company_dim.csv

The data/company_dim.csv file is a **dimension table** used in this SQL project.  
It contains reference information about companies such as their IDs, names, official websites, Google search links, and thumbnail images.  

### Schema  
| Column        | Description                                      |
|---------------|--------------------------------------------------|
| company_id  | Unique identifier for each company               |
| name        | Company name                                     |
| link        | Official company website (if available)          |
| link_google | Direct Google search link for the company        |
| thumbnail   | Company thumbnail image (Google-hosted preview)  |


---

## Data: `job_postings_fact.csv`

The `data/job_postings_fact.csv` file is a **fact table** that contains detailed information about job postings.  
It includes attributes such as job title, location, source platform, schedule type, remote option, posting date, and salary details.  
This dataset can be joined with dimension tables (e.g., `company_dim.csv`) using `company_id`.  

### Schema  
| Column                | Description                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| `job_id`              | Unique identifier for the job posting                                       |
| `company_id`          | Foreign key referencing the company (from `company_dim.csv`)                |
| `job_title_short`     | Standardized short form of the job title (e.g., "Data Analyst")             |
| `job_title`           | Full job title as listed in the posting                                     |
| `job_location`        | Location of the job posting                                                 |
| `job_via`             | Source platform (e.g., LinkedIn, Trabajo.org)                              |
| `job_schedule_type`   | Type of employment (e.g., Full-time, Contractor)                            |
| `job_work_from_home`  | Boolean indicating if the role is remote                                    |
| `search_location`     | Standardized search location used in data collection                        |
| `job_posted_date`     | Date and time the job was posted                                            |
| `job_no_degree_mention` | Boolean indicating if no degree requirement is mentioned                  |
| `job_health_insurance` | Boolean indicating if health insurance is mentioned                        |
| `job_country`         | Country where the job is located                                            |
| `salary_rate`         | Salary rate type (e.g., yearly, hourly)                                     |
| `salary_year_avg`     | Average yearly salary (if provided)                                         |
| `salary_hour_avg`     | Average hourly salary (if provided)                                         |



