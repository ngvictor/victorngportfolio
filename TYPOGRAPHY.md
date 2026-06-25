# Typography Standard

The single source of truth for **type** on this portfolio. Applies to **every page**:
`index.html`, `project-playable-ads.html`, `project-ai-workflows.html`, and
`project-horizon-vr.html` (when built).

For color, spacing, motion, and components, see **[DESIGN.md](DESIGN.md)**.

Distilled from **Pierrick Calvez — "A Five-Minute Guide to Better Typography"**
(<https://www.pierrickcalvez.com/journal/a-five-minute-guide-to-better-typography>),
then translated into concrete rules for this codebase's tokens and components.

> Typography is the technique of arranging type for effective communication —
> and a bit of delight.

---

## The one-screen summary

Calvez's closing slide, in order. When in doubt, walk this list top to bottom:

1. **Don't nerd over typefaces — pick one.** (Done: Instagram Sans.)
2. **Think of type as blocks**, not individual letters. Squint: judge the grey shapes.
3. **Align with your eyes.** It's aligned when it *feels* aligned.
4. **Hierarchy first.** Establish the levels before anything else.
5. **Use contrast.** Make different things clearly different.
6. **Fine-tune with spacing.** Line-height, measure, tracking. Then *voilà*.

Everything below is the detail behind these six.

---

## 1. One typeface, four weights

The guide: *"Start with one typeface. Pick one that has lots of weights. Four at least."*
Light + Regular + Medium + Bold **equals a typeface.**

We use **Instagram Sans**, self-hosted, with exactly those four weights. This maps
1:1 onto the rule — no second family needed.

| Weight | Value | `@font-face` file | Use for |
|--------|-------|-------------------|---------|
| Light | 300 | `InstagramSans-Light.ttf` | Large display / hero only (sparingly) |
| Regular | 400 | `InstagramSans-Regular.ttf` | Body copy, captions |
| Medium | 500 | `InstagramSans-Medium.ttf` | Subheads, labels, UI, emphasis |
| Bold | 700 | `InstagramSans-Bold.ttf` | Headings, the loud moments |

- Token: `--sans: 'Instagram Sans', 'DM Sans', system-ui, sans-serif`
  (DM Sans stays only as a fallback while fonts load).
- `--serif` points at the same stack — we are intentionally a **one-family** site.
- **Do not add a third weight family or a decorative face** without revisiting this doc.
  "Don't nerd over typefaces."

---

## 2. Hierarchy — the two "in doubt" rules

Hierarchy is built from **two levers only: size and weight.** The guide gives a
concrete default for each.

### Size: *in doubt, multiply by two*
Calvez's example steps 100pt → 50pt → 25pt. Double (or roughly double) between
levels so the jump is unmistakable. Our scale:

The clamps below are mirrored from the CSS for reference — **the stylesheets are
canonical.** What matters is the *ratio*: roughly double between levels. If you change
a size, change it in the CSS; this table follows.

| Role | Size (desktop) | Weight | Line-height |
|------|----------------|--------|-------------|
| Stat-band number | `clamp(3.25rem, 7vw, 5.5rem)` | 400 (serif token) | 1.0 |
| Display / hero H1 | `clamp(3rem, 6vw, 5rem)` | 400–700 | 1.05–1.15 |
| Section title (H2) | `clamp(2.25rem, 4vw, 3.25rem)` | 600 | 1.08 |
| Subhead (H3) | `clamp(1.75rem, 2.8vw, 2.15rem)` | 600 | 1.2 |
| Lead / tldr | `clamp(1.5rem, 2.4vw, 1.875rem)` | 400–500 | 1.45 |
| Body | **1.375rem (22px)** | 400 | 1.5–1.6 |
| Table / dense data | 1rem (16px) | 400–600 | 1.4 |
| Caption / label | 0.9375rem (15px) | 400 / 500 | 1.6 |

Adjacent levels should differ enough to read instantly. If two sizes look "close,"
they're too close — push them apart.

### Weight: *in doubt, skip a weight*
For weight contrast, jump Bold → Medium → Light and **skip the rung between** so the
contrast is visible. Bold heading, Medium subhead, Light/Regular body. Don't set a
heading in Medium next to body in Regular and expect it to carry — the gap is too small.

> Rule of thumb: never lean on size *and* weight being subtle at the same time.
> One of them should be doing obvious work.

---

## 3. Readability — measure, size, leading

### Measure (line length): 40–70 characters
*"Tame the flow. Use between 40 and 70 characters per line."* Too wide and the eye
loses the next line's start.

- Body text blocks get a **max-width of ~`66ch` (≈ 620–720px)**. Never let prose run
  the full 1280px page width.
- Current note: `.media-caption` is capped at `820px`. At 15px that's ~75–80 chars —
  slightly over. Prefer `max-width: 70ch` for any multi-line caption or paragraph.

### Body size: a large 22px
*"12px is too small. 14–25px is better."* Body copy on this portfolio is **1.375rem
(22px)** — a deliberately large, editorial reading size near the top of the guide's
range. Everything else keys off it: subheads must clear it (H3 ≈ 28–34px, not 22px),
and secondary text steps down — **1rem (16px)** is the floor for dense UI like tables,
15px is fine for short captions/labels but not for reading passages.

### Line-height (leading): 1.2× to 1.5×
*"In doubt, use a line-spacing of 1.2× to 1.5× the font size."* And it scales with
line length:

- **x1.2 for short paragraphs** (and headings can go tighter, ~1.05–1.2).
- **x1.5 for long-form reading** (case-study body copy → `line-height: 1.5–1.6`).
- Big display type: tighten toward 1.05–1.15 so lines don't drift apart.

Not too tight, not too loose — the guide's "Naa / Noo" test. Squint; the lines should
feel evenly spaced, neither cramped nor floating.

---

## 4. Alignment

*"Type is not an exact science. It is aligned when it feels aligned. Realign if
necessary."* And the safe default: **"In doubt, align left."**

- **Body and long-form: always left-aligned, ragged right.** Never justify on the web.
- **Centered is allowed only for short display text** — the homepage hero, a section
  lead, a pull-quote. The moment it's more than ~2 lines, left-align it.
- Trust the eye over the math: if a centered block *looks* off, nudge it until it feels
  right, even if the numbers say it's centered.

---

## 5. Punctuation

*"Now for some nerdy stuff."* Use real characters, not keyboard approximations.

- **Curly quotes** `" "` `' '`, never straight `" '`.
- **Real apostrophe** `'` (don't → don't).
- **The three dashes — know which is which:**

| Mark | Char | Use |
|------|------|-----|
| Hyphen | `-` | Compound terms: `full-moon`, `time-out`, `one-of-a-kind` |
| En dash | `–` | Ranges & connections: `2018–2024`, `London–Paris` |
| Em dash | `—` | **Avoid in body prose.** See the project rule below. |

> **Project rule — no em dashes in body copy.** This portfolio's writing is actively
> de-AI'd, and a sprinkle of em dashes is the loudest "this was drafted by an LLM" tell.
> The em dash is sanctioned in **exactly one place: the page H1 title**
> (e.g. "Playable Ads — A new ad format for Meta"). Everywhere else, restructure: use a
> colon, a full stop, a comma, or parentheses. When in doubt, two short sentences beat
> one em-dashed clause. (This overrides the generic guide, which permits em dashes freely.)

---

## 6. The fine detail

### Think in blocks
*"Type is a beautiful group of letters, not a group of beautiful letters."* Evaluate a
text block as a **shape and a grey value**, not letter by letter. Squint at any screen:
the blocks should sit in a clear rhythm with even spacing between them.

### Kerning / tracking
*"Finally, pay attention to kerning"* (and beware **"keming"** — letters spaced so badly
they read as the wrong word). On the web we don't hand-kern, but we do control **tracking**:

- **All-caps labels get positive letter-spacing** (`0.12–0.15em`) — e.g. `.section-label`
  already uses `0.14em`. Caps look cramped without it.
- **Large display headings get slightly negative tracking** (`-0.01 to -0.02em`) so big
  type doesn't feel loose. Body text: leave tracking at 0.

---

## Per-page checklist

Apply to every page before shipping:

- [ ] One family only — `--sans` (Instagram Sans). No stray font-family declarations.
- [ ] Heading → body contrast obvious in **both** size (≈2×) and weight (skip a rung).
- [ ] Body copy 16–18px, line-height 1.5–1.6, max-width ~66–70ch.
- [ ] Headings tracked tight (-0.01/-0.02em); all-caps labels tracked open (+0.14em).
- [ ] Long text left-aligned; centering only for short display lines.
- [ ] Curly quotes, real apostrophes, en dashes for ranges, hyphens for compounds.
- [ ] **No em dashes in body copy** — only the H1 title is allowed one.
- [ ] Squint test: blocks read as clean shapes with even spacing.

---

*Source: Pierrick Calvez, "A Five-Minute Guide to Better Typography."
Adapted as this project's standard. When a new question comes up, answer it the way the
guide would: communicate clearly first, delight second.*
