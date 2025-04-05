# Hands-on Lab: String Patterns, Sorting and Grouping in MySQL

**Estimated Time Needed:** 30 minutes

In this lab, you will learn how to create tables and load data in the **MySQL** database service using the **phpMyAdmin** graphical user interface (GUI) tool.

---

## **Objectives**

After completing this lab, you will be able to:

- **Filter** the output of a `SELECT` query using string patterns, ranges, or sets of values.  
- **Sort** the result set in ascending or descending order based on a specified column.  
- **Group** query outcomes based on a selected parameter for refined data analysis.

---

## **Software Used**

You will use:

- **MySQL** – A Relational Database Management System (RDBMS) used to store, manipulate, and retrieve data.  
- **SN Labs Cloud IDE** – A virtual lab environment provided as part of IBM Skills Network.

---

## **Database Used**

The database is a sample **HR** database with 5 tables:

- **EMPLOYEES**
- **JOB_HISTORY**
- **JOBS**
- **DEPARTMENTS**
- **LOCATIONS**

Each table includes a few rows of sample data.

---

## **Load the Database**

1. Open **phpMyAdmin** from the Skills Network Toolbox in Cloud IDE.  
2. Create a blank database named `HR`. Use the provided `Script_Create_Tables.sql` to create tables.  
3. Download the following CSV files if not already downloaded:
   - `Departments.csv`
   - `Jobs.csv`
   - `JobsHistory.csv`
   - `Locations.csv`
   - `Employees.csv`  
4. Import each CSV file into its respective table in the `HR` database.

---

## **String Patterns**

You can use string patterns to filter query results using the `LIKE` operator.

```sql
SELECT F_NAME, L_NAME
FROM EMPLOYEES
WHERE ADDRESS LIKE '%Elgin,IL%';
