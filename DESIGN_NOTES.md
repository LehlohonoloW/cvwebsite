# DESIGN RECORD v1 — WESSIE.PRIME (dark command deck) · superseded
# DESIGN RECORD v2 — "CUPERTINO" (2026-08-10, current)

User directives: "make it look completely different" → "give it the Apple look".
(Field-dossier blueprint sketch considered, then superseded by the Apple directive.)

## v2 Art direction (Apple.com grammar)
| Axis | v1 | v2 |
|---|---|---|
| Canvas | dark space-teal | white + #f5f5f7 alternating bands |
| Type | Sora display | SF system stack (-apple-system), tight -0.02em tracking, huge centered headlines |
| Accent | gold/teal glow | Apple blue #0071e3 + #06c links, one restrained gradient phrase |
| Surfaces | glass + glow | rounded-28px tiles, soft 0 12px 40px shadows, hairlines #d2d2d7 |
| Buttons | squared mono | pill radius 980px, blue fill / text-link with › |
| Field | starfield | soft mesh-gradient blobs, cursor parallax, blur(60px), near-invisible |
| Chrome | command deck | frosted slim nav; Spotlight-style ⌘K; macOS Terminal windows (traffic lights) |
| Removed | rail, marquee, custom cursor, tilt, sec-num chips | (un-Apple) |

Preserved function: ⌘K palette actions, HELIX command set, timeline draw-on-scroll,
scroll-spy nav, live JHB clock + uptime footer, reveals, copy email, motion toggle,
reduced-motion static render, skip link, semantic structure, WCAG AA contrast.

## Verification gates v2
- [ ] v1 suite re-run: console errors, overflowX 0, mobile 390, reduced motion, interactions

---
# v1 original record below
# WESSIE.PRIME — Immersive CV Rebuild · Design Record

Date: 2026-08-10 · Scope: replace `docs/index.html` (GitHub Pages, publish root `docs/`)
Deploy: drop-in single file; PDF link unchanged (`./Lehlohonolo Wessie-CV V3 Polished.pdf`).

## Pillars
1. **Immersion first** — the page is a living console, not a document.
2. **Reactive world** — signature element: a cursor-reactive signal constellation
   (canvas, player-local particles, proximity links, click ripples, hover bursts).
3. **One continuous journey** — boot → hero → modules → timeline → console → contact,
   tracked by a coded scroll rail.
4. **Depth, easy start** — 60-second recruiter scan intact; HELIX terminal + ⌘K palette
   for the curious.
5. **Craft over slop** — Lehro Spectrum palette (gold/azure/emerald/coral, no AI-purple),
   angular LW monogram, IBM Plex Mono console texture.

## Decision record
| Decision | Choice | Alternatives | Why |
|---|---|---|---|
| Architecture | Single self-contained `index.html` | build step, multi-page | matches repo, GitHub Pages-safe, smallest safe change |
| Reactive layer | Canvas 2D particle field | WebGL/three.js | zero deps, 60fps budget, DPR-capped, pauses offscreen |
| Fonts | Google Fonts @import (Sora/Space Grotesk/IBM Plex Mono) | self-host | parity with current site; strong system fallbacks |
| Palette | Lehro Spectrum on warm-paper dark | AI-purple gradients | workspace brand canon; slop avoidance |
| Terminal | Real command parser (help/whoami/stack/projects/hire/…) | fake typed video | actual interactivity = the ask |
| Navigation | ⌘K palette + rail + anchors | hamburger menu | console metaphor; mobile uses palette |
| Motion | rAF loops gated on `prefers-reduced-motion` + palette toggle | always-on | accessibility gate |

## Canon preserved
All CV facts, 7 OSS modules (Bilquo, SupportOID, Payconnectoid, ComplianceKit,
PDFoid, MCPSOIDS, Gidevo), timeline, credentials, contact details — unchanged.

## Verification gates
- [ ] Zero console errors, full scroll loop (headless Chromium)
- [ ] Desktop 1280px + mobile 390px screenshots, no overlap/overflow
- [ ] Reduced-motion pass renders statically
- [ ] Keyboard: skip link, palette arrows/esc, terminal input
- [ ] Photosensitivity: no strobes; slow ripples only

## Still genuinely open
- Fonts render as fallbacks in sandbox QA (no network); live site loads Google Fonts.
- GitHub Pages deploy not run here — user pushes to trigger workflow.
