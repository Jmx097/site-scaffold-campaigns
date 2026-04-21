# Proof Library

Single source of truth for every factual claim, statistic, named entity, or product capability cited on any of the four pages. If a claim appears on a page, it appears here first with a source.

---

## Rules for using this file

1. **Don't cite what isn't here.** If a section file introduces a new claim, stop and add it to this library first (with source). Silent claims without sources are forbidden.

2. **Strength levels.** Every claim is tagged:
   - **Validated** — we have direct evidence or documentation. Use freely.
   - **Industry benchmark** — from third-party research. Cite the source publicly.
   - **Our observation** — pattern we see in our own work, not externally validated. Use only if the wording makes the frame clear ("In our data…", "In our experience…").
   - **Pending** — we want to make this claim but don't yet have validation. DO NOT use until status changes.

3. **Named entities** use canonical spelling (see below). Typos or inconsistent capitalization are drift signals.

---

## Canonical product and entity names

Always spell these exactly this way. Consistency matters for AI-search ranking (entity recognition) and for brand credibility.

### Our stack
- **OpenClaw** (one word, capital O, capital C)
- **Claude Cowork** (two words; the product is "Cowork," Anthropic/Claude branding is the parent; use "Claude Cowork" in full on first mention, "Cowork" acceptable on subsequent same-paragraph mentions)
- **Apollo** (not "Apollo.io" in running prose, unless specifying the website)
- **Hunter** (not "Hunter.io")
- **HeyReach** (one word, capital H and R)
- **Smartlead** (one word, capital S)
- **ScaledMail** (one word, capital S and M)
- **n8n** (lowercase, always)

### Competing categories (when we reference them)
- **Instantly** (sending platform, Smartlead alternative)
- **Mailforge** (ScaledMail competitor)
- **Zapier, Make** (automation tools, lighter than n8n)

### Regulatory and industry frameworks
- **NERC CIP** (North American Electric Reliability Corporation Critical Infrastructure Protection)
- **OEB** (Ontario Energy Board)
- **CER** (Canada Energy Regulator)
- **AER** (Alberta Energy Regulator)
- **CASL** (Canadian Anti-Spam Legislation)

### Partner and customer entities
- **VersaFile** (the consulting company)
- **M-Files** (the ECM product; note the hyphen)
- **Plinko Solutions** or **Plinko** (same brand, "Plinko" acceptable after first mention)
- **OPG** (Ontario Power Generation) — large-utility example
- **Hydro One** — large-utility example
- **Northland Power** — IPP example
- **Bruce Power, Hydro Québec, AltaGas, Enbridge Gas** — additional enterprise examples

---

## Validated facts about our stack and process

### Plinko's outbound stack composition
**Claim:** Plinko's outbound engine runs on Apollo (firmographics), Hunter (email finding/verification), HeyReach (LinkedIn automation), Smartlead (email sending), ScaledMail (inbox provisioning), and a custom orchestration layer built on n8n and OpenClaw.
**Source:** Documented internally in `outreach-stack-audit.md` and `n8n-workflows/README.md`.
**Strength:** Validated.
**Allowed on:** All pages where the stack is relevant (tryplinko, dfyplinko). Reference in partial form on plinkoenergy (credit Plinko-side sourcing machinery without the full stack).

### Plinko's weekly routine automation
**Claim:** The weekly outbound routine (Monday 6am CRON → Apollo pull → scoring → HeyReach + Smartlead + WhatsApp call list) runs automatically via three n8n workflows triggered by a master signal sweep.
**Source:** `n8n-workflows/README.md`.
**Strength:** Validated (though workflows are being rebuilt for Smartlead — note as "in production" only after rebuild deploys).
**Allowed on:** dfyplinko (as proof of "we drink our own champagne"). Allowed on tryplinko as a generic "weekly routine" claim, less specific.

### OpenClaw + Cowork used for landing page drafting
**Claim:** The landing pages and sales infrastructure described are themselves built using the OpenClaw + Claude Cowork workflow.
**Source:** Meta-observation of Jon's process.
**Strength:** Validated.
**Allowed on:** dfyplinko (as the strongest possible proof moment — "the page you're reading was built with the stack we're selling you"). Do not overuse; once per page.

### VersaFile sector experience
**Claim:** VersaFile is Canada's M-Files implementation partner for the electric power, utilities, and midstream energy sectors.
**Source:** VersaFile's positioning; consulting work confirmed.
**Strength:** Validated.
**Allowed on:** versafilecanada (primary). plinkoenergy (as partner credit).

---

## Industry benchmarks (third-party — cite source publicly)

### Cold email reply rates (2026)
**Claim:** Average cold email reply rate across B2B in 2026 is approximately 3.43%. Signal-triggered sends see 1.2–3.2% meeting conversion vs. 0.3–0.6% for unsegmented cold lists.
**Source:** Aggregate of industry reports; exact citation TBD (Smartlead public benchmarks, Woodpecker 2025 report, and others).
**Strength:** Industry benchmark.
**Allowed on:** tryplinko, dfyplinko.
**Caveat:** Update citation before publishing if we want the stat on the page.

