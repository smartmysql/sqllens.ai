# Performance Monitor (PM) demo

**Product:** Live MySQL metrics, process list, and replication-oriented signals inside VS Code.

## Walkthrough script

### 1. Open Performance Monitor

1. Connect to a running MySQL instance (demo or staging).  
2. Open **Performance Monitor** from the SQLLens sidebar or Command Palette.  
3. Point out the metric cards: connections, buffer pool, threads, QPS-style counters (as shown in your build).

![Open Performance Monitor](../media/gifs/performance-monitor-open-demo.gif)

### 2. Guided tour

1. Walk through tabs or sections (processes, status variables, config hints — per your SKU).  
2. Tie one metric to a story: e.g. rising **Threads_running** during a load test.  
3. Optional: open a long-running query in another tab and watch process list update.

![Performance Monitor tour](../media/gifs/performance-monitor-tour-demo.gif)

## Talk-track

- **Developers** — “See pressure on the instance while you tune queries in the editor.”  
- **DBAs** — “Quick health snapshot without leaving the IDE; pair with QO for drill-down.”  

## Pair with other pillars

| Follow-on | Why |
|-----------|-----|
| [Query Optimizer](query-optimizer.md) | Fix a hot query seen under load |
| [Query Profiler](query-profiler.md) | Stage timings for one session |
| [Query Builder](query-builder.md) | Reduce ad-hoc SQL errors before they hit prod |

## Related demos

- [Demo catalog](README.md)
