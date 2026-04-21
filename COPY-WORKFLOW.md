# Copy Workflow — Recursive Section Writing

The process for producing landing page copy across the four domains. Not just a file layout — a discipline that prevents context drift, compounds proof across pages, and makes rewrites safe.

---

## Why this exists

V1 copy (`landing-page-copy.md` at the project root) was drafted in one pass. It's serviceable but not refined — no formal critique, no rewrite pass, no shared source of truth for positioning or voice.

V2 is built using recursive section writing: every section passes through intent → draft → critique → rewrite → locked before anything gets assembled into a page. Every page draws from the same shared foundation (positioning, voice, proof, CTA rules) so the four domains feel like a family, not four strangers.

---

## File structure

```
landing-pages/
├── COPY-WORKFLOW.md          ← you are here
├── README.md                  ← Vercel deploy guide (HTML implementation)
│
├── shared/
│   ├── positioning.md         ← the four motions, how they relate, buyer narratives
│   ├── voice-and-guardrails.md ← tone rules per page, words to use / avoid
│   ├── proof-library.md       ← every factual claim, stat, or named entity we can cite
│   └── cta-rules.md           ← CTA hierarchy, placement, UTM conventions
│
├── versafilecanada/
│   ├── brief.md               ← ICP, anti-ICP, goals, acceptance criteria
│   ├── sitemap.md             ← section order and per-section intent
│   ├── hero.md                ← Intent → Draft → Critique → Rewrite → Locked
│   ├── pain.md                ← same structure (N/A noted if section not used)
│   ├── solution.md
│   ├── process.md
│   ├── faq.md
│   ├── cta.md
│   ├── assembled-copy.md      ← final copy once all sections lock
│   ├── index.html             ← implementation (currently V1; updated after lock)
│   └── vercel.json
│
├── plinkoenergy/    (same shape)
├── tryplinko/       (same shape)
└── dfyplinko/       (same shape)
```

---

## The recursive process — how to write any section

For every section file (`hero.md`, `pain.md`, etc.), work top-down:

### 1. Intent (never skip)

What this section must do for the reader. What they must feel, understand, or decide before they scroll past.

One paragraph. Written before any copy.

Example from `versafilecanada/hero.md`:
> The Enterprise ECM buyer has arrived from cold email. They have 8-12 seconds before deciding if this is real or marketing spam. Intent: prove this is a serious Canadian M-Files partner who works at their regulatory scale, within one scroll. No fluff, no AI-stock-photo energy.

### 2. Draft

First pass. Often the V1 copy from `landing-page-copy.md`. No critique yet — just get words on the page.

### 3. Critique

Honest read of the draft against intent. Specifically ask:
- Does the opening line earn the next scroll?
- Would the target buyer (specific persona from brief.md) actually say this out loud?
- Is there a single hedge word ("we think", "may be able to", "typically") that kills trust?
- Is every claim cited in `shared/proof-library.md`? If not, is it removed or promoted to a claim with source?
- Does anything overlap another section? Merge or cut.
- Voice check against `shared/voice-and-guardrails.md`.
- One sentence the reader could highlight and quote — is it there?

Bulleted list. Specific. Not "feels weak" — "the third paragraph hedges with 'may be able to' — promote or cut."

### 4. Rewrite

Revised draft addressing every critique bullet. Not a polish pass — a re-think when the critique demands it.

If the rewrite barely changed the draft, the critique wasn't honest. Go back.

### 5. Locked

Approved final. This is what goes into `assembled-copy.md` and then into the HTML. Lock is a decision — "this is good enough to ship." Subsequent edits create a new rewrite pass, not silent edits to the locked block.

---

## Rules of the road

### Shared foundation is authority

Anything in `shared/` governs the per-page files. If `voice-and-guardrails.md` says "no marketing superlatives," a section file saying "the best ECM partner" loses. Fix shared first, then fix the section.

### Proof library is the single source of truth for claims

Every statistic, named company, regulatory framework, or product claim on any page must appear in `shared/proof-library.md` with a source. If you need a claim not in the library, add it there first (with source), then cite it.

### Don't write the same thing twice

If "signal-triggered sends" appears on three pages, write the definitive version once in `shared/positioning.md` and reference it. Per-page variation happens in the critique/rewrite pass, not in parallel independent drafts.

### Lock is contractually binding

Once a section is locked, don't edit it without going through critique → rewrite. Silent edits are how copy drifts. If V2 HTML is built and you want to tweak a headline, open a new rewrite pass explicitly.

### Briefs block sections

Don't write a section file for a page whose `brief.md` isn't locked. The brief defines ICP, promise, and acceptance criteria — without it, section intent is guesswork.

---

## Build order for the four pages

Recommended order for the first V2 pass, driven by strategic priority:

1. **versafilecanada** — enterprise anchor, highest-stakes tone, sets the "serious" pole
2. **dfyplinko** — the new positioning pivot (outbound + OpenClaw/Cowork), sets the "committed" pole
3. **plinkoenergy** — combines VersaFile formality with Plinko warmth, calibrated against the two poles
4. **tryplinko** — casual sibling of dfyplinko, calibrated against the committed pole

Within each page, work sections in publish order: hero → (whatever comes next per sitemap).

---

## Handoff to implementation

When all section files on a page are locked and `assembled-copy.md` is populated:

1. Read `assembled-copy.md` alongside existing `index.html`
2. Update HTML section-by-section, preserving current structure where possible
3. Re-deploy via Vercel
4. Check UTM + Cal.com attribution still work (regression from HTML edits)
5. Move to next page

HTML structure/styling decisions happen during implementation — not in the copy files. Copy files are format-agnostic prose.

---

## When to update shared files

Shared files evolve. Signals that shared files need an edit:

- A critique keeps raising the same voice question across multiple sections → add a rule to `voice-and-guardrails.md`
- A proof claim appears on multiple pages with slightly different numbers → canonicalize in `proof-library.md`
- A new page motion needs positioning that doesn't fit any existing narrative → add it to `positioning.md`

When shared files change, re-critique any sections that rely on them. Tedious but that's the point — shared changes should propagate.

---

## What this prevents

- **Context drift:** six weeks in, a new page pulls copy from three old pages and contradicts all of them. Shared foundation stops this.
- **Silent rewrites:** "I just tweaked the headline" turns into a month of un-reviewed edits that dilute the original intent. Lock + explicit rewrite passes stop this.
- **Unsubstantiated claims:** "2x more conversations" sits in three drafts before someone notices it has no source. Proof library stops this.
- **Voice slippage:** VersaFile copy starts sounding like Plinko copy because the writer forgot which page they're on. Voice-and-guardrails stops this.
- **Section rework:** changing the hero forces rewriting three other sections that referenced the hero's framing. Sitemap intent declarations stop this.
