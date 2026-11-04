---
name: instagram-reel-research
description: Use when the user shares an Instagram reel/post URL or asks for its transcript, summary, comments or stats; returns clean JSON via Instadata MCP.
---
# Instagram reel & post research (Instadata)

## Setup
Uses the `instadata` MCP server (https://mcp.instadata.dev). Sign in with OAuth when prompted, or set header `Authorization: Bearer ik_live_...` (key at https://instadata.dev/app/keys). 25 free credits on signup; then $5 per 1,000 credits. Read-only, public data only.

## Workflow
1. Transcript: get_transcript (1 credit + 20 per started minute). Summary + key points: get_summary (4 + 20/min).
2. Stats: get_post_stats (views, likes, comments, caption, audio, posted time).
3. Comments: get_comments (1 credit/comment) to mine audience questions and objections.
4. Return transcript quotes with timestamps where available, hook (first 3s), structure, CTA, and the source URL.
