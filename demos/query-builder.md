# Visual Query Builder

Build complex SQL in the editor by dragging tables and columns from your connection tree. SQLLens infers JOINs from foreign keys, adapts to the active SQL clause, and supports keyboard shortcuts before each drop.

<p align="center">
  <img src="../media/gifs/query-builder-landing-demo.gif" alt="Visual Query Builder" width="720" />
</p>

## Key capabilities

- Drag **tables** to start `SELECT`, `UPDATE`, `DELETE`, or `INSERT` statements  
- Add **JOINs** with type shortcuts (`LJ`, `RJ`, `IJ`, …) before dropping the next table  
- Drop **columns** into `SELECT`, `WHERE`, `JOIN … ON`, `GROUP BY`, `ORDER BY`, and more  
- Resolve ambiguous relationship paths with explicit prompts instead of silent guesses  

## Demo walkthrough

1. Connect to a database and open a new `.sql` file bound to that schema.  
2. Drag the **employees** table onto an empty line to seed a `SELECT`.  
3. Type `LJ` and drag **dept_emp**, then **departments**, to build a multi-table join.  
4. Drag columns into `GROUP BY` and `ORDER BY` to finish an aggregate report.  

## Example outcome

```sql
SELECT d.dept_name, COUNT(*) AS headcount
FROM employees e
JOIN dept_emp de ON de.emp_no = e.emp_no AND de.to_date = '9999-01-01'
JOIN departments d ON d.dept_no = de.dept_no
GROUP BY d.dept_name
ORDER BY headcount DESC;
```

<p align="center"><a href="README.md">← All demo guides</a></p>
