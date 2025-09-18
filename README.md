# HR Management Analytics – Power BI Dashboard  

## Overview  
This project delivers an interactive **HR Management Analytics Dashboard** developed in Power BI. It provides a comprehensive view of workforce dynamics, helping HR managers and executives monitor headcount, hiring, turnover, retention and diversity.

## Objectives  
The goal of this dashboard is to enable **data-driven HR decision-making** by:  
- Tracking **headcount trends** and distribution  
- Monitoring **new hires** and **terminations** over time  
- Measuring **turnover** and **retention rates** by department, job level, and demographic segments  
- Analyzing **workforce diversity** (gender, marital status, ethnicity, education)  
- Visualizing **geographic distribution** of employees  
- Understanding **salary costs and distribution**  

## Data Sources  
- **people_employment_history.csv** – Job history, hire date, termination date, salary, job level  
- **people_data.csv** – Demographics (gender, race, education, marital status, location, work mode)  
- **Dates Table** – Custom DAX-generated date table to enable time intelligence (year, month, etc.)  

## Data Modeling  
The Power BI data model is designed as a **star schema**, featuring:  
- Two date relationships (hire date and termination date) managed with `USERELATIONSHIP`  
- Calculated columns for **Age**, **Age Buckets**, and **Experience Buckets** (Junior, Mid-level, Senior)  
- Key DAX measures:  
  - `New Hires`, `Terminations`, `Active Employees`  
  - `Turnover Rate`, `Retention Rate`  
  - `Total Cost`, `Min Salary`, `Max Salary`, `Average Salary` (filtered by active employees)  

## Key Visuals  
The dashboard is structured into three pages:  

**1. Workforce Overview**  
- Headcount by department, job level, city, gender, marital status, age group, education, and ethnicity  
- KPI card with total headcount  
- US map showing employee distribution  

**2. Retention Analysis**  
- KPIs: Starting headcount, Ending headcount, Retention %  
- Retention by Job Level, Department, Age Group  
- Retention trend over time  

**3. Turnover Analysis**  
- KPIs: New hires, Terminations, Turnover rate  
- Terminations by Department, Job Level, Age Group  
- Turnover trend over time  

## Tools & Technologies  
- **Power BI Desktop** – Dashboard design, data modeling  
- **DAX** – Calculated measures, relationships, filters  
- **Star Schema Design** – Clean, scalable data model  

## Insights  
- Clear understanding of workforce composition and diversity  
- Identification of departments and job levels with higher turnover  
- Visibility into retention performance and historical trends  
- Insight into salary distribution and cost evolution  

## How to Use  
1. Clone or download the repository  
2. Open the `.pbix` file in Power BI Desktop  
3. Refresh the data (if connected to live source)  
4. Use slicers (Year, Department) to filter data dynamically  

## Future Enhancements  
- Add **predictive analytics** to forecast turnover and hiring needs  
- Include **engagement survey data** for deeper HR insights  
- Automate data refresh with scheduled Power BI service updates  
