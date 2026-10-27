# Graphly plugin for Claude Code

One-step install of the Graphly MCP server (`https://graphly.click/mcp`, OAuth 2.1, no API key).

```
/plugin marketplace add uycung/graphly-claude-plugin
/plugin install graphly@graphly
```

Then run `/mcp`, choose `graphly` and sign in with Google in the browser.

The plugin ships only the MCP connection. The tools (`create_diagram`, `create_wireframe`, `edit_diagram`, ...)
and the workflow prompts (`diagram`, `wireframe`, `build_from_board`, `repo_architecture`) come from the server,
so they update without a plugin release.

Graphly: https://graphly.click/ - MCP setup for other clients: https://graphly.click/docs/mcp/
