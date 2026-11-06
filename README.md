# InfiniteRanks MCP plugin

Read your saved AI search visibility evidence from Cursor, ChatGPT or Claude.

## Connect

Install the plugin and sign in to InfiniteRanks when prompted. Choose the workspace you want the client to read and grant access to that workspace. The server URL is `https://app.infiniteranks.com/mcp`.

## Install

| App | How |
|---|---|
| ChatGPT | Install InfiniteRanks from the ChatGPT plugin directory, then sign in when asked. |
| Codex | `codex plugin marketplace add hasi100/infiniteranks-mcp-plugin`, then install InfiniteRanks from `/plugins`. |
| Claude Code | `/plugin marketplace add hasi100/infiniteranks-mcp-plugin`, then `/plugin install infiniteranks`. |
| Cursor | Install from the Cursor plugin directory, or add this repository as a plugin source. |
| Any MCP client | Add the remote server `https://app.infiniteranks.com/mcp` and sign in with OAuth. |

Sign-in is OAuth in your browser (read-only scope `mcp:read`); no API key is needed.

## Files

- `plugin.json`, `mcp.json`: the Agent Plugins package used by the ChatGPT directory (OAuth declared on the server).
- `.codex-plugin/`, `.claude-plugin/`, `.cursor-plugin/` and `.mcp.json`: host manifests. Their server entry has no `extensions` block, because Codex currently rejects it (openai/codex#53658); these apps discover OAuth from the server.

## What it can read

- Workspace, brand and competitor details
- Saved prompts and their latest revisions
- Saved AI answers, mentions and citations
- Visibility, share of voice, position and sentiment summaries
- Most cited domains and open recommended actions

## Read-only scope

The MCP tools only read saved workspace data. They cannot add or edit prompts, add competitors, start collection, change actions or spend credits. Reading prompts does not start a collection.

## Documentation and support

- Guide: https://www.infiniteranks.com/docs/mcp
- Website: https://www.infiniteranks.com
- Support: hello@infiniteranks.com
- Privacy: https://www.infiniteranks.com/privacy
- Terms: https://www.infiniteranks.com/terms
