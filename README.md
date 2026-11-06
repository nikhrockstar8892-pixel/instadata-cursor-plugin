# Instadata — Instagram research for Cursor (MCP)

Ask your agent about any public Instagram reel, profile or hashtag. Instadata returns
**reel transcripts & summaries**, stats, comments, profiles, hashtags, locations, brand
collaborations and **Meta Ad Library ads** as clean JSON via a hosted MCP server
(`https://mcp.instadata.dev`). Read-only. No Meta developer app.

**Try:** "Summarize this reel and its top comments: <reel URL>" ·
"Vet @brand: followers, last 10 posts, engagement" · "What ads is @brand running?"

## Install
- Cursor Marketplace: search **Instadata** → Install.
- Manual: add to `~/.cursor/mcp.json`:
```json
{ "mcpServers": { "instadata": { "url": "https://mcp.instadata.dev" } } }
```

## Auth
- **OAuth 2.1 + PKCE** (default): Cursor opens a sign-in at instadata.dev on first tool call.
- **Bearer key**: `Authorization: Bearer ik_live_...` from https://instadata.dev/app/keys.

## Pricing
25 free credits on signup, no card (free keys return up to 5 items per list call). Then **$5 per 1,000 credits** ($5/mo plan with rollover, $54/yr for 12,000, top-ups $5/1k). Most calls cost 1 credit per item; transcripts 1 + 20 per started minute; ads/collaborations 3 per row.

## Skills
| Skill | Triggers |
|---|---|
| instagram-profile-research | instagram.com profile URL, @handle, influencer/brand vetting |
| instagram-reel-research | reel/post URL, transcript, summary, comments, stats |
| instagram-hashtag-trend-research | hashtags, trends, keyword search, content ideas |
| instagram-ads-research | Meta Ad Library, competitor ads, paid partnerships |

## Reviewer notes
- Remote MCP only (Streamable HTTP) — no local code executed.
- Read-only; public data only; no posting, DMs, or login to Instagram accounts.
- Test: install, sign in with OAuth (25 free credits), ask "Get the transcript of https://www.instagram.com/reel/<id>/" or "Profile stats for @natgeo".
- Reviewers: sign up at https://instadata.dev for 25 free credits (OAuth or API key). Verified 4 Nov 2026 (live): DCR accepts Cursor’s full bundle — `cursor://anysphere.cursor-mcp/oauth/callback`, `https://www.cursor.com/agents/mcp/oauth/callback`, `https://www.cursor.com/bot/mcp/oauth/callback`, and `http://localhost:8787/callback` (PR #4 merged @ 7bf91a4). Contact: https://instadata.dev.
- Related open-source skills: https://github.com/nikhonit/instagram-api-skills

## License
MIT
