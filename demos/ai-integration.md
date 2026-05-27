# AI & LLM integration demo

**Product:** Generate, fix, and explain SQL using integrated cloud routing and/or your own provider keys — without leaving the editor.

## Walkthrough script

### 1. AI SQL Copilot (sqllens.ai showcase 02)

1. Open the **AI Assist** panel or command tied to SQL generation.  
2. Prompt example: *“List employees hired in 1999 with current salary above department average.”*  
3. Show generated SQL inserted or offered into the active editor.  
4. Emphasize **active database context** — generation respects the connection/schema bound to the file.

![AI SQL Copilot — same as sqllens.ai showcase 02](../media/gifs/ai-integration-demo-v4.gif)

### 2. Generate & autocomplete (gallery)

![AI SQL integration overview](../media/gifs/ai-integration-demo.gif)

### 3. Fix / explain flow

1. Paste a broken query (missing join, wrong alias).  
2. Run **Fix SQL** or **Explain this query**.  
3. Narrate diff or explanation panel — suitable for onboarding junior devs.

## Talk-track

| Audience | Message |
|----------|---------|
| Team leads | Faster first draft; human review still required |
| Security | Optional local-only providers; cloud sign-in is optional |
| Finance | Usage tied to sqllens.ai account when cloud routing is enabled |

## Guardrails to mention

- Always review generated DDL/DML before running on production.  
- Read-only connections should block destructive suggestions at execution time.  
- Enterprise policies may require cloud-only or cloud-disabled modes.  

## Related demos

- [SQL workspace](sql-workspace.md)  
- [Query Builder](query-builder.md)  
- [Demo catalog](README.md)
