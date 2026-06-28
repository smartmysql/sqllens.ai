<p align="center">
  <img src="media/logo-128.png" alt="SQLLens.AI" width="120" />
</p>

<h1 align="center">SQLLens.AI</h1>

<p align="center">
  <strong>The autonomous database engineer for VS Code and Cursor.</strong><br/>
  Write SQL faster, optimize performance with AI, and keep MySQL running at peak health.
</p>

<p align="center">
  <a href="https://sqllens.ai/"><img src="https://img.shields.io/badge/Website-sqllens.ai-1a73e8?style=for-the-badge" alt="sqllens.ai" /></a>
  <a href="https://marketplace.visualstudio.com/items?itemName=skylineai.sqllens"><img src="https://img.shields.io/badge/Install-VS%20Marketplace-007ACC?style=for-the-badge&logo=visualstudiocode&logoColor=white" alt="VS Marketplace" /></a>
</p>

<p align="center">
  <a href="https://sqllens.ai/">Live product tour</a>
  ·
  <a href="demos/">Demo guides</a>
  ·
  <a href="mailto:hello@skylineai.app">Contact</a>
</p>

---

## Overview

SQLLens.AI is an advanced **MySQL and MariaDB** workspace inside your editor: visual query building, AI-assisted SQL, query optimization, slow-query analysis, live performance monitoring, and session profiling — in one integrated experience.

This repository publishes **product demonstrations** (screen recordings and walkthrough guides) aligned with the [sqllens.ai](https://sqllens.ai/) website. It does not include extension source code. Demo https://youtu.be/3kf03MTH9Bc

## Product tour

The recordings below follow the same order as the [sqllens.ai](https://sqllens.ai/) feature showcases.

### 01 · Visual Query Builder

Drag tables and columns from your schema tree into the SQL editor. SQLLens builds JOINs from relationships and respects the clause under your cursor.

<p align="center">
  <img src="media/gifs/query-builder-landing-demo.gif" alt="Visual Query Builder demo" width="720" />
</p>

<p align="center"><a href="demos/query-builder.md"><strong>View demo guide →</strong></a></p>

### 02 · AI SQL Copilot

Describe what you need in plain language. Generate, fix, and explain SQL without leaving the editor.

<p align="center">
  <img src="media/gifs/ai-integration-demo-v4.gif" alt="AI SQL Copilot demo" width="720" />
</p>

<p align="center"><a href="demos/ai-integration.md"><strong>View demo guide →</strong></a></p>

### 03 · Query Optimization Engine

Turn execution plans into an interactive tree, score each step, and apply index recommendations from the optimizer workbench.

<p align="center">
  <img src="media/gifs/query-optimizer-workbench-demo.gif" alt="Query Optimization Engine demo" width="720" />
</p>

<p align="center"><a href="demos/query-optimizer.md"><strong>View demo guide →</strong></a></p>

### 04 · Slow Query Analyzer & Query Profiler

Rank costly statements from slow-query logs and inspect stage-level timings for a session.

<p align="center">
  <img src="media/gifs/query-profiler-demo.gif" alt="Query Profiler demo" width="720" />
</p>

<p align="center"><a href="demos/query-profiler.md"><strong>View demo guide →</strong></a></p>

### 05 · Performance Monitor

Open live metrics on demand — processes, health signals, and workload spikes when the database feels slow.

<p align="center">
  <img src="media/gifs/performance-monitor-tour-demo.gif" alt="Performance Monitor demo" width="720" />
</p>

<p align="center"><a href="demos/performance-monitor.md"><strong>View demo guide →</strong></a></p>

<p align="center">
  <a href="demos/"><strong>See all 12 feature recordings →</strong></a>
</p>

## Install SQLLens.AI

Install only from the official Marketplace listing:

**[skylineai.sqllens on VS Marketplace](https://marketplace.visualstudio.com/items?itemName=skylineai.sqllens)** — see [INSTALL.md](INSTALL.md).

> This repo does **not** ship `.vsix` installers or extension source code.

## Get started

1. Install from **Marketplace** or **Releases** (VSIX) above.
2. Open the **SQLLens.AI** activity bar and add a MySQL connection.
3. Explore the [demo guides](demos/) or visit [sqllens.ai](https://sqllens.ai/) for the full product story.

**New to the editor workspace?** Start with the [SQL workspace guide](demos/sql-workspace.md).

## Repository layout

| Path | Description |
|------|-------------|
| [`demos/`](demos/) | Step-by-step demo guides for each major feature |
| [`media/gifs/`](media/gifs/) | Product screen recordings (WebP-quality captures) |
| [`build/`](build/) | Extension release metadata for integrators |
| [`sqllens-demos.code-workspace`](sqllens-demos.code-workspace) | Optional VS Code workspace for browsing this repo |

## License

Released under the [MIT License](LICENSE).
