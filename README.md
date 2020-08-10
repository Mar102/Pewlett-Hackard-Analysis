# Pewlett-Hackard-Analysis
The assignment consists of three parts: two additional analyses and a technical report to deliver the results to his manager. To help him complete these tasks, you will submit the following deliverables:

* Technical Analysis Deliverable 1: Number of retiring employees by itle. You will create three new tables, one showing number of [titles] retiring, one showing number of employees with each title, and one showing a list of current employees born between Jan. 1, 1952 and Dec. 31, 1955. New tables are exported as CSVs. 

* Technical Analysis Deliverable 2: Mentorship Eligibility. A table containing employees who are eligible for the mentorship program You will submit your table and the CSV containing the data (and the CSV containing the data)

## Resources
Data Source: departments.csv, employees.csv, dept_emp.csv, dept_manager.csv, salaries.csv and titles.csv
Software: PostgreSQL11.8 (pgAdmin 4.23)

## Summary
Summary of queries created for the project: https://github.com/Mar102/Pewlett-Hackard-Analysis/blob/master/queries.sql

Created a ERD diagram to guide the completion of deliverables.
![](https://github.com/Mar102/Pewlett-Hackard-Analysis/blob/master/EmployeeDB.png)

Task description, Deliverable 1: I created a table containing the number of employees who are about to retire (those born 1952-1955). I used an inner join to connect the previously created tables-- Current Employees, Titles and Salary -- to pull only the matching items between all values within the tables. After exporting it to a CSV file, retiring_byTitle.csv, the able contained the following information:
- Employee number
- First and last name
- Title
- from_date
- Salary

After noticing substantial duplicates in the data, I created a new table that includes only the most recent title of each employee, no duplicates. The duplicated items were assessed using partitions in data and saved under a new CSV file titled, "retiring_noDup.csv" The partition decreased the data from 54,722 to 33,118 values.

Then, I created another table to group my non-duplicated data by titles.
![](https://github.com/Mar102/Pewlett-Hackard-Analysis/blob/master/EmployeesRetiringbyTitle.png)

Task description, Deliverable 2: Created a new table, exported as "mentorship_eligibility.csv," to hold employees eligible to participate in mentorship programs. I once more used inner joins to only capture matching values between my employee, titles and department employee tables. The final table contains the following data points:
* Employee number
* First and last name
* Title
* from_date and to_date

I once more checked for duplicates and cleaned the data to only keep the most current positions for employees(mentorship_eligibility_noDup.csv).

Lastly, I grouped the data by title for easier comparison. 
![](https://github.com/Mar102/Pewlett-Hackard-Analysis/blob/master/Mentorship_byTitle.png)


