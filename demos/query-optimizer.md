# Query Optimization Engine

Diagnose slow queries with Visual Explain and the optimizer workbench — index suggestions, plan scoring, and optional batch review.

<p align="center">
  <img src="../media/gifs/query-optimizer-workbench-demo.gif" alt="Query Optimizer workbench" width="720" />
</p>

## Key capabilities

- Interactive **execution plan** tree with cost highlights  
- **Index recommendations** tied to real statistics  
- **Before / after** comparison when trying rewrites on a dev instance  
- **Batch optimize** for multiple statements from slow-query analysis  

## Demo walkthrough

1. Open a slow `SELECT` on representative data (multi-table join recommended).  
2. Launch the **Query Optimizer** workbench from CodeLens or the Command Palette.  
3. Walk through the plan tree: scans, row estimates, and highest-cost steps.  
4. Apply a suggested index on a non-production database and re-run `EXPLAIN`.  

## Visual Explain

<p align="center">
  <img src="../media/gifs/query-optimizer-visual-explain-demo.gif" alt="Visual Explain" width="720" />
</p>

## Example query

```sql
SELECT e.first_name, e.last_name, s.salary
FROM employees e
JOIN salaries s ON s.emp_no = e.emp_no AND s.to_date = '9999-01-01'
WHERE s.salary > (
  SELECT AVG(salary) FROM salaries WHERE to_date = '9999-01-01'
)
ORDER BY s.salary DESC
LIMIT 20;
```

<p align="center"><a href="README.md">← All demo guides</a></p>
