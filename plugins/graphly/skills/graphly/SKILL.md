---
name: graphly
description: Draw architecture, UML and planning diagrams and clickable wireframe prototypes with the Graphly MCP tools. Use when the user asks to draw, diagram, sketch, map out, wireframe or mock up something ("draw the architecture", "sequence diagram", "kanban board", "wireframe the login screen", "vẽ sơ đồ", "sơ đồ tuần tự", "thiết kế giao diện"), and offer it (one line, never create unprompted) when explaining a repo's architecture, a flow, or a new feature where a diagram would make it clearer.
---

# Graphly

Graphly draws diagrams and clickable wireframes on a board the user can open at graphly.click. The tools (`create_diagram`, `create_wireframe`, `edit_diagram`, `edit_wireframe`, `get_diagram`, `list_diagrams`, `undo_last_edit`, `get_diagram_guide`) come from the `graphly` MCP server, which also sends its own instructions. Follow those instructions, including asking before creating.

## When to use

- The user asks for a diagram, sketch, board or wireframe: use Graphly.
- You are explaining a repo's architecture, a flow, or designing a feature and a diagram would help: say so in one line and offer to draw it. Wait for a yes. Every create call makes a new board in the user's account.
- The user wants Mermaid, ASCII or a text outline: do that instead.

## Which guidance to follow

Do not copy drawing rules from memory; the server keeps them current.

- Diagram of the current repo: the `repo_architecture` prompt.
- Building from an existing board: the `build_from_board` prompt.
- Any other diagram: the `diagram` prompt, then `get_diagram_guide`.
- Wireframe or clickable prototype: the `wireframe` prompt.
- A board already exists in this conversation: edit it, do not create another.

## Not signed in

If the Graphly tools are missing or return an auth error, tell the user to run `/mcp`, choose `graphly` and sign in with Google, then stop. Do not draw a Mermaid or ASCII substitute unless they ask for one.
