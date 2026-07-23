# Brand Style Guide — Crystal Exteriors

> Design system reference. Established 2026-07-19 from an SVG-diagram card deck.
> Use exactly as specified below for the flyer, then reuse the same tokens/
> components for business cards, logo, and website — one brand, not three
> separate designs.

## Context

Business: residential pressure washing, Palm Beach County. Audience: homeowners.
Overall mood: clean, modern, trustworthy, data-driven editorial/tech aesthetic —
premium SaaS product marketing, not a typical "local service flyer." Every
graphic reads as a clean diagram or infographic, not decorative clip art.
Water/clean = blue and cyan, the primary brand color.

Deliverable 1: a 7x5in flyer, print-ready, left on a door/doormat — must work
as a glance-read (2-3 seconds before keep-or-toss). Later, same system: business
cards, logo, landing page/website.

## Color system (exact hex values)

**Neutrals (text & surfaces)**
| Token | Hex | Use |
|---|---|---|
| `--ink` | `#0d1a2b` | main text, near-black navy |
| `--sub` | `#51617a` | secondary text, slate blue-gray |
| `--faint` | `#8595ab` | tertiary text, labels, muted captions |
| `--line` | `#d9e2ee` | borders, dividers (very light blue-gray) |
| `--bg1` | `#f7f9fc` | background gradient start (near white) |
| `--bg2` | `#e9eef6` | background gradient end (soft blue-gray) |
| page-wrap | `#dfe5ee` | outer canvas background behind cards |

**Primary brand (water / clean / trust)**
| Token | Hex | Use |
|---|---|---|
| `--blue` | `#0a63c9` | primary brand — CTAs, links, key numbers |
| `--blue-deep` | `#084a94` | darker blue, text-on-light emphasis |
| `--cyan` | `#0e9bd8` | secondary gradient partner to blue |

**Signal colors**
| Token | Hex | Use |
|---|---|---|
| `--green` | `#189a52` | positive / result / "after" / success |
| `--red` | `#d93636` | problem / "before" / grime / urgency |
| `--amber` | `#c97a10` | caution / limited-time / warning |
| `--tile` | `#a9b9cd` | neutral flat fill, abstract placeholder shapes |

**Accent rotation** (color-code services — driveway, siding, roof, rust, etc.;
each service gets one lane. 5 tokens each: base / bright / deep / light-tint /
border-tint)
| Accent | base | bright | deep | tint | tintB |
|---|---|---|---|---|---|
| Red | `#c8323f` | `#e05a5a` | `#9c2531` | `#fbeaec` | `#f2c4c9` |
| Green | `#178a4c` | `#2fb96f` | `#0f6437` | `#e8f6ee` | `#bfe4cd` |
| Indigo | `#5646d6` | `#7a68f0` | `#3f2fae` | `#eeecfb` | `#d3cdf5` |
| Teal | `#0d8f8a` | `#2fb3ac` | `#0a6b66` | `#e3f5f3` | `#bde5e2` |
| Amber | `#c9740c` | `#e89b2e` | `#935208` | `#fbf1e2` | `#f2d9b3` |
| Violet | `#8e3ba8` | `#b565cd` | `#6b2a80` | `#f6ecf9` | `#e4c8ee` |
| Pink | `#be3d6f` | `#d9689a` | `#93264f` | `#fceef4` | `#f2c6d9` |
| Blue | `#0a63c9` | `#0e9bd8` | `#084a94` | `#e8f1fc` | `#c3dcf5` |

Color is functional, not decorative — blue/cyan = brand and CTAs, green = clean
result, red = the dirty/problem state, amber = urgency. Never use color just to
look pretty.

## Typography

Font stack: `"Segoe UI Variable Display", "Segoe UI", system-ui, sans-serif`
(swap for a licensed equivalent like Inter, General Sans, or Neue Montreal if
this needs to leave Microsoft's font — same geometric-grotesk character: clean,
slightly rounded, confident at heavy weights)

- **Headline (H1):** huge, weight 800, letter-spacing -0.015em, line-height 1.04,
  balanced text-wrap. Key phrase within the headline colored in brand blue as an
  inline span (not the whole headline).
- **Subhead:** weight 600, color `--sub`, one bolded phrase in `--ink` for emphasis.
- **Eyebrow/label tag:** small, weight 700, letter-spacing .22em (very wide
  tracking), uppercase, colored in the active accent, preceded by a short
  (46x5px) rounded gradient dash "tick."
