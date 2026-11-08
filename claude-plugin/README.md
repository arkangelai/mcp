# Arkangel AI plugin for Claude

Free, read-only health tools from [Arkangel AI](https://arkangel.ai) in Claude: ICD-10
(CIE-10) and CUPS codes, clinical calculators with evidence, and medical-claims audit
tools for Colombia, Mexico and Peru. No account, no patient data.

- MCP server: `https://arkangel.ai/mcp` (Streamable HTTP, no authentication)
- Setup for other clients: https://arkangel.ai/mcp-server

## Install

```bash
claude plugin marketplace add arkangelai/mcp
claude plugin install arkangel-ai@arkangel-ai
```

Or add only the server: `claude mcp add --transport http arkangel https://arkangel.ai/mcp`.

## Privacy Policy

The server keeps no tool arguments or results. It logs one line per call with the tool
name and the client's product name, and aggregated counts (tool, outcome, latency). Full
policy: https://arkangel.ai/privacy. Terms: https://arkangel.ai/terms. Support:
https://arkangel.ai/support.

Educational content for health professionals. It does not replace clinical or audit
judgment.
