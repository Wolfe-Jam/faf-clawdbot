# faf-clawdbot

**Portable souls for ClawdBot.**

Transform ClawdBot's `SOUL.md` into a structured, portable format using [FAF](https://faf.one) (IANA: `application/vnd.faf+yaml`).

Your soul works everywhere - ClawdBot, Claude Desktop, Cursor, VS Code, any MCP-compatible tool.

## Install

```bash
npm install -g faf-clawdbot
```

## Quick Start

```bash
# Create project.faf in your ClawdBot workspace
cd ~/clawd
faf-clawdbot init "my-assistant"

# Edit your soul
nano project.faf

# Generate SOUL.md
faf-clawdbot sync
```

## Commands

| Command | Description |
|---------|-------------|
| `init [name]` | Create `project.faf` in workspace |
| `sync` | Generate `SOUL.md` from `project.faf` |
| `watch` | Auto-sync on file changes |
| `status` | Show current FAF/SOUL status |

## Example project.faf

```yaml
project:
  name: "my-assistant"
  goal: "Personal AI across all platforms"

persona:
  voice: "Direct, helpful, no fluff"
  style: "Senior engineer"
  traits:
    - "Concise responses"
    - "Proactive suggestions"

context:
  owner: "James"
  preferences:
    - "No emojis unless asked"
    - "Code examples when relevant"

stack:
  model: "claude-opus-4-5"
  platforms:
    - "telegram"
    - "slack"
```

## Why FAF?

| SOUL.md | project.faf |
|---------|-------------|
| Freeform markdown | Structured YAML |
| ClawdBot only | Works everywhere |
| Local file | Cloud-syncable (MCPaaS) |
| Custom format | IANA-registered standard |

## Portability

Same `project.faf` works with:
- ClawdBot (via this tool)
- Claude Desktop (native)
- Cursor
- VS Code
- Any MCP-compatible tool

Edit once. Soul everywhere.

## Links

- **FAF Spec**: https://faf.one
- **IANA Registration**: `application/vnd.faf+yaml`
- **faf-cli**: https://www.npmjs.com/package/faf-cli
- **ClawdBot**: https://github.com/clawdbot/clawdbot

## License

MIT

---

*Built by [Wolfe-Jam](https://wolfejam.dev) | Powered by [FAF](https://faf.one)*
