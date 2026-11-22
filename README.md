# GlowUp — Cerebras × Kimi K3.1 Pro × OpenClaw Hackathon Entry

**An agent took a 2003-era website and shipped an Awwwards-grade rebuild to production — including a deploy nobody asked for.**

*#KimiOnCerebras · [Live site](https://rustic-roasters-coffee.vercel.app/)*

## What it does

GlowUp is a high-end web-designer agent built on the OpenClaw harness, powered by Moonshot AI's Kimi K3.1 Pro on Cerebras ultra-fast inference.

**Input:** one sentence + a dated website
**Output:** a premium redesign, live on the internet

The pipeline the agent ran autonomously:

1. **Read** the legacy site (`before/rustic-roasters.html` — Comic Sans, marquees, visitor counter)
2. **Rewrite** it as a single self-contained page (~65 KB): dark-luxe espresso palette, editorial serif + grotesk type pairing, scroll-reveal motion, `prefers-reduced-motion` respected, premium brand copy (real content, no lorem ipsum)
3. **Document** its own design system (`DESIGN.md`)
4. **Verify** the render in a browser
5. **Deploy to Vercel — unprompted.** The agent found the CLI and shipped itself to production.

## Why it's fast enough to matter

Kimi K3.1 Pro on Cerebras streams at up to ~2,000 tokens/sec. The entire 65 KB rebuild generated in under two minutes of visible streaming — the design process became watchable, which is the difference between a tool demo and a demo people share.

## Files

| File | Purpose |
|---|---|
| `index.html` | The rebuilt site (also deployed live) |
| `before/rustic-roasters.html` | The deliberately-dated input site |
| `DESIGN.md` | The design system the agent wrote about its own work |
| `OPENCLAW_PROMPT.md` | The exact brief given to the agent |
| `DEMO_STORYBOARD.md` | How we recorded the 60-second demo |

## Run it yourself

```bash
# OpenClaw with the Cerebras provider plugin, Kimi K3.1 Pro as default model
npx openclaw@latest
openclaw plugins install @openclaw/cerebras-provider
# set CEREBRAS_API_KEY in ~/.openclaw/.env, model: cerebras/moonshotai-kimi-k3.1-pro-trial
```

Paste `OPENCLAW_PROMPT.md` into a fresh session pointing at `before/`.

## Notes from the trenches (what we learned about agent engineering in 24h)

- Long agent sessions on rate-limited providers die at compaction, not at inference: the summarization call itself gets 429'd. Fresh chat per task + file-based memory (`workspace/memory/`) beats heroics.
- Budget output tokens deliberately (16k vs 40k) to keep prompt headroom.
- The best demo moment is the one the agent creates by accident — we didn't script the deploy.

MIT License.
