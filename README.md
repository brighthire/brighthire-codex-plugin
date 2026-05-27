# BrightHire Codex Plugin

Connect Codex to BrightHire interview intelligence data through the BrightHire MCP server.

## Status

This repository is a public-plugin starter package. It contains the Codex plugin manifest, BrightHire MCP server configuration, plugin skills, and basic brand assets.

## MCP Server

The plugin connects to the BrightHire MCP endpoint:

```text
https://app.brighthire.ai/mcp/v1/
```

The production plugin uses OAuth through the BrightHire MCP server. The plugin marketplace entry marks authentication as `ON_INSTALL` so Codex prompts users to connect BrightHire during installation. Do not place API keys, bearer tokens, OAuth secrets, private keys, or service-account credentials in this repository.

## Repository Layout

```text
.codex-plugin/plugin.json  Plugin manifest
.agents/plugins/           Local marketplace entry for testing
.mcp.json                  BrightHire MCP server configuration
skills/brighthire/         Codex guidance for when and how to use BrightHire
assets/                    Plugin icon and logo
```

## Local Development

Install or import this plugin from a local checkout in Codex, then verify that the BrightHire MCP server appears as a connected MCP server.

Suggested smoke tests:

1. Confirm Codex can discover the BrightHire MCP server.
2. Authenticate with BrightHire through OAuth when Codex prompts for connection.
3. Ask Codex to search for a BrightHire candidate, call, role, or interview.
4. Confirm responses avoid unnecessary exposure of sensitive interview data.

## Publishing Checklist

- Replace placeholder repository URLs if the public repo location changes.
- Confirm OAuth discovery, authorization, callback, token exchange, and refresh all work from a fresh install.
- Verify every MCP tool has a clear name, description, input schema, and safe read/write classification.
- Add polished screenshots under `assets/` if Codex plugin submission requires them.
- Review `SECURITY.md` and `PRIVACY.md`.
- Test installation from a fresh checkout.

## Security

BrightHire data can include sensitive candidate, interviewer, customer, and hiring-process information. Keep scopes narrow, avoid logging sensitive request content, and require explicit user confirmation for any write-capable tool.
