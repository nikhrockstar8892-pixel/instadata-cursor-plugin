# Instadata — Instagram Data API & MCP for Cursor

Public Instagram data for agents: profiles, posts, reels, **reel transcripts & summaries**, comments, hashtags, keyword search, locations, brand collaborations and **Meta Ad Library ads** — clean JSON via a hosted MCP server. Read-only.

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
- Reviewers: sign up at https://instadata.dev for 25 free credits (OAuth). Confirm Cursor MCP OAuth redirect URIs are allowlisted before relying on sign-in during review. Contact: https://instadata.dev.
- Related open-source skills: https://github.com/nikhonit/instagram-api-skills

## License
MIT
