# Lucas Bailey

> Local memory → governed execution → verifiable continuity

I build infrastructure for AI agents that can **remember what happened**, know
**what they were authorized to do**, emit signed records of **what they report doing**, and show
**when their authority ended** — with evidence that stays local, portable, and
independently verifiable.

## The stack

```text
whitemagic            local-first memory & session continuity   (MCP, Rust, MIT)
      │
      ▼
whitemagic-crystal    client-side encrypted memory & anchors    (AES-256-GCM / Ed25519, MIT)
      │
      ▼
continuity-receipt    portable, offline-verifiable evidence      (open spec, Apache-2.0)
      │
      ▼
mandala               bounded agent execution & Landlock kernel  (Bubblewrap / Landlock, MIT/Apache-2.0)
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
| **Review a protocol** — spec, 80 vectors, three verifier implementations (Python, Rust, TypeScript) | [`continuity-receipt`](https://github.com/lbailey94/continuity-receipt) |
| **Attack the architecture** — containment review snapshot & governed execution | [`mandala`](https://github.com/lbailey94/mandala) · [`mandalaos-gate-lite`](https://github.com/lbailey94/mandalaos-gate-lite) |
| **Verify memory integrity** — client-side encrypted crystals & off-store commitments | [`whitemagic-crystal`](https://github.com/lbailey94/whitemagic-crystal) · [AGMI scorecard (`10/10`)](https://agentmemoryintegrity.org/stores/whitemagic-crystals.html) |

Working notes and docs: [whitemagic.dev](https://whitemagic.dev)

The current open-alpha release is
[v11.2.1](https://github.com/lbailey94/whitemagic/releases/tag/v11.2.1)
(GitHub release, npm `latest`, and the website installer on Linux x86-64,
Linux arm64, and macOS arm64).
[Gen2 9.3.4](https://github.com/lbailey94/whitemagic/releases/tag/v9.3.4)
remains the qualified line for Homebrew, Scoop, winget, the Gemini CLI extension,
Windows x86_64, and Intel macOS.
Start with the [setup guide](https://www.whitemagic.dev/install) or the
[receipt consumer quickstart](https://github.com/lbailey94/continuity-receipt#readme).
Signatures bind signed bytes; source truth, real-world authority, completeness and
successful execution require the consumer's own policy and evidence.
