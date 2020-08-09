# Pewlett-Hackard-Analysis
The assignment consists of three parts: two additional analyses and a technical report to deliver the results to his manager. To help him complete these tasks, you will submit the following deliverables:

* Technical Analysis Deliverable 1: Number of Retiring Employees by Title. You will create three new tables, one showing number of [titles] retiring, one showing number of employees with each title, and one showing a list of current employees born between Jan. 1, 1952 and Dec. 31, 1955. New tables are exported as CSVs. 

* Technical Analysis Deliverable 2: Mentorship Eligibility. A table containing employees who are eligible for the mentorship program You will submit your table and the CSV containing the data (and the CSV containing the data)

## Resources
Data Source: departments.csv, employees.csv, dept_emp.csv, dept_manager.csv, salaries.csv and titles.csv
Software: PostgreSQL11.8 (pgAdmin 4.23)

## Summary
* Summary of queries created for the project: https://github.com/Mar102/Pewlett-Hackard-Analysis/blob/master/queries.sql

* Created a ERD diagram to guide the completion of deliverables.
![](https://github.com/Mar102/Pewlett-Hackard-Analysis/blob/master/EmployeeDB.png)

* Task description, Deliverable 1: I created a table containing the number of employees who are about to retire (those born 1952-1955), grouped by job title. I used an inner join to connect the previously created tables-- Current Employees, Titles and Salary --

