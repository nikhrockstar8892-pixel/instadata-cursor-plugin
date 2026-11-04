---
name: instagram-profile-research
description: Use when the user shares an instagram.com profile URL or @handle, or asks for Instagram data on a profile, creator, influencer or brand account — followers, bio, recent posts/reels, engagement, similar accounts, tagged posts, mentions, comments or paid brand collaborations. Powered by Instadata MCP.
---
# Instagram profile research (Instadata)

## Setup
Uses the `instadata` MCP server (https://mcp.instadata.dev). Sign in with OAuth when prompted, or set header `Authorization: Bearer ik_live_...` (key at https://instadata.dev/app/keys). 25 free credits on signup; then $5 per 1,000 credits. Read-only, public data only.

## Workflow
1. Normalize input to a handle (strip https://instagram.com/, @, query strings).
2. Call profile tool (full, 1 credit) for followers, bio, category, verified.
3. Pull channel posts/reels (1 credit/item) for recent content and engagement; compute avg likes/comments and engagement rate = avg interactions / followers.
4. Optional: similar accounts, tagged posts, mentions, recent comments, brand collaborations (3 credits/row) for influencer vetting.
5. Report a concise table with links to every post cited. Tell the user the credit cost before large paginated pulls.
