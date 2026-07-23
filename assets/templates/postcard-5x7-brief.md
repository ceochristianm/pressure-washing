# Postcard Brief — 5x7 Portrait, One-Sided (Greenacres/local field card)

> Created 2026-07-19. Front-only design, printed at Staples on 14pt cardstock,
> gloss finish front. Back stays completely blank white/uncoated — intentionally,
> for handwriting custom on-site quotes with a Sharpie. Do not design the back.

## 1. Text for the front

**Headline:**
> LOOK WHAT WE FOUND UNDER THE GRIME.

(Ties directly to the before/after photo instead of restating it — avoids
repeating the curb-appeal/HOA angle already used on the 7x5 doorstep flyer, so
the two pieces don't read identically if a homeowner sees both.)

**Kicker/subhead (small, above or below headline):**
> Professional Soft-Wash & Pressure Washing — Palm Beach County

**Service bullets (no prices — removed per 2026-07-19 direction):**
- Driveways & Sidewalks
- Siding & House Wash
- Roof Soft-Washing
- Gutters & Downspouts

**Trust line (small, true as of today — no review claims, GBP has zero reviews):**
> Licensed & Insured

**CTA (large, dominant element):**
> Call or Text: (561) XXX-XXXX

Placeholder — replace with the real business line before printing. Same
placeholder convention as the doorstep flyer, deliberately unmistakable as a
placeholder so it can't get printed by accident.

**Small brand tag (bottom corner, minor):**
> getcrystalexteriors.com · @getcrystalexteriors

## 2. AI image generation prompt

Vertical (5:7 portrait) photorealistic before/after driveway split, written to
leave clean negative space for text overlay and to hold up at 300 DPI print:

> Photorealistic vertical split-comparison image, 5:7 portrait aspect ratio,
> professional real-estate/exterior-cleaning photography style. Diagonal
> dividing line from lower-left to upper-right. One side: a suburban Florida
> concrete driveway heavily stained with black algae streaks, green mold
> splotches, and grime, dull overcast lighting, dirty worn texture, visible
> tire marks. Other side: the same driveway freshly pressure-washed — bright
> clean light-gray concrete, water still glistening, warm golden-hour
> sunlight, vibrant and inviting. Include the edge of a single-story South
> Florida stucco home with clean white or light-blue siding, a manicured
> lawn, and a palm tree in the background for context. Shot on a full-frame
> camera, 35mm lens, shallow depth of field on the background, tack-sharp
> focus on the concrete texture in the foreground, natural realistic color
> grading, no oversaturation, high dynamic range, ultra-detailed, 8K quality.
> Leave the top 20% of the frame as relatively open sky/negative space and the
> bottom 15% as clean unbroken pavement, so bold marketing text can be
> overlaid without competing with visual detail. No text, no watermark, no
> logos, no people in the frame.

Generate at the highest resolution the tool allows (minimum ~1575 x 2205px to
cover the 5.25 x 7.25in bleed canvas at 300 DPI; more headroom is better —
upscaling a low-res AI image for print is where softness/artifacts show up).

## 3. Canva & printing specifications

**SIZING — corrected for portrait, not the flyer's landscape numbers:**
This is a 5in-wide x 7in-tall card. Canvas = trim + 0.125in bleed all sides =
**5.25 x 7.25in (width x height)**. The earlier draft spec had this flipped to
7.25 x 5.25 (that's the landscape doorstep-flyer canvas) — set the Canva
canvas to **5.25in wide by 7.25in tall**, or it prints sideways/wrong-cropped.

**COLOR — RGB #0a63c9 / #0e9bd8 in a CMYK/print environment:**
Ballpark CMYK equivalents (indicative, not exact — actual conversion depends
on the specific press profile): `#0a63c9` ≈ C88 M63 Y0 K0; `#0e9bd8` ≈ C74
M23 Y0 K0. Blues like these are generally within CMYK gamut and don't shift
as badly as neon greens/oranges do, but some dulling (roughly 5–15%
desaturation) on a digital press is normal, not a sign of a bad file.
Practical guidance for a Staples in-store job specifically: Staples print
centers run digital toner presses that typically accept RGB directly and do
their own internal conversion — don't hand-convert to CMYK yourself unless
Staples' upload tool explicitly asks for a CMYK PDF (double-converting can
look worse than leaving it RGB). **Order one physical proof card before
running a full batch**, hold it next to the on-screen hex value, and nudge
saturation up 5–10% in Canva and reprint the proof if it looks dull — that's
more reliable than trying to hand-calculate an exact conversion.

**LAYOUT SAFETY:**
Content-safe area = canvas inset 0.375in from every edge (0.125in bleed +
0.25in safe margin) → a usable **4.5 x 6.5in** content box. Keep the headline,
bullets, CTA phone, and brand tag entirely inside that box — nothing critical
within 0.25in of the trim line.

**Recommended layout (solves text-over-photo legibility at the same time):**
Don't float text directly on the photo edge-to-edge — that's where
readability breaks depending on what's behind it. Instead: let the AI image
fill the **top ~60%** of the card full-bleed (the emotional "wow" moment,
photo alone, no text on it), then anchor a **solid white rounded panel**
across the **bottom ~40%** containing the kicker, headline, service bullets,
trust line, and CTA. This guarantees 100% legibility regardless of the photo
underneath, and reuses the brand system's existing Panel/Callout components
(`brand-style-guide.md`) instead of a generic dark-gradient-scrim-on-photo
treatment — keeps this piece visually consistent with the doorstep flyer.

**EXPORT & final readability check:**
Export via Canva's Print/PDF option pre-sized to 5.25 x 7.25in, no margin,
bleed included. Before final export: zoom to 100% actual size and view from
~2–3 feet away (how a card is actually read, not how it looks zoomed-in on a
monitor); do a quick grayscale/B&W preview to check contrast independent of
color; if using a translucent panel anywhere, keep it at minimum ~80% opacity
white so text stays legible over the busiest part of the photo. Print one
physical proof and check it in daylight and indoor light before ordering the
full run.

## Notes
- Front-only design — back is intentionally blank white/uncoated for on-site
  handwritten quotes. Nothing to design there.
- Greenacres, FL is not yet in the ZIP shortlist in
  `../../docs/01-strategy/zip-code-targeting.md` — flagging in case this is a
  new target area worth adding, not just a one-off local card.