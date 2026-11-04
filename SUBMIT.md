# Submitting Instadata

## Pre-flight (do first)
1. Replace `assets/logo.png` if a newer brand mark exists (`assets/logo.svg` is a placeholder mark).
2. OAuth DCR (live verified 4 Nov 2026): Cursor bundle including `cursor://anysphere.cursor-mcp/oauth/callback` + https callbacks + localhost:8787 — HTTP 201.
3. Fix the "unhealthy" status on Glama for the MCP connector; verify `https://mcp.instadata.dev` answers MCP initialize.
4. Push this folder:
```bash
cd /workspace/instadata-cursor-plugin
git init && git add . && git commit -m "Instadata Cursor plugin v1.0.0"
gh repo create nikhrockstar8892-pixel/instadata-cursor-plugin --public --source . --push
```

## A) Cursor Marketplace (feeds Grok Bot plugin catalog / SearchPlugins)
1. Go to https://cursor.com/marketplace/publish, sign in with the Instadata/Nikhil Cursor account.
2. Repository URL: `https://github.com/nikhrockstar8892-pixel/instadata-cursor-plugin`.
3. It reads `.cursor-plugin/plugin.json`; check name `instadata`, logo, description, keywords render.
4. Category: Data / Developer tools. Paste "Reviewer notes" from README into the notes field; add a free test-account note (25 free credits on OAuth signup).
5. Accept Publisher Terms, submit. Manual review; answer reviewer emails promptly.
6. After approval, verify in Grok Bot: SearchPlugins "instagram" should return Instadata.

## B) cursor.directory (separate, faster queue)
1. Go to https://cursor.directory → sign in → Submit / "Add MCP" (and "Add plugin" if offered).
2. Name: Instadata — Instagram Data MCP. URL: https://mcp.instadata.dev. Repo link as above. Logo: assets/logo.png.
3. Description: reuse plugin.json description. Tags: instagram, mcp, reels, transcripts, api.
4. Note: slug "instagram-data" is taken (fastsocial) — use `instadata`.
