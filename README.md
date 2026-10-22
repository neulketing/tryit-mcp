# TRYIT MCP

Short-form video trend data for AI agents — viral Shorts, Reels and TikTok, rising keywords and creators, YouTube reference-channel breakdowns, original-upload candidates and long-running Meta ads across 100+ countries.

- **Server URL:** `https://inctryit.com/mcp` (remote, Streamable HTTP)
- **Auth:** OAuth 2.1 (sign in with your TRYIT account — no key needed) or `Authorization: Bearer <API key>`
- **Free sample tools without sign-in:** `https://inctryit.com/api/mcp`
- **Docs & pricing:** https://inctryit.com/en/mcp · Official MCP Registry name: `com.inctryit/tryit`

## Tools

| Tool | What it does | Credits |
|---|---|---|
| `account_status` | Plan, credit balance, monthly grant and recent transactions | free |
| `estimate_cost` | Credit price of each tool | free |
| `trending_items` | Top 12 trending short-form videos (sample) | free |
| `rising_keywords` | Keywords rising today | free |
| `rising_creators` | Rising creators in a country by viral multiple | free sample / 1 |
| `search_content` | Search viral short-form content by topic, country, platform | 1 |
| `keyword_trend` | Daily history (up to 30 days) for a keyword | 1 |
| `similar_content` | 12 videos similar in meaning to one item | 2 |
| `search_ads` | Longest-running collected Meta ads by brand or copy | 2 |
| `analyze_channel` | YouTube reference-channel breakdown | 5 |
| `find_original` | Earliest known uploads of a clip (candidates, not a rights verdict) | 5 |

All tools are read-only. Credits are charged only when results come back; repeats within 60 seconds are free and errors are refunded. Free accounts get monthly credits after a one-time phone verification.

## Connect

**Claude (web, desktop, mobile):** Settings → Connectors → Add custom connector → `https://inctryit.com/mcp` → sign in to TRYIT and allow.

**ChatGPT:** Plugins → Add → Add custom MCP server → `https://inctryit.com/mcp`, authentication OAuth → connect and allow.

**Claude Code:**
```
claude mcp add --transport http tryit https://inctryit.com/mcp
```
or as a plugin:
```
/plugin install tryit --marketplace neulketing/tryit-mcp
```

**Gemini CLI:**
```
gemini extensions install https://github.com/neulketing/tryit-mcp
```

**Cursor / VS Code / other clients** (`mcp.json`):
```json
{ "mcpServers": { "tryit": { "url": "https://inctryit.com/mcp" } } }
```

## Data & privacy

Views, subscribers and keyword counts are observed public values; scores, grades and viral multiples are computed by TRYIT. Results are capped per call (no pagination or bulk export).

- Privacy policy: https://inctryit.com/en/privacy
- Terms: https://inctryit.com/terms
- Support: hello@inctryit.com
