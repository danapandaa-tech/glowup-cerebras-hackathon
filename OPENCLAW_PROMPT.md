# OpenClaw Prompt — "Glow-Up" (paste into OpenClaw chat during the live demo)

This is the exact instruction given to OpenClaw (running Kimi K3.1 Pro on Cerebras) in the demo video. Keep it as one paste so the whole build streams at once — the speed is the show.

---

## Prompt v1 (the one for the video)

```
Take the dated local business site at cerebras-hackathon/before/rustic-roasters.html and rebuild it as an award-winning, Awwwards-grade single-page site. Requirements:

1. Read the existing site first. Keep the real business content (name, menu + prices, hours, address, news) — redesign everything around it, including rewriting the copy into premium brand voice (no lorem ipsum).
2. Design system: dark luxe palette (espresso/espresso-cream), editorial serif display type (e.g. Fraunces or Cormorant) paired with a clean grotesk for body, generous whitespace, large type scale (clamp()), subtle grain/texture, one accent colour max.
3. Motion: smooth scroll-reveals, a hero with slow parallax or steam animation, hover micro-interactions on the menu rows. Respect prefers-reduced-motion.
4. Output: a single self-contained index.html (Tailwind via CDN or inline CSS is fine — it must open directly in a browser with zero setup) + a short DESIGN.md explaining the system in 10 lines.
5. When done, open it in the browser to verify it renders, then deploy it and give me the live URL.

Show your work as you go.
```

## Why each line is there (do not cut for the video)
- Line 1 → proves it *read* the old site (agent, not generator) and preserves real content → the "glow-up" story holds up.
- Line 2 → forces genuinely high-end design vocabulary, not bootstrap-default. This is what earns retweets.
- Line 3 → motion = the thing that looks impressive in a 60-sec video.
- Line 4 → zero-setup deliverable; keeps the demo reliable (rule #5 of hackathon playbooks).
- Line 5 → browser verify + live URL = the punchline of the video.

## Prompt v2 (backup, if we pick a different "before" subject)
Same skeleton, swap line 1's path. Any dated single-page site works. A real small-business site (with permission) or a well-known brand's ancient page beats a fictional one for virality — people share "they fixed X's website."

## Reasoning toggle
The guide says thinking is off by default on Cerebras (set `reasoning_effort` to enable) — but our verification probe saw reasoning tokens emitted by default on the `moonshotai-kimi-k3.1-pro-trial` endpoint. Practical consequence: give every call a real token budget (≥200) or content comes back empty. For the video, record one take with reasoning on and one with `reasoning_effort: none` (if supported) — the no-reasoning take will stream faster and the speed is the show; keep the on-reasoning take as the design-quality fallback.
