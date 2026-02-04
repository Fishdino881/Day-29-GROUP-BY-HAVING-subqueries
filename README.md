# Day-29-GROUP-BY-HAVING-subqueries

Overview

On Day 29, I practiced advanced SQL querying techniques used for aggregation, filtering grouped data, and nested queries. These concepts are essential for analytics, reporting, and complex data analysis.

Topics Covered

1. GROUP BY
Used to group rows that share the same values and apply aggregate functions.

SELECT department, COUNT(*) AS total_employees
FROM employees
GROUP BY department;

Common aggregate functions:
	•	COUNT()
	•	SUM()
	•	AVG()
	•	MIN()
	•	MAX()


2. HAVING
Used to filter results after grouping (works with aggregate functions).

SELECT department, AVG(salary) AS avg_salary
FROM employees
GROUP BY department
HAVING AVG(salary) > 60000;

Difference:
	•	WHERE → filters rows
	•	HAVING → filters groups


3. Subqueries
A query written inside another query.

SELECT name, salary
FROM employees
WHERE salary > (
    SELECT AVG(salary)
    FROM employees
);

Subqueries help break complex logic into smaller, readable queries.


Learning Outcome

Learned how to summarize data using GROUP BY
Understood filtering aggregated data with HAVING
Gained confidence using subqueries for complex conditions
