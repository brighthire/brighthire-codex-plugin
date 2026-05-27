# Security

Do not commit credentials to this repository.

The BrightHire Codex plugin should authenticate users through a supported connection flow. It must not require users to paste raw API keys, bearer tokens, OAuth secrets, private keys, or service-account JSON into Codex chat or into checked-in files.

BrightHire MCP tools may expose sensitive customer, candidate, interviewer, transcript, scorecard, and hiring-process data. Keep access scoped to the authenticated user and organization. Prefer read-only tools unless a write action has a clear product need and a reviewable confirmation step.

Report security issues through BrightHire's normal security intake process.
