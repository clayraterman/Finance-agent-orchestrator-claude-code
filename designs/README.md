# Paper Design Specs — Execution Guide

## Prerequisites
- Paper Desktop app open with the "Piggy Banker Financial Agent Orchestrator V1" file
- Claude Code running locally (`claude` in terminal)
- MCP connection working (`.mcp.json` points to Paper at `localhost:29979`)

## How to Deploy Designs to Paper

Run Claude Code locally and give it these instructions:

### Step 1: Mission Control Dashboard
```
Read the file designs/mission-control.html. Create a new artboard in Paper named
"Mission Control - Claude Code v1" at 1440x900 using create_artboard. Then use
write_html to insert the HTML content from that file into the artboard. Take a
screenshot when done.
```

### Step 2: Login Page
```
Read the file designs/login.html. Create a new artboard in Paper named
"Login - Claude Code v1" at 1440x900 using create_artboard. Then use write_html
to insert the HTML content. Take a screenshot when done.
```

### Step 3: Add Client Modal
```
Read the file designs/add-client-modal.html. Create a new artboard in Paper named
"Add Client Modal - Claude Code v1" at 1440x900 using create_artboard. Then use
write_html to insert the HTML content. Take a screenshot when done.
```

## Design System
See `design-system.md` for the full color palette, typography, spacing, and component specs.

## Iteration
After reviewing v1, create new versions by duplicating and modifying:
- `Mission Control - Claude Code v2`, `v3`, etc.
- Never modify the original Codex v1 artboards
