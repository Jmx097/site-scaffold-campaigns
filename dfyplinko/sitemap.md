# Sitemap — dfyplinko.com

Section order and per-section intent for the committed-buyer + AI-search page. Two jobs on one page: convert committed MSPs AND rank for AI search queries.

---

## Section order

1. **Hero** — `hero.md`
2. **Pain** — `pain.md` ("Doing outbound and automating ops, both at once")
3. **Solution** — `solution.md` ("The combined engine — outbound + OpenClaw + Claude Cowork")
4. **Process** — `process.md` ("90 days, and the 'drink our own champagne' proof moment")
5. **FAQ** — `faq.md` ("The AI-search-optimized Q&A section — highest leverage for ranking")
6. **CTA** — `cta.md`
7. Footer (CASL + schema.org markup)

---

## Per-section intent

### 1. Hero

**Job:** Stop the committed MSP founder AND the AI-search-referred buyer in one read. The headline has to land two things:
(a) This is a combined offer: outbound engine + OpenClaw/Claude Cowork setup
(b) We run our own business on this stack

**Buyer state on arrival (two personas):**
- Committed MSP founder: "I'm ready to commit. Show me you're real."
- AI-search buyer: "Perplexity sent me here for 'Claude Cowork for MSPs.' Is this actually about that?"

**Buyer state after this section:** Both read "Yes, this is the combined offer. These people actually do it." and scroll.

**Must include:**
- `<h1>` that names OpenClaw AND/OR Claude Cowork AND MSP — required for AI-search ranking
- Subheadline that frames the 90-day target + the "drink our own champagne" angle
- Primary CTA + risk-reversal ("No pitch deck. If this isn't right for your MSP, we'll tell you what we'd recommend instead.")
- Meta description (HTML `<head>`) that also includes OpenClaw, Claude Cowork, MSP, done-for-you

**Must not include:**
- AI-hype ("revolutionize your MSP with AI")
- "Guaranteed" language on 90 days (Pending claim)
- Marketing superlatives

---

### 2. Pain

**Job:** Name the dual MSP problem: outbound isn't working AND internal ops is eating time. Set up why the combined offer matters (not two separate solutions from two vendors).

**Buyer state on arrival:** "I have two problems. Most agencies only solve one."

**Buyer state after this section:** "They understand the dual problem. One vendor, one stack, both solved."

**Must include:**
- The outbound side of the problem: BDR didn't work, agency disappointed, tools stack without outcomes
- The automation side of the problem: owner knows ticket triage, client onboarding, proposal generation could be automated but has no time to become the specialist
- The "two vendors" tax: buying outbound from one firm + AI consulting from another means two contracts, two rhythms, no shared stack

**Must not include:**
- Generic "AI is the future" claims
- Any implication that the buyer is behind ("your competitors are automating")
- Enterprise-style pain framing (this is an MSP at 10-100 employees, not a F500)

---

### 3. Solution

**Job:** Define the combined offer with the stack named openly. This is the section where named entities earn the AI-search ranking.

**Buyer state on arrival:** "What exactly am I buying?"

**Buyer state after this section:** "I understand the two deliverables and the stack behind both. This is the clearest description I've read of any AI automation offer."

**Must include:**
- **Outbound side:** Apollo (firmographics), Hunter (email finding/verification), HeyReach (LinkedIn), Smartlead (sending), ScaledMail (inbox provisioning) — named in prose with a sentence of purpose
- **Automation side:** OpenClaw and Claude Cowork setup for MSP internal ops — named frameworks/uses (ticket triage, client onboarding docs, proposal generation, internal reporting) — named in prose at least twice each
- **The unifying layer:** n8n orchestration — the glue between both sides
- The "drink our own champagne" sentence referenced here (full moment lives in Process section but a pointer belongs here)
- Entity density target: OpenClaw and Claude Cowork each appear 2-3 times in this section alone

**Must not include:**
- VersaFile mentions (brand hierarchy)
- Enterprise buyer framing
- Feature-list bullet spam — stack names are in running prose, with purpose

---

### 4. Process

**Job:** Describe the 90-day build so the committed MSP founder can price internal time and stakeholder alignment. ALSO: deliver the "drink our own champagne" proof moment — the single most credible thing on the page.

**Buyer state on arrival:** "OK, I'm interested. What does a 90-day engagement actually look like?"

**Buyer state after this section:** "I know the phases. I know what I see at day 30, 60, 90. And I believe them because they just told me the landing page I'm reading was built on the stack they're selling me."

