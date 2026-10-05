# Widely MCP — distribution pack

The server is already live at `https://mcp.widely-mobile.com/mcp`. People connect with their Widely login. There is no API key. Docs: https://widely-mobile.com/mcp. Privacy: https://widely-mobile.com/en/privacy-policy (section “Connecting an AI”). Support: info@widely-mobile.com.

This folder is the manifest set for the four directories. Approval time is outside the build. Each submission uses the same URL.

## MCP Registry

Namespace `com.widely-mobile` is proved with a DNS TXT record on `widely-mobile.com`, then:

```bash
mcp-publisher login dns --domain widely-mobile.com
mcp-publisher publish server.json
```

`server.json` is the registry schema dated 2025-12-11.

## Cursor Marketplace

This folder is the plugin root (`.cursor-plugin/plugin.json`, `mcp.json`, `assets/logo.png`). Cursor reviews plugins from a public Git repository. Submit this repository (or a thin public copy of this folder) through the Cursor Marketplace form. Keywords: phone, calls, sms, voicemail, telecom, transcripts.

## Claude Connectors and ChatGPT

Both take the same remote URL, `https://mcp.widely-mobile.com/mcp`, OAuth (no API key), the docs URL, the privacy URL, and `assets/logo.png`. Those two portals need the Widely publisher login; they cannot be filed from the repo.

## Gemini CLI

```bash
gemini extensions install https://github.com/Swift-Mobile-Solutions-Dev/widely-mcp
```

On first tool use, Gemini CLI opens a browser for Widely OAuth (Dynamic Client Registration).

## Cline

Follow `llms-install.md`. Add the remote URL `https://mcp.widely-mobile.com/mcp` and complete Widely OAuth. Do not run a local install from this repository.

