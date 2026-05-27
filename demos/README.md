# Product demos

Markdown scripts for sales, solutions engineering, and customer walkthroughs.  
Each page links to GIFs in [`../media/gifs/`](../media/gifs/).

## Demo catalog

| Demo | Guide | GIF(s) |
|------|-------|--------|
| SQL workspace & connect | [sql-workspace.md](sql-workspace.md) | `sql-workspace-overview-demo.gif`, `sql-workspace-run-demo.gif` |
| Query Builder | [query-builder.md](query-builder.md) | `query-builder-landing-demo.gif`, `query-builder-highlight-demo.gif` |
| Query Optimizer (QO) | [query-optimizer.md](query-optimizer.md) | `query-optimizer-visual-explain-demo.gif`, `query-optimizer-workbench-demo.gif` |
| Performance Monitor (PM) | [performance-monitor.md](performance-monitor.md) | `performance-monitor-open-demo.gif`, `performance-monitor-tour-demo.gif` |
| Query Profiler | [query-profiler.md](query-profiler.md) | `query-profiler-demo.gif` |
| AI & LLM integration | [ai-integration.md](ai-integration.md) | `ai-integration-demo.gif`, `ai-integration-demo-v4.gif` |

## Suggested demo order (30–45 min)

1. Connect and open the sidebar — [sql-workspace.md](sql-workspace.md)  
2. Drag-and-drop Query Builder — [query-builder.md](query-builder.md)  
3. Run a slow query → Visual Explain — [query-optimizer.md](query-optimizer.md)  
4. Live metrics — [performance-monitor.md](performance-monitor.md)  
5. AI generate/fix SQL — [ai-integration.md](ai-integration.md)  

## Sample database

Use the MySQL **`employees`** sample schema for JOIN-heavy stories.  
Upstream: [datacharmer/test_db](https://github.com/datacharmer/test_db).

```bash
git clone https://github.com/datacharmer/test_db.git
cd test_db
mysql -h 127.0.0.1 -u root -p < employees.sql
```

Verify: `SELECT COUNT(*) FROM employees.employees;`

## Day-of checklist

1. Test connection and expand `employees` in the tree.  
2. Open a new `.sql` file bound to that database.  
3. Run **two** scenarios from Query Builder + Optimizer guides.  
4. Have Marketplace install link ready for prospects.  
