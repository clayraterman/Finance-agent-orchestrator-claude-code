@AGENTS.md

# UI Component System — shadcn/ui

This project uses **shadcn/ui** for all UI components. The configuration lives in `components.json`.

## Rules for building UI

- **Always use shadcn/ui components** (`@/components/ui/*`) as the foundation for any UI work. Never build raw HTML/Tailwind equivalents when a shadcn component exists.
- To add a new shadcn component: `npx shadcn@latest add <component>` (e.g., `card`, `table`, `dialog`, `input`, `select`, `tabs`, `badge`, `chart`).
- Compose pages from shadcn primitives in `src/components/` (not in `ui/` — that's reserved for shadcn base components).
- Use the `cn()` utility from `@/lib/utils` for conditional class merging.
- Follow the existing Tailwind CSS v4 setup with CSS variables for theming (defined in `src/app/globals.css`).

## Paper integration (design source of truth)

The **Paper** MCP server is connected and provides access to design specs, notes, and records from the team's workspace. When implementing UI from Paper designs:

1. Use Paper MCP tools to fetch the relevant design notes/records for context.
2. Map design elements to the closest shadcn/ui component.
3. Match colors to the project's CSS variable theme tokens rather than hardcoding values.
4. If a design requires a component not yet installed, install it via `npx shadcn@latest add` before use.
