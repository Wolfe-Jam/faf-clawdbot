# faf-clawdbot

**Universal AI context for ClawdBot.**

Bridge ClawdBot to the universal AI context layer using [FAF](https://faf.one) (IANA: `application/vnd.faf+yaml`).

One `project.faf` → works everywhere:

```
project.faf (universal)
    │
    ├──→ ClawdBot (SOUL.md)
    ├──→ Claude Desktop (native)
    ├──→ Cursor (native)
    ├──→ VS Code (native)
    └──→ Any MCP-compatible tool
```

**Edit once. Context everywhere.**

## Install

```bash
npm install -g faf-clawdbot
```

## Quick Start

```bash
# Create project.faf in your ClawdBot workspace
cd ~/clawd
faf-clawdbot init "my-assistant"

# Edit your context
nano project.faf

# Generate SOUL.md for ClawdBot
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
  tone: "Direct, helpful, no fluff"
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

## Why Universal?

| SOUL.md (ClawdBot only) | project.faf (Universal) |
|-------------------------|-------------------------|
| Freeform markdown | Structured YAML |
| Trapped in one tool | Works everywhere |
| Local file | Cloud-syncable (MCPaaS) |
| Custom format | IANA-registered standard |

## The Universal Layer

```
┌─────────────────────────────────────────────────────────────┐
│                 UNIVERSAL AI CONTEXT                        │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│   project.faf sits between package.json and README.md       │
│                                                             │
│   package.json    ← npm's context                           │
│   project.faf     ← AI's context (IANA-registered)          │
│   README.md       ← human's context                         │
│                                                             │
│   ONE FORMAT → EVERY AI TOOL                                │
└─────────────────────────────────────────────────────────────┘
```

## Links

- **FAF Spec**: https://faf.one
- **IANA Registration**: `application/vnd.faf+yaml`
- **faf-cli**: https://www.npmjs.com/package/faf-cli
- **ClawdBot**: https://github.com/clawdbot/clawdbot

## License

MIT

---

*Built by [Wolfe-Jam](https://wolfejam.dev) | Powered by [FAF](https://faf.one)*
