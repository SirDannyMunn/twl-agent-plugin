# TWL Agent Plugin

Connect an MCP-compatible assistant to your TWL account to manage workflows, campaigns, data workspaces, documents, signals, spaces, and browser actions.

## Setup

This package uses the portable Agent Plugins format: root `plugin.json`, `mcp.json`, and `skills/twl/SKILL.md`. Its remote Streamable HTTP endpoint is `https://api.usetwl.com/mcp/workflows`.

Install using your client's Agent Plugins support and complete TWL OAuth. Each user signs in to their own account. No credentials are included. A TWL account and applicable service entitlements are required.

OAuth discovery:
- `https://api.usetwl.com/.well-known/oauth-protected-resource/mcp/workflows`
- `https://api.usetwl.com/.well-known/oauth-authorization-server`

Users with multiple TWL organizations may need the `X-Organization-Id` request header set to their intended organization's UUID. Tool access remains scoped to the authenticated user's permissions.

## Examples

- List my TWL workflows and their status.
- Show my TWL campaigns.
- Find my onboarding document in TWL.
- Create a private draft document summarizing this plan.

Some tools modify data, launch automations, or perform external actions. Inspect tool annotations and follow the user's scope and the client's approval controls.

## Compatibility and review status

This package is prepared for marketplace review. Grok Bot installation, OAuth and end-to-end tool execution have not yet been validated. Do not interpret this repository as a marketplace approval. The same hosted server has been exercised in the ChatGPT review workflow.

## Links

- Website and support: https://usetwl.com
- Privacy: https://www.usetwl.com/privacy
- Terms: https://www.usetwl.com/terms

This repository contains only plugin configuration, usage instructions, and a logo. It does not contain the TWL backend, private workspace data, credentials, or reviewer accounts. The package retains its existing Proprietary license designation; no open-source relicensing is implied.
