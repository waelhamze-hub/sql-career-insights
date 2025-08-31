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

### Sample Rows  
company_id | name | link | link_google | thumbnail
0 | Cryptology | NULL | https://www.google.com/
... | https://encrypted-tbn0
...
1 | Edraak | NULL | https://www.google.com/
... | https://encrypted-tbn0
...
2 | Groupe ADP | http://www.groupeadp.fr/
 | https://www.google.com/
... | https://encrypted-tbn0
...
