# Ex-4-Creating-Procedures-using-PL-SQL

# DATE:25.9.2023

# AIM: To create a procedure using PL/SQL.

# Steps:

   1. Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
   2. Create a procedure named as insert_employee data.
   3. Inside the procdure block, write the query for inserting the values into the employee table.
   4. End the procedure.
   5. Call the insert_employee data procedure to insert the values into the employee table.
   6. Display the employee table

# Program:
```
SQL> CREATE TABLE ep(
     empid NUMBER,
     empname VARCHAR(10),
     dept VARCHAR(10),
     salary NUMBER
    );
CREATE OR REPLACE PROCEDURE emp_data AS
    BEGIN
    INSERT INTO ep(empid,empname,dept,salary)
    values(1,'SHAKTHI','MD',10000000);
    INSERT INTO ep(empid,empname,dept,salary)
    values(2,'ARUN','HR',500000);
    INSERT INTO ep(empid,empname,dept,salary)
    values(3,'DHANUSH','IT',200000);
    COMMIT;
   FOR emp_rec IN (SELECT * FROM ep)LOOP
   DBMS_OUTPUT.PUT_LINE('EMPLOYEE ID:'||emp_rec.empid||',EMPLOYEE NAME:'|| emp_rec.empname||
   ',DEPARTMENT:'||emp_rec.dept||',SALARY:'||emp_rec.salary);
   END LOOP;
   END;
  /
```

# Output:

![270758399-50848e70-e38e-44fe-84d2-7f6e92d05db9](https://github.com/prithviraj5703/Ex-4-Creating-Procedures-using-PL-SQL/assets/121418418/dd186a1e-2624-42db-a882-2a096e13d3f0)


# Result:
THE PROGRAM HAS BEEN IMPLEMENTED SUCCESSFULLY
