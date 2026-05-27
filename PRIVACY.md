# Privacy

This plugin connects Codex to BrightHire through the BrightHire MCP server at:

```text
https://app.brighthire.ai/mcp/v1/
```

When enabled, Codex may send user requests and relevant conversation context to the BrightHire MCP server so BrightHire can return matching interview intelligence data. Returned data may include information about candidates, interviewers, calls, transcripts, scorecards, roles, and organizations depending on the authenticated user's permissions.

Do not use this plugin with data you are not authorized to access. BrightHire should enforce access control server-side for every MCP tool call.
