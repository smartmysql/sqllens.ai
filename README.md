# sqllens.ai

**Write SQL faster. Boost MySQL performance with AI.**  
Advanced MySQL GUI for **VS Code** and **Cursor** — query builder, optimizer, profiler, performance monitor, and AI-assisted SQL.

[![VS Marketplace](https://img.shields.io/badge/VS%20Marketplace-skylineai.sqllens-blue)](https://marketplace.visualstudio.com/items?itemName=skylineai.sqllens)

> This repository is the **public showcase**: product demos, animated captures, and build metadata.  
> Extension **source code** is maintained separately and is not published here.

## Quick links

| Resource | Link |
|----------|------|
| Install extension | [VS Marketplace — SQLLens.AI](https://marketplace.visualstudio.com/items?itemName=skylineai.sqllens) |
| Product website | [skylineai.app](https://skylineai.app) |
| Issues & feedback | [GitHub issues](https://github.com/sudheer2000/skylinemysql/issues) |
| Contact | [hello@skylineai.app](mailto:hello@skylineai.app) |

## What’s in this repo

| Folder | Contents |
|--------|----------|
| [`demos/`](demos/README.md) | Markdown demo scripts and feature walkthroughs |
| [`media/gifs/`](media/gifs/) | UI recordings (Query Builder, Optimizer, AI, PM, Profiler, workspace) |
| [`build/`](build/README.md) | `package.json` (metadata), `extension-manifest.json` — **not** a compilable extension tree |
| [`sqllens-demos.code-workspace`](sqllens-demos.code-workspace) | Open in VS Code / Cursor to browse demos with recommended extensions |

### Open in VS Code

1. **File → Open Workspace from File…** → choose `sqllens-demos.code-workspace`, or open this folder directly.  
2. Install the recommended **SQLLens.AI** extension when prompted (or from Marketplace).  
3. Read demo scripts under `demos/` — preview markdown with built-in preview (`Ctrl+Shift+V`).  

> **Note:** This repo cannot run **F5 → Run Extension**; that requires the private development repository with full source and `out/extension.js`.

## Featured demo

![Query Builder — drag tables and columns into the SQL editor](media/gifs/query-builder-landing-demo.gif)

See the full [demo catalog](demos/README.md).

## Highlights

- **SQL workspace** — Explorer, per-file database context, CodeLens, favorites
- **Query Builder** — Drag-and-drop tables/columns with FK-aware JOINs
- **Query Optimizer** — Visual Explain, index recommendations, batch optimize
- **Performance Monitor** — Live metrics, processes, replication signals
- **Query Profiler** — Stage timings for a session
- **AI integration** — Generate, fix, and explain SQL (local or cloud routing)
- **Slow Query Log Analyzer** — Find offenders from server logs

## Install (end users)

1. Open **Extensions** in VS Code or Cursor (`Ctrl+Shift+X` / `Cmd+Shift+X`).
2. Search for **SQLLens.AI** (`skylineai.sqllens`).
3. Install and open the **SQLLens.AI** activity bar.
4. Follow [Get started — connect a database](demos/sql-workspace.md#connect).

Developers building from source should use the private development repository, not this showcase repo.

## License & attribution

- **sqllens.ai** — MIT. See [ATTRIBUTION.md](ATTRIBUTION.md).
- Based on [vscode-database-client](https://github.com/cweijan/vscode-database-client) by Weijan Chen (MIT).

## Maintainers

To refresh GIFs and demo markdown from the product repo:

```bash
# In the Skylinemysql (private) clone:
node scripts/sync_sqllens_ai_public_repo.js --target ../sqllens.ai
```

Then commit and push this public repository.