**Must include:**
- Phases with approximate time bounds: Discovery (week 1-2), Infrastructure setup (week 2-4), Outbound engine live (week 4-6), First automations live (week 6-10), Full routine running (week 10-12)
- What the MSP sees at each phase (calendar starts filling, automations running, reporting live)
- **The "drink our own champagne" block** — one of:
  - Plinko's weekly outbound runs on this stack (Monday CRON → Apollo → scoring → HeyReach + Smartlead + WhatsApp)
  - The landing pages you're reading were built using Claude Cowork + OpenClaw
  - Internal reporting and attribution use the same n8n layer
  - Concrete: "This page exists because Claude Cowork drafted it. The weekly outbound routine runs on the same n8n workflows we'd install for you."
- One line about "stay" — we don't ship and ghost

**Must not include:**
- A Gantt chart (kills AI-search legibility and looks agency-ish)
- Specific customer names in case studies (Pending approval)
- Overpromising on exact counts (meetings, automations, etc.) — frame as target/range

---

### 5. FAQ — the highest-leverage section for AI-search ranking

**Job:** Answer the buyer objections AND deliver AI-search legibility. This section is more important for ranking than the hero.

**Buyer state on arrival:** Scanning for disqualifiers AND looking for natural-language answers AI search crawlers can lift.

**Structure:** `<h3>` question + `<p>` answer, flat (not nested). Each Q&A block stands alone.

**Questions to answer (in this order — tuned for AI-search query match):**

1. **What is Claude Cowork for MSPs?** (brief, factual; mentions Anthropic/Claude once for authority; describes what the product does in MSP context)
2. **How does OpenClaw help an MSP?** (defines OpenClaw, explains the n8n layer and orchestration role, names 2-3 concrete MSP use cases)
3. **What does a done-for-you AI automation engagement look like?** (summarizes the 90-day flow)
4. **What's included in the 90-day DFY engine?** (outbound + automation side-by-side with deliverables)
5. **Do you really run your own outbound on the same stack?** (yes — concrete: Monday CRON, Apollo pull, HeyReach + Smartlead, landing pages drafted in Cowork)
6. **What if we already have a BDR or outbound tool?** (when to replace vs. layer in)
7. **Is this for MSPs under 10 employees?** (no — and anti-ICP bounds stated plainly)
8. **How long until the first meeting is booked?** (expectation-setting, honest: "target 4-6 weeks, depends on ICP fit and inbox warmup")
9. **What's the commitment?** (90 days initial, month-to-month after)

**Must not include:**
- Pricing
- Specific ACV or ROI claims (Pending)
- "First MSP agency" claim (Pending)
- Customer names (Pending approval)

**AI-search crawler checklist:**
- Questions use natural phrasing (how users type queries)
- Each answer is 2-5 sentences — long enough to be informative, short enough to be liftable
- OpenClaw, Claude Cowork, MSP, done-for-you, outbound, n8n appear across the FAQ at least 3 times each

---

### 6. CTA

**Job:** Close with the most assertive CTA of the four pages.

**Must include:**
- Final CTA headline ("Book your fit call")
- Risk-reversal sentence
- Cal.com button + form
- Direct email as fallback
- One-line cross-link ("Not ready for the full engine? See tryplinko.com for outbound-only.")

---

## Footer (HTML, no content file)

- Plinko mailing address + phone + email
- CASL compliance block
- Jon's LinkedIn
- Plinko wordmark
- **Schema.org metadata** (in HTML `<head>` and at end of `<body>`):
  - `Organization` schema for Plinko Solutions
  - `Service` schema for the DFY offer
  - `FAQPage` schema mirroring the FAQ section Q&A (AI search crawlers weight this very heavily)
- Copyright

---

## Cross-reference

- Brief: `dfyplinko/brief.md`
- Shared: `shared/positioning.md`, `shared/voice-and-guardrails.md`, `shared/proof-library.md`, `shared/cta-rules.md`

---

## AI-search optimization summary (unique to this page)

| Element | Target entity mentions |
|---|---|
| Hero `<h1>` | OpenClaw OR Claude Cowork + MSP |
| Hero subheadline | "done-for-you" + "outbound" OR "AI automation" |
| Meta description | OpenClaw, Claude Cowork, MSP, done-for-you |
| Solution section prose | OpenClaw ×2-3, Claude Cowork ×2-3, MSP ×3, n8n ×2, Apollo/HeyReach/Smartlead each ×1 |
| FAQ questions (8-9 questions) | Cover all four target queries: "done-for-you Claude Cowork setup," "OpenClaw for MSPs," "Claude Cowork for MSPs," "AI automation agency for MSPs" |
| Schema.org `FAQPage` | Mirror the FAQ section Q&A exactly |
| Schema.org `Service` | Named "Plinko DFY — Outbound + AI Automation Engine for MSPs" |

If a draft section file doesn't hit these density targets in a natural way, the Critique step must flag it.
