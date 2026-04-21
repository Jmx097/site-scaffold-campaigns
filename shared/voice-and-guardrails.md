# Voice & Guardrails

Per-page voice calibration and word-level rules. Every section file is checked against this during Critique.

---

## Voice dimensions

Each page gets a rating on three dimensions. The section-level Critique step uses these ratings to catch tonal drift.

**Formality:** 1 = peer Slack message, 5 = enterprise RFP response
**Technical density:** 1 = avoids jargon entirely, 5 = assumes domain fluency
**Assertiveness:** 1 = gentle, humble, options-based, 5 = direct, committed, opinionated

| Page | Formality | Technical | Assertiveness |
|---|---|---|---|
| versafilecanada.com | 5 | 4 | 3 |
| plinkoenergy.com | 4 | 4 | 3 |
| tryplinko.com | 2 | 3 | 3 |
| dfyplinko.com | 3 | 4 | 5 |

---

## Words and phrases we **never** use

These are trust-killers or tells of generic marketing drift. If one appears in a section, the Critique should catch it and the Rewrite should remove it.

### Weasel and hedge words
- "We think", "we believe", "we feel"
- "May be able to", "could potentially", "should help"
- "In our opinion" (just state the opinion)

### Marketing superlatives
- "Best-in-class", "world-class", "industry-leading"
- "Cutting-edge", "next-generation", "revolutionary"
- "Game-changing", "disruptive"
- "Seamless" (almost always false)

### Empty transitions
- "At the end of the day"
- "Simply put" (nothing is simple)
- "That's why we..."
- "We're passionate about..."
- "It's all about..."

