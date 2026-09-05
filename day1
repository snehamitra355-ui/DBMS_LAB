
-- Question 1
-- Display the data in the existing EMP table.
---------------------------------------------------------
SELECT * FROM EMP;

---------------------------------------------------------
-- Question 2
-- Display the structure of the EMP table.
---------------------------------------------------------
DESC EMP;

---------------------------------------------------------
-- Question 3
-- Create Student table.
---------------------------------------------------------
CREATE TABLE Student (
    Roll NUMBER(5),
    Name VARCHAR2(30),
    Age NUMBER(5),
    Course VARCHAR2(5),
    Math NUMBER(6,2),
    Physics NUMBER(6,2),
    Computer NUMBER(6,2),
    Birthday DATE
);

---------------------------------------------------------
-- Question 4
-- Create MSc table from Student with same structure.
---------------------------------------------------------
CREATE TABLE MSc AS
SELECT *
FROM Student
WHERE 1=2;

---------------------------------------------------------
-- Question 5
-- Display the structure of MSc table.
---------------------------------------------------------
DESC MSc;

---------------------------------------------------------
-- Question 6
-- Create MCA table with renamed columns.
---------------------------------------------------------
CREATE TABLE MCA AS
SELECT
    Roll,
    Name AS First_Name,
    Age,
    Course AS Department,
    Math,
    Physics,
    Computer,
    Birthday
FROM Student
WHERE 1=2;

---------------------------------------------------------
-- Question 7
-- Display the structure of MCA table.
---------------------------------------------------------
DESC MCA;

---------------------------------------------------------
-- Question 8
-- Insert records into Student table.
---------------------------------------------------------
INSERT INTO Student VALUES
(1,'Rahul',19,'BCA',79,67,89,TO_DATE('15-JUN-93','DD-MON-YY'));

INSERT INTO Student VALUES
(2,'Kunal',21,'BCA',68,76,59,TO_DATE('16-AUG-91','DD-MON-YY'));

INSERT INTO Student VALUES
(3,'Aditi',20,'MSc',90,73,56,TO_DATE('20-SEP-92','DD-MON-YY'));

INSERT INTO Student VALUES
(4,'Sumit',20,'MCA',57.5,78,81,TO_DATE('07-DEC-91','DD-MON-YY'));

INSERT INTO Student VALUES
(5,'Anirban',22,'MCA',80,68,63,TO_DATE('15-SEP-94','DD-MON-YY'));

INSERT INTO Student VALUES
(6,'Kumkum',21,'BCA',72,54.5,60,TO_DATE('08-FEB-95','DD-MON-YY'));

INSERT INTO Student VALUES
(7,'Suman',21,'BCA',91.5,32,61,TO_DATE('10-MAR-94','DD-MON-YY'));

INSERT INTO Student VALUES
(8,'Rohit',22,'MSc',85,76,92,TO_DATE('19-APR-92','DD-MON-YY'));

COMMIT;

---------------------------------------------------------
-- Question 9
-- Display all student details.
---------------------------------------------------------
SELECT * FROM Student;

---------------------------------------------------------
-- Question 10
-- Display details of Roll No. 5.
---------------------------------------------------------
SELECT *
FROM Student
WHERE Roll = 5;

---------------------------------------------------------
-- Question 11
-- Display Roll, Name and marks of all subjects.
---------------------------------------------------------
SELECT
    Roll,
    Name,
    Math,
    Physics,
    Computer
FROM Student;

---------------------------------------------------------
-- Question 12
-- Display students belonging to BCA department.
---------------------------------------------------------
SELECT *
FROM Student
WHERE Course='BCA';

---------------------------------------------------------
-- Question 13
-- Insert MCA students into MCA table.
---------------------------------------------------------
INSERT INTO MCA
SELECT
    Roll,
    Name,
    Age,
    Course,
    Math,
    Physics,
    Computer,
    Birthday
FROM Student
WHERE Course='MCA';

COMMIT;

---------------------------------------------------------
-- Question 14
-- Insert MSc students into MSc table.
---------------------------------------------------------
INSERT INTO MSc
SELECT *
FROM Student
WHERE Course='MSc';

COMMIT;

---------------------------------------------------------
-- Question 15
-- Display structure of Student and MCA tables.
---------------------------------------------------------
DESC Student;

DESC MCA;

---------------------------------------------------------
-- Question 16
-- Display details with Course appearing first.
---------------------------------------------------------
SELECT
    Course,
    Roll,
    Name,
    Age,
    Math,
    Physics,
    Computer,
    Birthday
FROM Student;

---------------------------------------------------------
-- Question 17
-- Update Math marks of Roll No. 7 from 91.5 to 95.
---------------------------------------------------------
UPDATE Student
SET Math = 95
WHERE Roll = 7;

COMMIT;

---------------------------------------------------------
-- Question 18
-- Update name of Roll No. 4 in MCA table.
---------------------------------------------------------
UPDATE MCA
SET First_Name='Sumitava'
WHERE Roll=4;

COMMIT;

---------------------------------------------------------
-- Question 19
-- Delete student with Roll No. 2.
---------------------------------------------------------
DELETE FROM Student
WHERE Roll=2;

COMMIT;

---------------------------------------------------------
-- Question 20
-- Delete all students from Student table.
---------------------------------------------------------
DELETE FROM Student;

COMMIT;
