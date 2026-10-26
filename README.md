# Lucas Bailey

> Local memory → governed execution → verifiable continuity

I build infrastructure for AI agents that can **remember what happened**, know
**what they were authorized to do**, prove **what they actually did**, and show
**when their authority ended** — with evidence that stays local, portable, and
independently verifiable.

## The stack

```text
whitemagic            local-first memory & session continuity   (MCP, Rust, MIT)
      │
      ▼
continuity-receipt    portable, offline-verifiable evidence      (open spec, Apache-2.0)
      │
      ▼
mandalaos-gate-lite   bounded agent execution that emits receipts (review snapshot)
      │
      ▼
whitemagic-plugins    client integrations & adapters
```

Each repository stands on its own — WhiteMagic does not require MandalaOS, and
Continuity Receipt does not require WhiteMagic.

## Three entrances

| Want to… | Start at |
| --- | --- |
| **Use it** — memory and continuity for your coding agent | [`whitemagic`](https://github.com/lbailey94/whitemagic) |
| **Review a protocol** — spec, vectors, three independent verifiers (Python, Rust, TypeScript) | [`continuity-receipt`](https://github.com/lbailey94/continuity-receipt) |
| **Attack the architecture** — containment review snapshot | [`mandalaos-gate-lite`](https://github.com/lbailey94/mandalaos-gate-lite) |

Working notes and docs: [whitemagic.dev](https://whitemagic.dev)