### Generic agency/consulting speak
- "Leverage synergies", "strategic alignment"
- "Holistic approach"
- "We partner with you on your journey"
- "Unlock potential"
- "Transform your business"
- "Drive outcomes" (what outcomes?)
- "Best practices" (whose?)
- "Turnkey" (say what's included)

### AI-hype vocabulary (especially risky on dfyplinko)
- "Revolutionize"
- "AI-powered everything"
- "The future of [X]"
- "Harness the power of AI"
- "Intelligent automation" (say what it does)

### False urgency / pressure
- "Limited time", "act now"
- "Don't miss out"
- "Book before slots fill up"

---

## Words and phrases we **favor**

### Concrete specifics
- Named companies (e.g., OPG, Hydro One — if approved; or generic if not)
- Named tools (Apollo, HeyReach, Smartlead, OpenClaw, Claude Cowork, n8n, M-Files)
- Named frameworks (NERC CIP, OEB, CER)
- Named personas ("records manager," "engineering doc control lead")
- Actual numbers with units

### Direct, structural prose
- "We do X. You do Y. The result is Z."
- "What we actually run:" followed by concrete items
- "Worst case:" to set a floor on downside
- "Here's the truth:" when introducing an honest counter-claim

### Acknowledgment of trade-offs
- "Not for everyone."
- "Skip this call if…"
- "This won't work if…"
- Explicit anti-ICP sections build more trust than trying to sound universal.

---

## Punctuation and formatting rules

### Dashes and hyphens
- Use em dashes (`—`) sparingly for emphasis or parenthetical. Not as a sentence connector pattern.
- Use en dashes (`–`) for number ranges: "100–500 employees."
- Use hyphens (`-`) for compound modifiers: "signal-triggered sends."

### Lists
- Bulleted lists: reserve for genuinely parallel items. Not as a substitute for prose.
- Numbered lists: only when sequence matters or when the reader will count.
- Avoid nested lists in copy files. (HTML can render depth, but source prose should be flat.)

### Emphasis
- **Bold** for the single most important claim in a block. One per paragraph, max.
- *Italic* for product names, publication names, specific quoted phrases.
- NEVER ALL CAPS except for product names with established all-caps (none in our stack).

### Contractions
- Use contractions except in the most formal section (versafilecanada.com hero and formal blocks).
- "We've deployed" reads as confident; "We have deployed" reads as stilted.

---

## Per-page voice notes

### versafilecanada.com
- Measured. No exclamation points anywhere on the page.
- One sentence ≥ 20 words is allowed in formal blocks; two in a row is not.
- Regulator names (NERC, OEB, CER) are name-dropped but never overused — twice per section max.
- Avoid any phrase that sounds like an agency pitch ("We partner with…", "We help companies…").
- Voice test: if this could appear in a Canadian Crown corporation's RFP response without edits, tone is right.

### plinkoenergy.com
- Warmer than versafilecanada but more deferential than tryplinko. Mid-market buyers feel talked-down-to by enterprise tone and over-promised-to by agency tone. Split the difference.
- "Peer-to-peer Canadian" is the voice — not American-agency, not enterprise-consultant.
- Light use of second-person: "If that's you" is fine; "You deserve better" is not.
- Avoid gushing about the VersaFile partnership. Credit it once (in How It Works), reference once more (in footer), done.

### tryplinko.com
- Casual but crisp. Not flippant. MSP owners are busy, skeptical, and done with BS.
- Sentence fragments are allowed: "Not Tuesday at 9 a.m. because 'that's when people check email.'"
- Named tools are a proof moment — don't hide the stack.
- Self-aware punchlines are OK if they're accurate: "You know why that gap exists."
- Voice test: if an MSP founder forwarded this to another MSP founder without cringing, tone is right.

### dfyplinko.com
- Most assertive. Most confident. This is the page where we tell the buyer exactly what we'll do and when.
- Strong declarative sentences. Short. Structural.
- Negative qualifications work: "No long contract." "Not for MSPs under 10." "Not a lead list."
- **AI-search legibility takes precedence over cleverness.** Every key entity (OpenClaw, Claude Cowork, MSP, AI automation) should appear in prose, not just in metadata. Use the phrases the target buyer would search.
- Use natural-language Q&A format in the FAQ — this is what AI search crawlers weight.
- Voice test: if the copy passed through Perplexity's "summarize this page" and produced a clean three-sentence summary with "OpenClaw" and "Claude Cowork" in it, we're on target.

---

## Cross-page voice consistency

Despite the per-page variance, some things stay the same across all four:

1. **Honest anti-sell.** Every page names who it's NOT for. This is a Jon-brand trust signal, not a trope to skip.

2. **Specific over generic.** Every claim is as specific as we can make it without overstating. "100-500 person utilities" not "mid-market utilities." "3-5x the reply rate of cold lists per 2026 benchmarks" not "much better reply rates."

3. **No CTA shame.** Each page ends with the CTA, confidently. No "we know you're busy, but if you have a minute…" energy.

4. **Plain language over sophisticated vocabulary.** "Document control" beats "information lifecycle stewardship." "We source the conversation" beats "we facilitate discovery engagements."

5. **Contractions on all pages except the versafilecanada hero.** Formal tone doesn't mean Victorian.

---

## Voice violation examples (anti-patterns to catch in Critique)

### Drift toward marketing generic
> **Bad:** "VersaFile is a trusted partner that helps Canadian energy companies transform their document management."
> **Why:** "Trusted partner" is generic. "Helps X transform" is agency-speak. No specific claim.
> **Fix:** "VersaFile has deployed M-Files across Canadian electric utilities, crown corporations, and midstream operators. We configure, deploy, and stay."

### Hedge killing the claim
> **Bad:** "We may be able to help MSPs book more meetings."
> **Why:** "May be able to" is a hedge. It's the first phrase a skeptical reader cuts.
> **Fix:** "We book qualified MSP conversations. 2x the volume of a cold-sequence-from-Gmail approach, per our 2026 data."

### Superlative without substance
> **Bad:** "Our cutting-edge AI automation delivers seamless results."
> **Why:** "Cutting-edge," "seamless" — two superlatives in one sentence. Says nothing.
> **Fix:** "We set up OpenClaw + Claude Cowork for your ticket triage, client onboarding docs, and weekly reporting. Running in 90 days. Same stack we use for our own outbound."

### Over-personal peer talk in an enterprise context
> **Bad (on versafilecanada):** "Hey, we get it — audits are brutal. Let's chat."
> **Why:** Tonally wrong for Motion 1. Enterprise buyers reject this.
> **Fix:** "If your team is preparing for a regulatory audit, a 15-minute intro is the lowest-friction way to see if we're worth a longer conversation."

### Under-personal formality on the MSP page
> **Bad (on tryplinko):** "Plinko Solutions provides comprehensive outbound services for small-to-medium managed service providers."
> **Why:** Reads like a PR boilerplate. MSP founders scroll past.
> **Fix:** "A complete outbound engine for MSPs that can't justify a full BDR team."

---

## Process reminder

Voice rules apply to every section during Critique. Don't assume the draft is on-tone — check it explicitly against this file. If a draft repeatedly drifts in the same direction, that's a signal to either (a) update this file with a new rule, or (b) re-read the section intent because the draft may be solving the wrong problem.
