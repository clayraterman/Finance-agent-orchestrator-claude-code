# Finance Agent Orchestrator — Paper Design System

This repo connects to Paper (design tool) via MCP for UI design iteration.

## Paper MCP Setup
- Server configured in `.mcp.json` at `http://127.0.0.1:29979/mcp`
- Requires Paper Desktop app to be open locally

## Design Instructions
- Design specs live in `/designs/` as HTML files
- Use Paper MCP `write_html` tool to render them into artboards
- Never edit Codex v1 artboards — create new "Claude Code vN" versions
- See `/designs/README.md` for execution instructions

## Brand & Design System
See `/designs/design-system.md` for full color/typography/component specs.
