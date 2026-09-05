-- =========================================
-- ASGN 1: Create EMP1 table
-- =========================================

CREATE TABLE EMP1 (
    id NUMBER(2),
    name VARCHAR2(10),
    basic NUMBER(6,2),
    designation VARCHAR2(10),
    age NUMBER(2)
);


-- =========================================
-- ASGN 2: Modify BASIC column
-- =========================================

ALTER TABLE EMP1
MODIFY (basic NUMBER(2));


-- =========================================
-- ASGN 3: Increase NAME size
-- =========================================

ALTER TABLE EMP1
MODIFY (name VARCHAR2(15));


-- =========================================
-- ASGN 4: Create EMP_TRAINEE table
-- =========================================

CREATE TABLE EMP_TRAINEE AS
SELECT
    id AS emp_id,
    name,
    basic,
    designation,
    age
FROM EMP1
WHERE 1 = 0;


-- =========================================
-- ASGN 5: Insert records into EMP1
-- =========================================

INSERT INTO EMP1(id, name, basic, designation, age)
VALUES (1, 'Rohit', 6700, 'Manager', 24);

INSERT INTO EMP1(id, name, basic, designation, age)
VALUES (2, 'Sunil', 6200, 'Engineer', 27);

INSERT INTO EMP1(id, name, basic, designation, age)
VALUES (3, 'Payal', 6300, 'Engineer', 25);

INSERT INTO EMP1(id, name, basic, designation, age)
VALUES (4, 'Kunal', 6700, 'Trainee', 28);

INSERT INTO EMP1(id, name, basic, designation, age)
VALUES (5, 'Sunita', 6230, 'Trainee', 26);

INSERT INTO EMP1(id, name, basic, designation, age)
VALUES (6, 'Bimal', 7000, 'Trainee', 25);

COMMIT;


-- =========================================
-- ASGN 6: Insert trainees into EMP_TRAINEE
-- =========================================

INSERT INTO EMP_TRAINEE
SELECT *
FROM EMP1
WHERE designation = 'Trainee';


-- =========================================
-- ASGN 7: Add SKILLS and DOJ columns
-- =========================================

ALTER TABLE EMP1
ADD (
    skills VARCHAR2(10),
    doj DATE
);


-- =========================================
-- ASGN 8: Update skills for trainees
-- =========================================

UPDATE EMP1
SET skills = 'Java'
WHERE designation = 'Trainee';


-- =========================================
-- ASGN 9: Rename AGE column
-- =========================================

ALTER TABLE EMP1
RENAME COLUMN age TO age_in_years;


-- =========================================
-- ASGN 10: Drop AGE column from EMP_TRAINEE
-- =========================================

ALTER TABLE EMP_TRAINEE
DROP COLUMN Age;


-- =========================================
-- ASGN 11: Rename EMP1 table
-- =========================================

ALTER TABLE EMP1
RENAME TO EMP_MGR_ENGR;


-- =========================================
-- ASGN 12: Remove all records from table
-- =========================================

TRUNCATE TABLE EMP_MGR_ENGR;
