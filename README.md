# Fun Machine plugin

Lets Claude Code or Codex read the Fun Machine API docs while it builds your integration. It adds the `funmachine` MCP server (search the docs, read any endpoint) and a skill on how to use it.

First, create a docs key at https://funmachine.xyz/docs/ai-agents.

## Claude Code

```
/plugin marketplace add fun-machine-dev/funmachine-plugin
/plugin install funmachine@funmachine
```

Claude Code asks for the docs key on install and keeps it in your system keychain.

## Codex

```
export FUNMACHINE_DOCS_KEY=<your docs key>
codex plugin marketplace add fun-machine-dev/funmachine-plugin
codex plugin add funmachine@funmachine
```

Put the `export` in your shell profile so every Codex session has it.
