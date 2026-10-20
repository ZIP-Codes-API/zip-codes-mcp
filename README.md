# Zip-Codes.com Location Intelligence: Spatial Analysis, Districts & 14+ Years of Demographics

Location intelligence for US addresses and ZIP Codes, through the Model Context Protocol. Zip-Codes.com can validate a US street address and return its ZIP+4, census tract demographics, income, housing and school district in one call. It answers from current USPS data, updated monthly, and Census boundaries, so an agent looks addresses and ZIP Codes up instead of guessing them. Request the enrichments you need. The survey estimates describe the census tract and carry margins of error.

ZIP boundaries follow USPS carrier routes and are refreshed quarterly. Coverage includes PO Box and single-organization ZIP Codes that Census ZIP-area files leave out. Boundary enrichments show which counties and districts a ZIP overlaps, with shares measured by area. The USPS county assignment is available alongside the mapped counties.

For history, request Census TIGER/Line boundaries from 2010–2025. American Community Survey profiles use consistent field names across 2011–2024 releases for ZIP Code areas and 2022–2024 for tracts. A ZIP's survey estimates come from the Census ZCTA with the same code.

## Connect

Server URL: `https://mcp.zip-codes.com/mcp` (Streamable HTTP).

### Claude Code

```bash
claude mcp add --transport http zip-codes https://mcp.zip-codes.com/mcp
claude mcp add --transport http zip-codes https://mcp.zip-codes.com/mcp --header "X-Api-Key: YOUR_KEY"
```

### Cursor (`~/.cursor/mcp.json`) and other `mcpServers` clients

```json
{
  "mcpServers": {
    "zip-codes": {
      "url": "https://mcp.zip-codes.com/mcp",
      "headers": {
        "X-Api-Key": "YOUR_KEY"
      }
    }
  }
}
```

### VS Code (`.vscode/mcp.json`)

```json
{
  "servers": {
    "zip-codes": {
      "type": "http",
      "url": "https://mcp.zip-codes.com/mcp",
      "headers": {
        "X-Api-Key": "YOUR_KEY"
      }
    }
  }
}
```

### Claude / Claude Desktop custom connector

Add `https://mcp.zip-codes.com/mcp` as a custom connector. Connectors send no custom header, so they run in demo mode.

## Tools (11)

| Tool | Title | What it does |
|---|---|---|
| `about_data` | About this data | Where this server's data comes from: for each dataset the authority behind it, the edition served where the source publishes editions (TIGER/Line, ACS, ZCTA), how often a new release is taken, and a ready-made citation string. |
| `city_name_rules` | City name rules | How USPS names a ZIP Code, and which of those names may be used on mail. |
| `county_reference` | County reference | US counties and county equivalents — all 3,235 of them — with their Census and USPS names, which disagree for over a hundred, plus ANSI code, legal type, land and water area, and USPS delivery footprint. |
| `distance` | Distance between two places | Distance between two places, in miles and kilometres, plus the compass bearing from the first to the second. |
| `metro_area_reference` | Metro area reference | US metropolitan and micropolitan statistical areas (CBSAs) — all 935. |
| `quick_zip` | Quick ZIP / ZIP+4 / reverse geocode | The fast, small answer for a postal code. |
| `radius_search` | Radius search | Find every US ZIP Code and Canadian postal area within a radius of a centre point, with the distance to each. |
| `suggest_places` | Place search (type-ahead) | Search for a place by partial name, misspelled name, or partial code — the resolver that turns what a person typed into something the other tools can look up. |
| `validate_address` | Validate a US address | Validate and standardise a US street address and return its ZIP+4. |
| `zip_facts` | ZIP Code facts | Statistics about US ZIP Codes and Canadian postal codes: how many exist, how they break down by type, delivery point and carrier route totals, per-state tables, and ranked lists such as the ZIP Codes with the most carrier routes. |
| `zip_lookup` | ZIP Code lookup | The full record for a postal code — the main location-intelligence tool. |

## Pricing

No key needed to start. A free key gives 2,500 credits a day; plans and credit packs: https://www.zip-codes.com/api/pricing

## Support

Email jharris@zip-codes.com. Issues are turned off on this repository; email reaches the people who run the server.

## Links

- Overview: https://www.zip-codes.com/api/mcp
- API docs: https://api.zip-codes.com/docs
- Server overview for agents: https://mcp.zip-codes.com/llms.txt
