# Query Builder demo

**Audience:** Sales, solutions engineering, onboarding.  
**Product:** Schema-driven query assembly in the **SQL editor** — drag tables and columns from the connection tree, use inline shortcuts before a drop, and get **foreign-key-aware JOIN** suggestions.

![Query Builder landing demo](../media/gifs/query-builder-landing-demo.gif)

## Value proposition

- **Speed** — Assemble `SELECT` / `UPDATE` / `DELETE` / `INSERT` without retyping object names.  
- **Correctness** — JOIN conditions from cached FK metadata, including bridge tables and multiple paths (with disambiguation when needed).  
- **Context-aware columns** — Drops respect cursor clause: `WHERE`, `SELECT`, `JOIN … ON`, `ORDER BY`, `GROUP BY`, `HAVING`, `SET`.  
- **Keyboard rhythm** — Short tokens typed **before** dragging (`s`, `LJ`, `W`, …) expand into patterns; the drag fills in tables or columns.

## Feature checklist

| # | Feature | User action |
|---|---------|-------------|
| 1 | New query from table | Drag a **table** onto an empty or valid line |
| 2 | JOIN expansion | Drag a second table when a `SELECT` is in scope |
| 3 | JOIN shortcuts | Type `IJ`, `LJ`, `RJ`, `FJ`, `CJ` before drag |
| 4 | Clause-aware column drop | Drag **column** with cursor in `SELECT` / `WHERE` / `ON` / etc. |
| 5 | DML shortcuts | `s`/`sel` → SELECT; `u` → UPDATE; `d` → DELETE; `i` → INSERT |
| 6 | WHERE helpers | `W`, `WL`/`WLIKE`, `WIN`, `WB`/`WBET`, `WN`/`WNULL`, … |
| 7 | ORDER / GROUP / HAVING | `OA`/`ORDER`, `GROUP`, `HAVING` + column drag |
| 8 | Aggregates | `COUNT`, `SUM`, `AVG`, … + column |
| 9 | Connection alignment | Active connection + database match the editor |

## Demo scenario 1 — Headcount by department

Target SQL (narrate: shortcut → drag `employees` → drag `dept_emp` → drag `departments` → GROUP BY drops):

```sql
SELECT d.dept_name, COUNT(*) AS headcount
FROM employees e
JOIN dept_emp de ON de.emp_no = e.emp_no AND de.to_date = '9999-01-01'
JOIN departments d ON d.dept_no = de.dept_no
GROUP BY d.dept_name
ORDER BY headcount DESC;
```

## Demo scenario 2 — Average salary by department

```sql
SELECT d.dept_name, ROUND(AVG(s.salary), 2) AS avg_salary
FROM salaries s
JOIN employees e ON e.emp_no = s.emp_no
JOIN dept_emp de ON de.emp_no = e.emp_no AND de.to_date = '9999-01-01'
JOIN departments d ON d.dept_no = de.dept_no
WHERE s.to_date = '9999-01-01'
GROUP BY d.dept_name
ORDER BY avg_salary DESC;
```

## Optional highlight reel

![Query Builder highlight](../media/gifs/query-builder-highlight-demo.gif)

## Talk-track tips

- If JOIN disambiguation appears, frame it positively: *multiple FK paths — the tool asks you to choose instead of guessing wrong.*  
- Pair with **Query Optimizer** when the assembled query is slow on realistic row counts.

## Related demos

- [SQL workspace](sql-workspace.md)  
- [Query Optimizer](query-optimizer.md)  
- [Demo catalog](README.md)
