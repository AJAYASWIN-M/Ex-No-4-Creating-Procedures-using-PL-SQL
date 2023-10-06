# Ex. No: 4 Creating Procedures using PL/SQL

### AIM: To create a procedure using PL/SQL.

### Steps:
1. Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
2. Create a procedure named as insert_employee data.
3. Inside the procdure block, write the query for inserting the values into the employee table.
4. End the procedure.
5. Call the insert_employee data procedure to insert the values into the employee table.
6. Display the employee table

### Program:
```sql
SQL> CREATE TABLE emp(empid number, empname varchar(10), dept varchar(10),salary number);
Table created.
SQL> CREATE OR REPLACE PROCEDURE insert_employee_data AS
  2  BEGIN
  3  INSERT INTO emp(empid, empname, dept, salary)
  4  values(1,'ajay','IT',100000);
  5  INSERT INTO emp(empid, empname, dept, salary)
  6  values(2,'aswin','HR',600000);
  7  INSERT INTO emp(empid, empname, dept, salary)
  8  values((3,'ajayaswin','seo',500000);
  9  COMMIT;
 10  FOR emp_rec IN (SELECT * FROM emp)LOOP
 11  DBMS_OUTPUT.PUT_LINE('EMPLOYEE ID:' || emp_rec.empid || ',EMPLOYEE NAME:' || emp_rec.empname || ',DEPARTMENT:'|| emp_rec.dept || ',SALARY:' || emp_rec.salary);
 12  END LOOP;
 13  END;
 14  /
Procedure created.
```
### Output:

![ex 4 dbms 2](https://github.com/AJAYASWIN-M/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/118679692/af0c23ab-bf44-40f0-bf35-6e6fdc865ec2)
![ex 4 dbms 1](https://github.com/AJAYASWIN-M/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/118679692/e2933a1a-d589-40c7-a18c-5b6b10fc8c0e)


![ex 4 dbms](https://github.com/AJAYASWIN-M/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/118679692/793de69d-44f8-42bc-873b-88f254d0891b)


### Result:
The program has been implemented successfully.
