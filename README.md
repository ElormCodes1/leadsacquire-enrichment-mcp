# LeadsAcquire MCP

**B2B company & people enrichment plus live hiring-intent — for your AI tools.**

Connect once, then ask in plain language. Your assistant looks up businesses,
the real people behind them (names, roles, contact details), and a company's
current open roles and hiring signals.

- **Endpoint:** `https://api.leadsacquire.com/mcp`
- **Auth:** `Authorization: Bearer <your API key>`
- **Get a free key:** https://app.leadsacquire.com (email magic-link, ~20 seconds)

Read-only. Works with any MCP-compatible client.

---

## Connect

**Claude Desktop / Claude Code / Cursor / any MCP client:**
```json
{
  "mcpServers": {
    "leadsacquire": {
      "type": "http",
      "url": "https://api.leadsacquire.com/mcp",
      "headers": { "Authorization": "Bearer YOUR_API_KEY" }
    }
  }
}
```

**Claude Code one-liner:**
```bash
claude mcp add leadsacquire --transport http https://api.leadsacquire.com/mcp \
  --header "Authorization: Bearer YOUR_API_KEY"
```

---

## Tools

| Tool | What it does |
|------|--------------|
| `search_businesses` | Find businesses by name, region, city, category, or rating |
| `enrich_company` | The people tied to a company — names, titles, emails/phones/socials |
| `find_decision_makers` | Just the decision-makers for a company, with contacts |
| `get_business` | A single business's full record |
| `hiring_signals` | Live open roles + a hiring-intent score, department breakdown, top locations, and buying signals |

## Example

> "Is ramp.com in growth mode right now?"

`hiring_signals("ramp.com")` → **182 open roles, intent 81/100**, Sales-heavy
(85 roles) → *expanding go-to-market*. Hiring velocity is reported only when the
source job board exposes a true first-posted date, so recency is never guessed.

---

## Pricing & keys

Create and manage keys at **https://app.leadsacquire.com**. Usage is metered per
key. Questions: [leadsacquire.com](https://leadsacquire.com).

MIT licensed client metadata. Data is read-only.
