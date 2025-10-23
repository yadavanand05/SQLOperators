# SQLOperators
# Employee-Performance-and-Bonus-Evaluation-System

##Case Study Background

A company, Tech Mahindra Solutions, maintains an employee database to calculate employee bonuses based on their salary, performance score, and department. The HR department wants to analyze which employees are eligible for a performance bonus, salary comparisons between employees, and logical decisions based on performance and department criteria. Your task is to write SQL queries using arithmetic, comparison, and logical operators to support these requirements.


CREATE TABLE empolye(
empolyee_id INT PRIMARY KEY, 
FIRST_NAME VARCHAR(50) NOT NULL,
LAST_NAME VARCHAR(50) NOT NULL,
EMAIL VARCHAR(50),
DEPARTMENT VARCHAR(30),
SALARY NUMERIC(15,4),
JOINING_DATE DATE,
AGE INT
);

select * from  employe

QUE 1 ---10% bonus from employe
select first_name,salary,
(salary*0.10) AS bonus from employe;

QUE 2 ----new salary
select * from employe
SELECT first_name,last_name,salary,
(salary*12) AS annual_salary,
(salary*0.5)AS totale_salary,
(salary*1.5)AS new_salary,
(salary+salary*0.5)AS new_salary2;

QUE 3 --FINDE EMPLOYE WHOSE AGE IS EXACTLY 30.
select * from employe
WHERE age =30;

QUE 4 ---FIND EMPLOYE WHOSE AGE IS NOT 25.
SELECT * FROM employe
WHERE age <>25;

QUE 5 --find whose age is above 40.
select * from employe 
where age >40;

QUE 6 --find whose salary is more than 70,000.
select * from employe
where salary >70000;

QUE 7 --find whose age is more than 70,000.
select * from employe
where age <30;

QUE 8 --find whose salary is less then 40,000.
select * from employe
where salary < 40000;

QUE 9 --find whose age is 35 or older (>=).
select * from employe 
where age >= 35;

QUE 10 --find ehose salary is 60000(>=).
select * from employe
where salary >=60000;

QUE 11 --find whose salary is 50000 or less (<=).
select * from employe 
where salary <= 50000;

QUE 12 --find whose age age is 28 or below (<=0)
select * from employe
where age <= 28;

QUE 13 --find whose age is greater than 25 and salary is greater than 50,000.
select * from employe
where age >25 and salary> 50000;

QUE 14 --find who are in the 'it'depasrtment and earn more than 70000.
select * from employe
where department = 'it' and salary > 70000;

QUE 15 --find whose age is less than 25 or salary is less than 40000
select * from employe
where age <25 or salary<40000;

QUE 16 --find who atre in 'hr'or 'finance'department.
select * from employe
where department ='hr'or department = 'finance';

QUE 17 --find not in the 'it' department.
select * from employe
where not department = 'it';

QUE 18 --whose age is not 30.
select * from employe
where not age = 30;


