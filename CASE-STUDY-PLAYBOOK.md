# Case Study Playbook

How to write and review a case study on this portfolio so it survives a busy
hiring manager. Apply to **every** project: `project-playable-ads.html` (the
worked example below), `project-ai-workflows.html`, `project-horizon-vr.html`,
and anything new.

Pairs with **[TYPOGRAPHY.md](TYPOGRAPHY.md)** (how the words look) and
**[DESIGN.md](DESIGN.md)** (color, space, motion, components). This doc is about
what the words *say* and how the story is *structured*.

> Synthesized from a hiring-manager review lens, a senior reviewer's structural
> feedback on the playable-ads study, the de-AI writing pass, and 2026
> portfolio-review research (Suska's 1000-portfolio review, UX Playbook's
> senior-hiring guide, Atlassian on process-over-outcome). When a new question
> comes up, answer it the way this doc would.

---

## The 1-minute test

Review every draft as the reader who matters: a **cynical, time-poor Principal
Designer or hiring manager** who gives it about **a minute** before deciding to
keep reading or move on, allergic to generic diagrams, buzzwords, and walls of
text. Score it on three pillars before anything else:

1. **Scannability** — can they tell the business impact in **10 seconds**?
2. **Ambiguity** — did you prove you can thrive in **low context** (no PM, no brief)?
3. **Craft** — does the UX execution read as **senior-level**?

For each pillar: gut reaction, what to **cut**, what to **expand**, where it
**sounds too academic**. No softening.

---

## 1. Structure — answer first (Minto)

Lead with the conclusion, then support it. The reader should never have to wait
for the setup to finish.

- **Metrics first.** Put the impact up top, right after the hero, before the
  story. Frame it as "here's what changed, here's how." Don't bury numbers in a
  closing section.
- **State the problem as the *user's* obstacle, early.** Not the org chart, not
  the market first — the human who couldn't do the thing. Market/competitor
  context is support, so it comes *second*.
- **Cut the setup.** Kill scoping play-by-play ("the one-pager, the success
  criteria"), throat-clearing ("the bar was simple"), and anything a reader would
  just ask about if they cared. Leave the meaningful 20%.
- **Name the scale.** If it ships to billions, say so. Tie the work to the wider
  ecosystem — reviewers can't infer reach you don't state.
- **Include non-metric impact.** Platform influence, adoption with zero extra
  cost, a competitor/partner reaction, a new category opened. These count.
- **Don't end at handoff.** Most portfolios stop at the shipped screen; senior
  ones own the outcome. Show what happened after launch, the real follow-up
  iteration, and how results compared to what you predicted. A short "what I'd
  iterate next" beat is one of the clearest seniority signals there is.
- **One project, one core problem.** Each study needs a single spine. If it
  sprawls across three problems it dilutes the signal and skimmers bail. Reviewers
  give a study three to five minutes — cut to the one decision that mattered most.

## 2. Voice — ownership without overclaiming

- **"I" language, plus cross-functional framing.** Show how you moved leadership
  and partners. "I worked with the format owners," not "the feature was approved."
- **Never "approved" / "got greenlit."** Passive-credit words hand ownership
  away. Say what *you* did: "the version we took live," "I made the case for."
- **Frame section titles at the altitude of what you did**, not clever-vague.
  "Designing for Two User Groups" beats "Designing Against the Pattern" — a reader
  shouldn't have to decode the title.
- **Frame what you cut as strategy, not confession.** "It got rejected. I agreed
  with the call." reads as senior, but go further: say *why* you cut it and what
  you traded off. Prioritization reasoning ("I killed playables-on-impression
  because the post-click tap is load-bearing") is core senior evidence.
- **Show influence without authority.** Senior work gets done through other
  people. Even with no direct reports, make the cross-functional moves explicit:
  how you moved a review, won over a partner, shifted a roadmap. That thread *is*
  the leadership story.

## 3. Writing — de-AI pass

The dominant tell that copy was AI-drafted is **repetition**, not word choice.
Fix structure first, then phrases.

- **Each fact gets ONE home.** Before shipping, count how often a stat, a phrase,
  or a list (e.g. "Feed, Stories, Reels") repeats across sections. Pick the best
  home for each and delete the echoes. One deliberate repeat is fine; five is not.
- **Kill the phrase tics:**
  - "X, not Y" / "wasn't X, it was Y" antithesis (worse with alliteration)
  - Textbook transitions: "But there was a nuance in the data"
  - Restated transformation arcs: "from a dead experiment into a live format"
  - Consultant compounds: "bridged a trust gap," "highest-leverage move,"
    "reduces the barrier to," "converted with more intent"
  - Press-release verbs: "opened up a new collaboration with"
  - Soft marketing words: "seamless," "flow," "experience"
  - Hedges: "I'm oversimplifying here"
- **Punctuation:** no em-dashes in body prose (the H1 title is the only sanctioned
  one). Curly quotes, real apostrophes, en dashes for ranges. See [TYPOGRAPHY.md](TYPOGRAPHY.md).
- **Keep the human fingerprints:** specific numbers, "vibe-coded in Figma Make,"
  "cheap to kill," concrete dialogue ("when can we test it"), opinionated first
  person ("I fought for…"). Don't sand these off while de-AI-ing.

## 4. Craft — let the work be seen

- **Screenshots ~1.5× larger, with whitespace** so detail is legible. Cramped
  half-column images undersell the work.
- **No arrows, guides, callout lines, or tooltips baked into design shots** — they
  cheapen the craft. Annotate in the caption or surrounding prose instead.
- **Real interaction recordings** beat static frames (e.g. the format running on a
  phone). Add them where you have them.
- **One-line captions** under media, in `--ink-muted`, centered, tight to the image.

---

## Worked example — playable-ads, before → after

| Lever | Before | After |
|-------|--------|-------|
| Metrics | Grid buried in §04 | "Impact" strip right after the hero |
| Problem | Opened on the market stat | Opens on the user obstacle ("People don't install an app they've never tried") |
| Setup | "unfunded experiment… the bar was simple…" | "It started from zero: just me and one engineering partner…" |
| Title | "Designing Against the Pattern" | "Designing for Two User Groups" |
| Voice | "the approved dual-CTA design" | "the dual-CTA design we took live" |
| Scale | unstated | "Scale: billions of people across both apps" in the metadata |
| Non-metric | absent | the Android overlay I designed prompted Google to build a native one |
| Visuals | half-column | 40/60 split, media at 60% |

---

## Pre-ship checklist

Walk this top to bottom before shipping any case study:

- [ ] Business impact readable in 10 seconds, metrics near the top.
- [ ] One project, one core problem — no sprawl; readable in 3–5 minutes.
- [ ] First problem statement is the *user's* obstacle, not the market.
- [ ] Setup/scoping trimmed to the meaningful minimum (Minto).
- [ ] Scale and ecosystem named; non-metric impact included.
- [ ] Story goes past handoff: post-launch result + what you'd iterate next.
- [ ] "I" + cross-functional voice; zero "approved"/"greenlit."
- [ ] Cuts framed as prioritization (why + trade-off), not just confession.
- [ ] Influence-without-authority thread visible (moved a review, partner, roadmap).
- [ ] Section titles describe what you did, not clever-vague.
- [ ] Repetition audited — each fact has one home.
- [ ] No phrase tics; no em-dashes in body; human fingerprints intact.
- [ ] Screenshots large with whitespace; no baked-in arrows/guides/tooltips.
- [ ] Real recording included where one exists.

---

*A case study's job is to prove, in about a minute, that you drive impact in low
context and execute at a senior level. Everything above serves that.*
