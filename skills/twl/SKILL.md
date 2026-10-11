---
name: twl
description: Use a connected TWL account to inspect or manage workflows, runs, data workspaces, documents, signals, spaces, and browser actions. Do not use for building or deploying Apps Layer manifest packages through the twl-tool CLI.
---

# TWL

Use the TWL MCP server for account-scoped work. Prefer its resources for reading workflow configuration and runtime state, and its tools for searches, validation, mutations, launches, and signals.

Before a broad or unfamiliar operation, call the server's tools documentation or health tool and inspect the relevant existing resource. Reuse returned identifiers exactly; do not guess organization, workflow, table, document, signal, space, listener, or run IDs.

For changes, preserve the user's requested scope and use the narrowest available mutation. Validate workflow definitions and nodes before launch when the server exposes validation for the operation. Report concrete results using the identifiers and status returned by TWL.

Treat CLI-only Apps Layer work as a separate surface. The `twl-tool` CLI lives in `packages/apps-layer/sdk` and owns app-manifest build, validation, planning, certification, and deployment. An MCP token with `mcp:use` does not authorize Apps Layer deployment.
