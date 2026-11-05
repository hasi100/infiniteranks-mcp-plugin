---
name: infiniteranks-get-started
description: Use the InfiniteRanks remote MCP connector to read saved AI visibility evidence. Use when the user asks about brand mentions, visibility, citations, prompts, competitors, or recommendations already saved in their selected workspace.
---

# InfiniteRanks

Use the connected InfiniteRanks MCP tools to explain what AI platforms have already said about the selected brand workspace.

## Safe workflow

1. Call `workspace_get` first to identify the selected workspace, market, language, brand, and competitors.
2. Use `visibility_summary`, `competitors_list`, `prompts_list`, `prompt_get`, `chats_search`, `answers_list`, `top_sources`, `sources_list`, and `actions_list` only as needed.
3. Cite the captured platform, prompt, and source URLs when explaining a finding. State the date range and distinguish missing evidence from zero visibility.
4. Never claim that results represent consumer products exactly; model API answers may differ from consumer assistants.

The connector is read-only. It cannot add or edit prompts, add competitors, start tracking, run a collection, change actions, or spend credits. If the user asks for one of those changes, explain that they must do it in InfiniteRanks.
