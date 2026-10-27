# Graphly plugin for Claude Code

One-step install of the Graphly MCP server (`https://graphly.click/mcp`, OAuth 2.1, no API key).

```
/plugin marketplace add uycung/graphly-claude-plugin
/plugin install graphly@graphly
```

Then run `/mcp`, choose `graphly` and sign in with Google in the browser.

The plugin ships the MCP connection and one skill (`graphly`) that tells Claude when to reach for Graphly: when you ask for a diagram or wireframe, or (as a one-line offer) when a diagram would clarify a repo or flow.

The tools (`create_diagram`, `create_wireframe`, `edit_diagram`, ...)
and the workflow prompts (`diagram`, `wireframe`, `build_from_board`, `repo_architecture`) come from the server,
so they update without a plugin release.

Graphly: https://graphly.click/ - MCP setup for other clients: https://graphly.click/docs/mcp/