### LinkedIn Sales Navigator reply lift
**Claim:** InMail responses are 64% higher when Spotlight filters (behavioral signals like "posted recently," "changed jobs," "company growing") are used to narrow targeting.
**Source:** LinkedIn Sales Navigator internal research, referenced in our Sales Nav reference doc.
**Strength:** Industry benchmark (vendor-stated).
**Allowed on:** tryplinko, dfyplinko — when talking about why signal triggers outperform cold spray.

### MSP buyer count
**Claim:** There are approximately 40,000+ MSPs in North America (common figure). A subset of 10–50 employee MSPs is the focus.
**Source:** Generally accepted MSP industry counts (ChannelE2E, CompTIA reports).
**Strength:** Industry benchmark.
**Allowed on:** tryplinko, dfyplinko.

### Email deliverability on unwarmed domains
**Claim:** Unwarmed domains sending cold email see 40-70% spam folder placement in the first 30 days. 14-21 day warmup brings that to under 10%.
**Source:** Deliverability research — Glock, Smartlead, Instantly public benchmarks.
**Strength:** Industry benchmark.
**Allowed on:** tryplinko, dfyplinko as justification for "we run this on warmed infrastructure."

---

## Our observations (unvalidated externally — use with hedging)

### 2x more conversations claim
**Claim:** Book 2x more qualified conversations (vs. doing nothing or doing it half-time yourself).
**Source:** Our observation across current Plinko clients.
**Strength:** Our observation.
**Allowed on:** tryplinko, dfyplinko.
**Hedging required:** Frame as "in our data" or "what we see with current clients," not as "industry research."

### 3-5x signal triggered reply rate
**Claim:** Signal-triggered sends see 3-5x the reply rate of unsegmented cold lists.
**Source:** Combination of industry benchmark + our observation.
**Strength:** Our observation (extrapolated from industry benchmark).
**Allowed on:** tryplinko, dfyplinko.
**Hedging required:** "3-5x the reply rate of cold lists per 2026 benchmarks" is acceptable wording.

---

## Pending claims (DO NOT USE until validated)

### Claim: "90 days to first qualified pipeline"
**Status:** Pending. This is our offer promise on dfyplinko, not a validated delivery time across a sample. We need either (a) at least 3 completed engagements proving the timeline, OR (b) reframe as "target timeline" not "guarantee."
**Decision pending.**

### Claim: specific customer names on versafilecanada or plinkoenergy
**Status:** Pending per-customer approval. Do not name any utility or IPP as a VersaFile client on public web pages without explicit written approval from that customer's procurement/marketing contact.

### Claim: "first MSP to combine outbound and AI automation in a single DFY offer"
**Status:** Pending. We don't have evidence no other agency does this. Don't claim a "first." Fine to claim differentiation ("most AI consultancies don't touch outbound; most outbound agencies don't touch AI; we do both").

### Claim: specific ACV or ROI numbers for dfyplinko engagements
**Status:** Pending. No public ACV/ROI claims until we have ≥3 engagements' worth of data.

---

## Proof moments that don't require numbers

Structural proof — observable facts about our process that build credibility without benchmarks.

### "We drink our own champagne" (dfyplinko)
The single strongest proof moment available on dfyplinko. Facts:
- Plinko's own outbound is powered by the stack we're selling.
- The weekly routine runs automatically.
- The landing pages were drafted in this workflow.
- Internal reporting and attribution uses the same n8n layer we'd install for the MSP buyer.

Use once, prominently. Don't dilute by repeating.

### "Named stack, no black box" (tryplinko, dfyplinko)
Tool names in prose — Apollo, Hunter, HeyReach, Smartlead, OpenClaw, n8n, Claude Cowork. This is a proof moment in itself: agencies that hide the stack are either incompetent or trying to keep clients dependent. We name it.

### "Canadian context" (versafilecanada, plinkoenergy)
VersaFile knows OEB, CER, NERC CIP. US-based M-Files partners don't. This is a deliverable proof element — not a stat, but a structural fact.

### "Explicit anti-ICP" (all pages, especially dfyplinko)
"Not for MSPs under 10 employees," "Not for MSPs over 100," "Not for anyone looking for lead lists." Anti-ICP sections are proof that we know our market — not everyone has run them.

---

## Adding a new claim to this library

Pattern:

```markdown
### [Short name of claim]
**Claim:** [The claim as it would appear in copy.]
**Source:** [Where we got this. URL, internal doc, benchmark report, our observation.]
**Strength:** [Validated / Industry benchmark / Our observation / Pending]
**Allowed on:** [Which pages this can appear on.]
**Hedging required:** [If any. Only for "Our observation" claims.]
```

---

## Audit cadence

Review this library:
- Before first publish of any page
- Every quarter (stale "Our observation" claims should promote to "Validated" or drop off)
- Whenever a new ICP or motion is added
