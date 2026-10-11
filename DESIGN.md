# Roundel Sim Club: Design Language

**Brand:** Roundel Sim Club, a social sim racing bar with twelve linked rigs in Columbus, OH (fictional)
**Concept:** *The race-car livery.* The site is painted like a 1970s endurance racer: big flat blue fields, red/white/yellow pinstripes, white number roundels and black pit boards. It feels like a night out, not a training facility.
**Audience:** Groups of friends, office parties, people who've never raced, plus a regular race-night crowd.
**Mood:** Loud, warm, sporty, a little cheeky. Bold rather than slick.

---

## 1. Core principles

1. **Livery first.** Large solid colour blocks, diagonal cuts between sections and thin tri-colour stripes. Paint on a car, not cards on a page.
2. **The roundel is the hero shape.** A white circle with a heavy black race number. Use roundels for dates, tier sizes, the logo and the hero. They're the only round elements on the site.
3. **Everything else is square.** No border radius anywhere except roundels. Use heavy 3–4px black borders on interactive and tabular elements.
4. **Expanded italic headlines.** Wide, heavy and slanted forward like lettering on a car door.
5. **Light, single theme.** The cool off-white sheet plus blue blocks is the identity. Don't make a dark variant.

## 2. Colour tokens

| Token | Hex | Use |
|---|---|---|
| `--blue` | `#1538C8` | Livery blue. Hero, header, footer, featured tier, eyebrows |
| `--ink` | `#0A1033` | Text, heavy borders, records section, "now racing" bar |
| `--sheet` | `#F2F4FA` | Page background (cool off-white, never cream) |
| `--white` | `#FFFFFF` | Roundels, parties section |
| `--red` | `#E3392E` | Stripe, eyebrow dash, bullets, "On track now" tag, roundel outer ring |
| `--yellow` | `#FFC81F` | CTAs, accent words in headlines, record times, featured-date roundel |
| `--blue-tint` | `#DCE3FF` | Body text on blue |
| `--slate` | `#9AA3D4` | Muted text on ink |
| `--rule` | `#C9CFE3` | Hairlines on the sheet |
| `--body-2` | `#3D4466` | Secondary body text on the sheet |

**Livery stripe:** a 14px band, red 5px / white 4px / yellow 5px. It sits under the header and above the footer.

## 3. Typography

| Role | Family | Settings |
|---|---|---|
| Display | **Anybody** (Google Fonts, variable `wdth 50–150`, `ital`) | Headlines: italic, weight 900, `font-stretch:150%`, UPPERCASE, line-height 0.9. Labels and nav: `font-stretch:62–75%`, weight 700–800, UPPERCASE, 0.04–0.2em tracking. Numbers in roundels and pit boards: upright 900, `font-stretch:62–72%` |
| Body | **Hanken Grotesk** | 400/500/700, 17px base, 1.55 line-height |

- The width axis is the main tool: **wide** for shouting, **narrow** for labels and numerals.
- Put the last line of the hero headline in yellow ("Twelve rigs. One bar. **Bring a grid.**").
- Eyebrows: a 28×4px red dash, then narrow uppercase text in blue.

## 4. Layout

- Max width 1400px. Gutter `clamp(16px, 4vw, 56px)`.
- **Header:** blue, 68px tall. Logo is a white roundel "12" plus "ROUNDEL" in expanded italic. Nav is narrow uppercase. CTA is a yellow block.
- **Hero:** full-bleed blue with the bottom edge cut on a diagonal (`clip-path: polygon(0 0,100% 0,100% calc(100% - 7vw),0 100%)`). Left: headline and copy. Right: a giant white roundel "12" with a blue gap and red outer ring (`box-shadow: 0 0 0 14px blue, 0 0 0 20px red`). Faint skewed speed-lines run along the cut.
- **"On track now" bar:** an ink strip that overlaps the bottom of the hero (negative margin). It starts with a red tag cell, then key/value cells for session, car/track and rigs free.
- The parties section opens with the opposite diagonal (`polygon(0 5vw,100% 0,…)`) so the sections read like panels on a car body.
- Section padding `clamp(64px, 9vw, 128px)`.

## 5. Signature components

- **Entry list (events):** like a race entry sheet, with a 4px ink top rule and hairline rows. Columns: a date roundel (day number + weekday, white with a 4px ink border; yellow for the featured event), title in expanded italic with a description, time/price meta, and a square "Join grid" button (3px ink border that inverts on hover).
- **Pit boards (lap records):** near-black slates `#05081C` with a 6px `#2A3060` frame and a hanger tab on top. Three stacked lines of narrow numerals (P1 / time in yellow / track code), then a dashed divider and the driver's name.
- **Bar menu:** two columns (Drinks, Food). Each item is an expanded italic name, a dotted leader and the price, with a description on the line below. Items are named after famous corners: Eau Rouge, Corkscrew, Parabolica.
- **Party tiers:** three columns inside one 4px ink frame, divided by 4px rules. Each tier starts with a roundel showing its rig count (6 / 12 / 24). The featured tier is blue with yellow bullets. Bullets are small square red blocks.
- **Flag rules:** a real flag swatch (blue, yellow, chequered via `repeating-conic-gradient`) on a black pole, with a short rule beside it.

## 6. Motion

- Almost none. Colour inverts on hover. The livery does the work.
- Don't animate on scroll.

## 7. Voice

- Friendly trash talk: "Bring a grid." "Settle it once and for all." "Buy the winner a drink if you punted them in turn one."
- Use motorsport vocabulary that a newcomer can still follow: grid, quali, stint, reverse-grid, chequered, steward.
- Inclusive. Make it clear beginners, kids' sessions and ladies' nights are welcome.

## 8. Don'ts

- No dark "gamer" look, RGB glow or carbon-fibre textures.
- No rounded corners except roundels.
- No gradients on surfaces. The only gradients are the stripe band and flag patterns.
- Don't use real team liveries or sponsor marks.
