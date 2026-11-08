# Arkangel AI MCP

Free, read-only health tools from [Arkangel AI](https://arkangel.ai) for AI assistants:
ICD-10 (CIE-10) and CUPS codes, clinical calculators with evidence, and medical-claims
audit tools for Colombia, Mexico and Peru. No account, no patient data.

This repo only holds the client packages. The server is hosted at
`https://arkangel.ai/mcp` (Streamable HTTP, no authentication). Setup for every client:
https://arkangel.ai/mcp-server

## Claude Code

```bash
claude plugin marketplace add arkangelai/mcp
claude plugin install arkangel-ai@arkangel-ai
```

Or add only the server: `claude mcp add --transport http arkangel https://arkangel.ai/mcp`.

## Gemini CLI

```bash
gemini extensions install https://github.com/arkangelai/mcp
```

## Other clients (ChatGPT, Grok, Cursor, VS Code…)

Point the client to `https://arkangel.ai/mcp`. Instructions: https://arkangel.ai/mcp-server

## Contents

| Path | What it is |
| --- | --- |
| `.claude-plugin/marketplace.json` | Claude plugin marketplace |
| `claude-plugin/` | Claude plugin: server URL, skill and icon |
| `gemini-extension.json`, `GEMINI.md` | Gemini CLI extension |

## Privacy

The server keeps no tool arguments or results. It logs one line per call with the tool
name and the client's product name, and aggregated counts (tool, outcome, latency).
Policy: https://arkangel.ai/privacy · Terms: https://arkangel.ai/terms ·
Support: https://arkangel.ai/support

Educational content for health professionals. It does not replace clinical or audit
judgment.
