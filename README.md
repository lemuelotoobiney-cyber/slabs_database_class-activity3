AUTHOR: Lemuel Waye Otoo-Biney

1.Vertical vs. Horizontal Software
----------------------------------
* Vertical Software
  InDrive is an application that allows for drivers to transport 
  customers from their pickup location to destination under a fair price. This 
  software assist users within a specific industry in this case transport.

* Horizontal Software
  Microsoft Excel used for creating tables, doing calculations with formulas e.g
  calculating average of student marks and collecting data that can be used
  in many industries like school, hospitals, workplaces.This software has 
  general function and is used in multiple industries.

---------------------------------------------------------------------------------
2.Batch Processing and Real-Time Processing
--------------------------------------------
* Batch Processing:
  MTN/Vodacom Telecom billing in a phone network with a sim card processes every 
  customer’s call/ call history, SMS and data automatically collecting and
  processing the data in batches without user interaction.

* Real-Time Processing:
  Hospital life support machines or monitors that have systems that responds to a
  patient's heart rate immediately after the heart beats.This system mode responds
  to an event within a fixed time.



---------------------------------------------------------------------------------------
SQL QUERY
---------
postgres=# CREATE DATABASE company_db;
CREATE DATABASE
postgres=# \c company_db
You are now connected to database "company_db" as user "postgres".
company_db=# CREATE TABLE employees(
company_db(# employee_id SERIAL PRIMARY KEY,
company_db(# first_name VARCHAR(25) NOT NULL,
company_db(# last_name VARCHAR(25) NOT NULL,
company_db(# salary NUMERIC(10, 2)
company_db(# );
CREATE TABLE
company_db=# INSERT INTO employees(employee_id, first_name, last_name, salary) VALUES
company_db-# (001, 'Lemuel', 'Otoo-Biney', 15000);
INSERT 0 1
company_db=# INSERT INTO employees(employee_id, first_name, last_name, salary) VALUES
company_db-# (002, 'Bruce', 'Wayne', 22000);
INSERT 0 1
company_db=# INSERT INTO employees(employee_id, first_name, last_name, salary) VALUES
company_db-# (003, 'Clarke', 'Kent', 19000);
INSERT 0 1
company_db=# INSERT INTO employees(employee_id, first_name, last_name, salary) VALUES
company_db-# (004, 'John', 'Doe', 25000);
INSERT 0 1
company_db=# SELECT * FROM employees WHERE salary > 20000.00;
 employee_id | first_name | last_name |  salary
-------------+------------+-----------+----------
           2 | Bruce      | Wayne     | 22000.00
           4 | John       | Doe       | 25000.00
(2 rows)


company_db=# SELECT * FROM employees;
 employee_id | first_name | last_name  |  salary
-------------+------------+------------+----------
           1 | Lemuel     | Otoo-Biney | 15000.00
           2 | Bruce      | Wayne      | 22000.00
           3 | Clarke     | Kent       | 19000.00
           4 | John       | Doe        | 25000.00
(4 rows)


company_db=# UPDATE employees
company_db-# SET salary = 30000.00
company_db-# WHERE employee_id = 3;
UPDATE 1
company_db=# SELECT * FROM employees;
 employee_id | first_name | last_name  |  salary
-------------+------------+------------+----------
           1 | Lemuel     | Otoo-Biney | 15000.00
           2 | Bruce      | Wayne      | 22000.00
           4 | John       | Doe        | 25000.00
           3 | Clarke     | Kent       | 30000.00
(4 rows)


company_db=# DELETE FROM employees
company_db-# WHERE employee_id = 4;
DELETE 1
company_db=# SELECT * FROM employees;
 employee_id | first_name | last_name  |  salary
-------------+------------+------------+----------
           1 | Lemuel     | Otoo-Biney | 15000.00
           2 | Bruce      | Wayne      | 22000.00
           3 | Clarke     | Kent       | 30000.00
(3 rows)
