# MCP Server Configuration Guide

## Overview
This guide covers MCP server configuration for the following tools: GitHub, Figma, Azure DevOps, Azure, Filesystem, Playwright, Jira, Confluence, and Atlassian.

---

## Available MCP Servers

- **GitHub**: github/github-mcp-server - GitHub's official MCP Server
- **Azure DevOps**: https://github.com/microsoft/azure-devops-mcp
- **Azure**: https://github.com/Azure/azure-mcp - Start Azure server from List MCP servers
- **Jira**: sooperset/mcp-atlassian - MCP server for Atlassian tools (Confluence, Jira)
- **Figma**: GLips/Figma-Context-MCP - Provides Figma layout information to AI coding agents
- **Filesystem**: Available in List MCP servers - Start server to use
- **Playwright**: microsoft/playwright-mcp - Playwright MCP server
- **Atlassian**: atlassian/atlassian-mcp-server - Securely connects Jira and Confluence with LLM, IDE, or agent platforms

---

## GitHub Configuration

### Setup Steps
1. Generate a GitHub Personal Access Token (PAT) classic token with the following scopes:
   - `repo`
   - `workflows`
2. Copy and paste the MCP configuration code in `.vscode/mcp.json` file
3. When VS Code prompts for the token, provide it to start the MCP server

---

## Figma Configuration

### Public Documentation
GLips/Figma-Context-MCP: MCP server to provide Figma layout information to AI coding agents like Cursor

### Setup Steps
1. Generate a token in Figma:
   - Navigate to Profile > Security
   - Create a new token and assign necessary permissions
2. Copy and paste the following code in `.vscode/mcp.json` file with your token:

```json
{
  "servers": {
    "figma": {
      "type": "stdio",
      "command": "npx",
      "args": [
        "-y",
        "figma-developer-mcp",
        "--figma-api-key=YOUR_FIGMA_API_KEY_HERE",
        "--stdio"
      ]
    }
  }
}
```

### Usage
Provide the design URL in Copilot Chat and use prompts like:
- "Generate responsive code for this design and add a quote. Change the background color to rose and add a quote."

---

## Jira and Atlassian Configuration

### Setup Steps
1. Generate an API token in Jira:
   - Navigate to Profile > Account Settings > Security
   - Create API token
2. Use the Atlassian MCP server: atlassian/atlassian-mcp-server - Remote MCP Server that securely connects Jira and Confluence
3. Copy and paste the following code in `.vscode/mcp.json` file:

```json
{
  "servers": {
    "atlassian/atlassian-mcp-server": {
      "type": "http",
      "url": "https://mcp.atlassian.com/v1/sse",
      "gallery": "https://api.mcp.github.com/v0/servers/28c650c6-5e61-4ab7-9eb2-505be6350476",
      "version": "1.0.0"
    }
  },
  "inputs": []
}
```

### Starting the Server
In VS Code, start the Atlassian MCP server by using the HTTP URL: `https://mcp.atlassian.com/v1/sse`

---

## Azure DevOps Configuration

### Repository
https://github.com/microsoft/azure-devops-mcp

### Setup Steps
1. Copy and paste the following JSON configuration in your IDE:

```json
{
  "inputs": [
    {
      "id": "ado_org",
      "type": "promptString",
      "description": "Azure DevOps organization name (e.g. 'contoso')"
    }
  ],
  "servers": {
    "ado": {
      "type": "stdio",
      "command": "npx",
      "args": ["-y", "@azure-devops/mcp", "${input:ado_org}"]
    }
  }
}
```

2. Provide your organization name when prompted in VS Code and start the server

---

## Playwright Configuration

### Overview
Playwright is a testing tool for web applications.

### Repository
microsoft/playwright-mcp: Playwright MCP server

### Setup Steps
1. Click install in VS Code Insiders
2. Copy and paste the following configuration:

```json
{
  "servers": {
    "playwright": {
      "command": "npx",
      "args": [
        "@playwright/mcp@latest"
      ],
      "type": "stdio"
    }
  },
  "inputs": []
}
```

### Usage
Provide a web page snapshot and use prompts with actions like `browser_click`, `browser_hover`. Copilot will fetch the summary and perform actions.