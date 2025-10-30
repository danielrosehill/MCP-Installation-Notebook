# Context7 MCP Installation - Claude Code

30 Oct 2025

## About Context7

Context7 is an MCP server that provides access to up-to-date documentation and code examples for various libraries and frameworks.

## Installation Command

The Context7 MCP can be installed using the Claude Code CLI with user-level scope:

```bash
claude mcp add --transport stdio context7 --scope user \
  -- npx -y @upstash/context7-mcp --api-key ctx7sk-xxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
```

### Important Notes

- **Scope**: Use `--scope user` for user-level access (recommended)
- **API Key**: Replace `ctx7sk-xxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx` with your actual Context7 API key
- The command uses `npx -y` to automatically install and run the package without prompting

## Configuration

After installation, the MCP server will be available in your Claude Code environment with user-level access, allowing you to query documentation for various libraries and frameworks.