- **Numbers/stats:** tabular-nums, extra bold (800), often huge (100-220px),
  gradient-clipped fill (blue→cyan) — the single most reusable "wow" element
  for a before/after price or square-footage stat (Megastat component).
- **Body copy:** weight 600-700, never thin/light — everything reads confident
  and bold, no regular/400 weight text anywhere.

## Component library

- **Chip** (feature/benefit pill): white bg, 2px solid `--line` border, 14px
  radius, soft shadow `0 6px 18px rgba(13,26,43,.06)`, gradient dot bullet
  (blue→cyan) on the left, bold label, optional muted trailing note on the right.
- **Panel** (default content container): white bg, 2px solid `--line` border,
  26px radius, soft shadow `0 10px 30px rgba(13,26,43,.07)`.
- **Callout** (short punchy CTA line): solid `--ink` dark pill, white bold text,
  one word/phrase highlighted in light blue `#7fc4ff`. Phone number or "Book Now."
- **Consequence/key-line block:** colored left border (8px solid accent), tinted
  background matching that accent, 10px radius, bold colored text.
- **Stat bar:** horizontal progress bar, light gray track, gradient fill
  (accent→accent2), bold white value+label inside the fill.
- **Numbered ledger row:** circular tinted badge with number, bold title, muted
  description, inside a white bordered rounded row. Numbered process/step lists.
- **Thesis/emphasis banner:** full-width gradient block (accent→accent2), huge
  white bold text. Once per page maximum, for the single biggest claim.
- **Megastat:** one enormous number (150-220px), gradient-clipped text. Reserve
  for the single most important number on the page.
- **Before/after comparison row:** two-column layout, white X-mark in solid red
  circle vs white check-mark in solid green circle — "without us / with us."
- **Winner/featured card:** double-layered gradient border around a plain white
  card — makes one option "glow" without changing its shape.
- **Stamp/badge:** rotated (~7°) bordered badge, uppercase bold, accent
  border+text on a semi-transparent white chip. "LICENSED & INSURED" etc.

## Shape, shadow & texture rules

- Corner radius scale: 999px (full pill — badges/chips), 12-16px (bars, rows,
  small tiles), 22-26px (panels, big cards). Never sharp corners.
- Borders: default 2px solid `--line` on white surfaces.
- Shadows: soft and cool-toned only — `rgba(13,26,43, .05–.16)`, never black.
  Bigger elements get a larger, softer blur.
- Background texture: subtle dot-grid (dots every ~38px, low opacity slate
  `rgba(120,140,170,.18)`) over a soft diagonal gradient `--bg1` → `--bg2`.
  Premium print texture without looking busy — works on printed pieces too.

## Diagram/icon style

No stock icon packs or clip art. Simple custom line-diagrams: thin rounded
strokes (3-9px), gradient area fills under lines, dashed lines for the
"old/dirty/before" state, solid gradient lines for "new/clean/after." Flat
colored rounded rectangles (`--tile` `#a9b9cd`) stand in for abstract
photo/content placeholders rather than literal icons.

## Flyer-specific adaptation (7x5in print)

- Build at 300 DPI: 2100 x 1500 px canvas for a 7x5in flyer.
- Add 0.125in bleed on all sides for print (2175 x 1575px with bleed); keep all
  critical text/logo inside a 0.25in safe margin from the trim edge.
- Confirm CMYK-safe equivalents before print — `#0a63c9` and `#0e9bd8` should
  convert cleanly, but verify with the printer or design tool before final export.
- Content checklist: one big headline, one hero before/after visual or megastat,
  one callout with the phone number, a short chip-list of 3-4 services, a
  trust-stamp badge, one clear CTA. Nothing else — reads in under 3 seconds.
- Landscape (7in wide x 5in tall) generally reads faster for a doorstep flyer
  than portrait — default to landscape unless matching a door-hanger die-cut.

## Build sequence

1. **Flyer** (this system, built 2026-07-19 — see `flyer-7x5-doorstep.html`)
2. Business card — reuse exact tokens/components
3. Logo mark — seed from the gradient-dot / rounded-tile motifs in the
   chip and stat-bar components
4. Website — same system, so everything feels like one brand