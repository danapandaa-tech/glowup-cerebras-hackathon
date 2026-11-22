# Demo Storyboard — 60 seconds, Audience Choice on X

Prize reality: wins come from **organic impressions by Tue Nov 24, 10:00 AM PT**. Post ASAP after the video is done — impressions accrue over ~2.5 days. Organic only: no boosting, no engagement rings (disqualification risk).

## Recording rules (from the official guide)
- ≤60 seconds, must *clearly show Cerebras speed improving the UX*
- Recommended: side-by-side vs a GPU-based provider
- Hide API keys, notifications, personal tabs before recording
- Standard OpenClaw only — the speed patch is for the Discord Speed Bounty entry, never in this video

## Shot list (60s)
| t | Shot | Purpose |
|---|------|---------|
| 0:00–0:05 | Full-screen the ugly `rustic-roasters.html` — marquee blinking, Comic Sans | The pain is instantly funny + recognizable. No setup talking. |
| 0:05–0:10 | Cut to OpenClaw chat: paste the Glow-Up prompt. Timer overlay starts | "One sentence in." Establishes agent, not generator. |
| 0:10–0:35 | Speed-build montage: Kimi streaming HTML/CSS at ~2000 tok/s (real-time, 1x — the stream itself IS the wow). Show tokens/s readout from OpenClaw if visible | Core claim: speed of thought. |
| 0:35–0:42 | Split-screen 5s: same prompt to a GPU-based provider (slower first token) vs Cerebras | Directly satisfies "side-by-side comparison" requirement. |
| 0:42–0:52 | Open the rebuilt `index.html` — scroll through the dark-luxe redesign, hover micro-interactions, motion reveals | The before/after payoff. This is the clip people retweet. |
| 0:52–0:60 | Deploy → live URL on screen, type it into address bar, site loads on the real internet | Punchline: "…and it's already live." |

## X post draft (fill handles at submission time)
```
We gave an AI agent one sentence and 40 seconds.

It took a 2003-era coffee shop website — Comic Sans, marquees, visitor counter — and rebuilt it as an award-grade site, live, on Kimi K3.1 Pro running at ~2,000 tokens/sec on Cerebras. Then deployed it.

The before/after at 0:42 🤯

#KimiOnCerebras @Cerebras @Kimi_Moonshot
```
Include: Project name (proposed: **GlowUp**), team handle(s), 2–4 sentence description, repo link (recommended), demo video attached.

## Reddit entry (same video, different post)
- Post to r/cerebras with flair "Kimi K3.1 Pro Hackathon", upload video directly (native upload outperforms YouTube links for upvotes)
- Softer hook than X: emphasise the workflow (read → redesign → verify → deploy) and any design decisions people can discuss.

## Speed Bounty side-entry (separate, Discord only, ~20 min after main build)
- Task: OpenClaw finds 5 real Christmas gifts from real retail sites, with product-page links
- MUST use the official speed patch build; video shows top TPS + TPS written in the message text ("Speed Bounty entry: X,XXX TPS")
- Post in #share-your-demo on Cerebras Discord before Sun 10AM PT
- Do NOT use the patched build in the X/Reddit videos

## Checklist before posting
- [ ] No keys/emails/notifications visible in recording
- [ ] Video ≤60s, speed visible (timer or token stream)
- [ ] Tags + hashtag exact: #KimiOnCerebras @Cerebras @Kimi_Moonshot
- [ ] Repo README runs in <5 min
- [ ] Posted immediately after final cut; then back to sleep — impressions count until Tue 10AM PT
