# HaitiBrand Email Assets

Banners, headers, hero images, and other assets used in Resend email campaigns.

## Why a dedicated repo

Agents (Kim, Gaelle, Research) need to upload email assets and reference their public URLs in Resend campaigns. This repo gives them a single, scoped surface — they can write here through the `email-assets-mcp` MCP server, and nowhere else. They have no access to other HaitiBrand repos (branding, mohaiti, Aria, hb-census, etc.).

## Public URLs

Any file at `path/to/file.ext` is reachable at:

```
https://raw.githubusercontent.com/haitibrand-co/email-assets/main/path/to/file.ext
```

Spaces in filenames must be URL-encoded as `%20`.

## Suggested structure

- `banners/` — campaign hero banners (1200×400 or similar)
- `headers/` — recurring email headers (logos, masthead bars)
- `clients/<client-slug>/` — per-client assets (when an asset is reusable across multiple sendouts for one client)
- `archive/` — retired assets we want to keep for reference

Don't worry too much about structure on day one. The MCP tool sanitizes paths and prevents escapes, so the worst case is a flat directory that we tidy later.

## Who can write

Only the `email-assets-mcp` MCP server, via tools exposed to Hermes agents. The server hardcodes this repo as its only target. Agents cannot specify a different repo.
