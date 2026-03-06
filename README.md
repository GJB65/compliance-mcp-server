# TheArtOfService Compliance Intelligence MCP Server

A remote MCP (Model Context Protocol) server providing AI agents with access to a comprehensive compliance knowledge graph containing **692+ compliance frameworks**, **13,700+ controls**, and **280,000+ cross-framework mappings**.

## Quick Start

### Connect via SSE (Server-Sent Events)

```
URL: https://api.theartofservice.com/mcp
Transport: SSE
Authentication: Bearer token (API key)
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

## Getting an API Key

1. Create a free account at [compliance.theartofservice.com](https://compliance.theartofservice.com/register)
2. Navigate to Settings → API Keys
3. Generate an API key (starts with `tas_`)

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

## Framework Coverage

Access controls and cross-mappings for 692+ frameworks including:

- **International Standards**: ISO 27001:2022, ISO 27701, ISO 22301, ISO 9001, ISO 14001
- **US Frameworks**: NIST CSF 2.0, NIST SP 800-53 Rev 5, NIST SP 800-171, CMMC 2.0, FedRAMP
- **Privacy Regulations**: GDPR, CCPA/CPRA, HIPAA, PIPEDA, LGPD, POPIA
- **Industry Standards**: PCI DSS 4.0, SOC 2, HITRUST CSF, SWIFT CSCF
- **Cyber Security**: CIS Controls v8, OWASP Top 10, MITRE ATT&CK, Essential Eight
- **Australian Frameworks**: ISM, PSPF, APRA CPS 234, SOCI Act, Privacy Act 1988
- **EU Regulations**: EU AI Act, DORA, NIS2 Directive, EU Cyber Resilience Act
- **Governance & ESG**: COSO ERM, COBIT 2019, TCFD, GRI Standards, UN SDGs

## Discovery

- MCP Discovery: `https://api.theartofservice.com/.well-known/mcp.json`
- OpenAI Plugin: `https://api.theartofservice.com/.well-known/ai-plugin.json`
- OpenAPI Spec: `https://api.theartofservice.com/openapi.json`

## Example Usage

Once connected, you can ask your AI agent:

- "What controls does ISO 27001:2022 have for access management?"
- "Map the controls between NIST CSF 2.0 and ISO 27001:2022"
- "Find all frameworks that cover data encryption requirements"
- "What's the coverage overlap between SOC 2 and HIPAA?"
- "Search for controls related to incident response"

## Pricing

| Plan | Calls/Month | Price |
|------|-------------|-------|
| Free | 100 | $0 |
| Professional | 10,000 | $49/month |
| Enterprise | 100,000 | Custom |

## REST API

In addition to MCP, a REST API is available at `https://api.theartofservice.com/api/agent/`. See the [OpenAPI spec](https://api.theartofservice.com/openapi.json) for full documentation.

## Support

- Website: [compliance.theartofservice.com](https://compliance.theartofservice.com)
- Email: support@theartofservice.com

## License

This is a hosted service. The MCP server endpoint is provided by TheArtOfService Pty Ltd.
