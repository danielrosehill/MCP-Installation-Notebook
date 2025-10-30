# Claude Code MCP Notes

Oct 30 2025

Some notes on Claude's current method for installing MCPs.

Key: pay attention to the ``--scope`` param.

``--scope user`` = "User" level installation (ie, always available in Claude CLI).

E.g.

```
claude mcp add --transport stdio cloudinary-asset-mgmt --scope user \
  -- npx -y --package @cloudinary/asset-management -- mcp start \
  --api-key 123456789012345 --api-secret aBcDeFgHiJkLmNoPqRsTuVwXyZ --cloud-name examplecloud
  ```

  ## But ... I Have Three Google Workspaces

  Right now I indeed have 3 Google Workspaces: personal, work, client. 

  What do you do when you might need Google Drive as an MCP but a different one for each project?

  I've found two approaches with various CLIs:

  - In some implementations, you can just create different names like "work-gdrive", "personal-gdrive." 
  - Alternatively ... this is where the project/repo level MCPs come in and shine: add a project level MCP.

The downside of project level MCP configs: it's cumbersome and time consuming.