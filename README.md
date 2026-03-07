# TheArtOfService Compliance Intelligence MCP Server

A remote MCP (Model Context Protocol) server providing AI agents with access to a comprehensive compliance knowledge graph containing **692+ compliance frameworks**, **14,200+ controls**, and **819,000+ cross-framework mappings**.

## Quick Start

### Connect via Streamable HTTP

```
URL: https://api.theartofservice.com/mcp
Transport: Streamable HTTP
Authentication: Bearer token (API key) — optional for up to 10 calls/day
```

### Claude Desktop Configuration

Add to your `claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "compliance-intelligence": {
      "url": "https://api.theartofservice.com/mcp",
      "headers": {
        "Authorization": "Bearer tas_YOUR_API_KEY"
      }
    }
  }
}
```

### Cursor Configuration

Add to your MCP settings:

```json
{
  "compliance-intelligence": {
    "url": "https://api.theartofservice.com/mcp",
    "headers": {
      "Authorization": "Bearer tas_YOUR_API_KEY"
    }
  }
}
```

### npm Package (stdio transport)

```bash
npm install -g @theartofservice/compliance-mcp
```

See [@theartofservice/compliance-mcp on npm](https://www.npmjs.com/package/@theartofservice/compliance-mcp).

### Python / Langchain

```bash
pip install theartofservice-compliance
```

See [theartofservice-compliance on PyPI](https://pypi.org/project/theartofservice-compliance/).

## Getting an API Key

1. Create a free account at [compliance.theartofservice.com](https://compliance.theartofservice.com/register)
2. Navigate to Settings → API Keys
3. Generate an API key (starts with `tas_`)

**Anonymous access**: 10 calls/day with no API key required.

## Available Tools

| Tool | Description |
|------|-------------|
| `agent_search_frameworks` | Search and list compliance frameworks by name, keyword, or jurisdiction |
| `agent_get_framework` | Get detailed information about a specific compliance framework |
| `agent_get_framework_controls` | Get all controls for a compliance framework, optionally filtered by domain |
| `agent_get_control` | Get detailed information about a specific control by code |
| `agent_get_control_cross_references` | Get cross-framework mappings for a control (equivalent controls in other frameworks) |
| `agent_cross_framework_map` | Map controls between two compliance frameworks |
| `agent_coverage_report` | Get cross-framework coverage analysis for a framework |
| `agent_search` | Full-text search across controls and frameworks |
| `agent_platform_stats` | Get platform statistics (framework, control, mapping counts) |
| `agent_pricing_info` | Get API pricing tiers and current usage information |

## Pricing

| Tier | Calls | Price |
|------|-------|-------|
| Anonymous | 10/day | Free |
| Free account | 100/month | Free |
| Professional | 10,000/month + $0.005 overage | $49/month |
| Enterprise | 100,000/month + $0.005 overage | Custom |

## Links

- **Platform**: [compliance.theartofservice.com](https://compliance.theartofservice.com)
- **API Docs**: [api.theartofservice.com/docs](https://api.theartofservice.com/docs)
- **npm**: [@theartofservice/compliance-mcp](https://www.npmjs.com/package/@theartofservice/compliance-mcp)
- **PyPI**: [theartofservice-compliance](https://pypi.org/project/theartofservice-compliance/)

## License

MIT
