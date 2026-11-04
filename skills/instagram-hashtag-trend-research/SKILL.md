---
name: instagram-hashtag-trend-research
description: Use when the user asks for Instagram hashtags, hashtag stats, trending reels or posts on a topic, keyword search on Instagram, niche/content research, or competitor content ideas from Instagram data. Also when they share an instagram.com/explore/tags URL. Powered by Instadata MCP.
---
# Instagram hashtag & trend research (Instadata)

## Setup
Uses the `instadata` MCP server (https://mcp.instadata.dev). Sign in with OAuth when prompted, or set header `Authorization: Bearer ik_live_...` (key at https://instadata.dev/app/keys). 25 free credits on signup; then $5 per 1,000 credits. Read-only, public data only.

## Workflow
1. Discover tags: hashtag search (keyword → hashtags with post counts, related tags).
2. Size: hashtag stats (1 credit) or analytics incl. top posts (4 credits).
3. Content: hashtag posts/reels and keyword/reels search (1 credit/result) — keyword search finds posts that never used the hashtag.
4. Rank by views/engagement, cluster formats and hooks, and list links. Keep pulls small on free keys (5 items per list call).
