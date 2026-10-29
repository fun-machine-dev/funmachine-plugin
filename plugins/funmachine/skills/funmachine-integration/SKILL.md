---
name: funmachine-integration
description: Build or change an integration with the Fun Machine API (Rips packs, Game Provider games, the operator wallet endpoints). Use when code calls funmachine.xyz or implements its wallet callbacks.
---

# Fun Machine integration

Read the docs through the `funmachine` MCP server. Don't guess endpoints, fields, or signing rules.

1. Pick the API.
   - `rips`: packs, prizes, shipments, and our games. Rips includes every Game Provider endpoint.
   - `game-provider`: our games only.
2. Call `get_guide` for that API before writing code. It covers auth, request signing, and the wallet rules.
3. Find each endpoint with `search_docs`, then read it with `get_endpoint`. Build requests and responses from its schema and examples.
4. The Operator Wallet API endpoints (`/get-session`, `/debit`, `/credit`, ...) are ones you build and we call. Everything else is ours to call.

If a tool returns 401, the docs key is missing or revoked. Create a new one at https://funmachine.xyz/docs/ai-agents.
