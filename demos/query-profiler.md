# Query Profiler demo

**Product:** Profile a SQL session and read **stage timings** (parse, optimize, execute, etc.) inside the editor.

## Walkthrough script

1. Connect to MySQL with profiling permitted for your user.  
2. Open a representative query in the SQL editor.  
3. Start **Query Profiler** from the Command Palette or context action.  
4. Execute the statement; show the stage breakdown and total time.  
5. Compare with **Visual Explain** from [Query Optimizer](query-optimizer.md) — profiler = *what time was spent*; explain = *how the plan ran*.

![Slow Query Analyzer & DB Profiler — same as sqllens.ai showcase 04](../media/gifs/query-profiler-demo.gif)

## Sample narrative

> “We ran the same join you saw in the Query Builder demo. Profiler shows most time in executing, not sending — so we open QO next to add an index.”

## Tips

- Use a dev database; profiling adds overhead.  
- Repeat after an index change to show delta in execute stage.  

## Related demos

- [Query Optimizer](query-optimizer.md)  
- [Performance Monitor](performance-monitor.md)  
- [Demo catalog](README.md)
