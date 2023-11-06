# Ex. No: 4 Creating Procedures using PL/SQL

### AIM: To create a procedure using PL/SQL.

### DATE:


### Steps:
1. Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
2. Create a procedure named as insert_employee data.
3. Inside the procdure block, write the query for inserting the values into the employee table.
4. End the procedure.
5. Call the insert_employee data procedure to insert the values into the employee table.
6. Display the employee table

### Program:
```
name :THANJIYAPPAN K
REG NO:212222240108
```
```
SQL> CREATE TABLE e(
     empid NUMBER,
     empname VARCHAR(10),
     dept VARCHAR(10),
     salary NUMBER
    );
CREATE OR REPLACE PROCEDURE emp_data AS
    BEGIN
    INSERT INTO e(empid,empname,dept,salary)
    values(1,'THANJI','AIDS',100000);
    INSERT INTO e(empid,empname,dept,salary)
    values(2,'VINOD','AIML',100000);
    INSERT INTO e(empid,empname,dept,salary)
    values(3,'ARVIND','AIML',100000);
    COMMIT;
   FOR emp_rec IN (SELECT * FROM e)LOOP
   DBMS_OUTPUT.PUT_LINE('EMPLOYEE ID:'||emp_rec.empid||',EMPLOYEE NAME:'|| emp_rec.empname||
   ',DEPARTMENT:'||emp_rec.dept||',SALARY:'||emp_rec.salary);
   END LOOP;
   END;
  /
```
### Output:
![image](https://github.com/22009011/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/118343461/b14071bc-f168-4d25-b091-60ab8e129f07)

### Result:
The procedures has been successfully created using PL\SQL
