# Brief — versafilecanada.com

The anchor page for VersaFile's direct enterprise motion. Highest-stakes tone, most formal copy, most conservative claims.

---

## One-line positioning

Canada's M-Files implementation partner for the energy sector. We've done this. We know your regulator. We configure, deploy, and stay.

---

## Who this page is for (ICP)

**Job titles (primary):**
- Records / Information Management manager
- Engineering document control lead
- Compliance or regulatory affairs director
- IT director (when ECM is in their portfolio)
- VP of Operations (Canadian utilities often have ops-own-records pattern)
- VP of IT / CIO (at larger operators)

**Company profile:**
- Electric utilities, crown corporations, IPPs, midstream energy, district energy, natural gas distribution
- 1,500 – 10,000 employees (enterprise band)
- Canadian — headquartered, regulated under NERC CIP, OEB, CER, AER, or provincial equivalents
- Currently running SharePoint + file shares + point tools (Bluebeam, Primavera docs, manual drawings review) — in other words, a fragmented document reality that's cracking under regulator pressure

**Buying trigger (what made them search):**
- Regulatory audit on the calendar (next 6-18 months)
- A prior incident where they couldn't produce a document in the window the regulator asked for
- SharePoint migration decision pending — someone said "let's look at M-Files"
- Engineering team complaints about drawing control
- New compliance requirement (e.g., NERC CIP version update)

**Emotional state when they land:**
- Skeptical. They've seen vendor slides before. They're scanning for genuine expertise vs. generic "we do ECM."
- Pressed for time. 8-12 seconds before they decide if this is real.
- Cautious about claims. "Seamless," "best-in-class," "partner with you" → exit.

---

## Who this page is NOT for (anti-ICP)

Explicit. We name these on the page to build trust.

- Non-Canadian operators (we don't know your regulator, go elsewhere)
- Sub-1,500 employee utilities (not our delivery profile — route them to Plinko Energy)
- Companies that want "just the software, no implementation" (we don't sell licenses without configuration; M-Files is too configurable to deliver value unboxed)
- Non-energy industries (law firms, hospitals, manufacturers have different ECM calculus; we know energy)
- Anyone looking for a pitch deck and a quote in an hour (we qualify before we scope)

---

## Page promise (what the buyer walks away believing)

1. This is a Canadian company, run by Canadians, who have shipped M-Files in regulated Canadian energy environments.
2. They understand our regulator (NERC CIP / OEB / CER) — they named it before we did.
3. They don't resell and disappear. They configure, deploy, train, and stay.
4. A 15-minute call is the lowest-friction next step and has no sales-pitch load.

---

## What success looks like (acceptance criteria)

The page ships when all of the following are true:

1. **Enterprise buyer test:** A records manager at a Canadian utility, reading the page on their phone between meetings, says out loud "these people have actually done this" within the first scroll.
2. **Regulator legibility:** NERC CIP, OEB, CER, or AER appears in the hero or immediately below. Exact regulator names are a structural proof element.
3. **No marketing superlatives.** Page passes `voice-and-guardrails.md` scan with zero hits on the banned-word list.
4. **Every claim is in `proof-library.md`** with source. No orphan claims.
5. **Three Cal.com CTAs + one form + one LinkedIn footer link.** No extra CTAs. No newsletter. No gated PDF.
6. **Four-capability grid visible:** configure, deploy, train, stay. These are the implementation-deep differentiators.
7. **Anti-ICP section present** — explicitly names who this isn't for.
8. **Tone is measured, not enthusiastic.** No exclamation points anywhere on the page. Contractions allowed outside the hero.
9. **Mobile rendering is clean at 320px.** Enterprise buyers skim on phones.
10. **CASL compliance:** mailing address, phone, email visible in footer.

---

## Proof moments to lean on (from proof-library.md)

- VersaFile has deployed M-Files in Canadian electric utilities and midstream operators (Validated)
- Sector specialization in energy (Validated)
- Canadian context — knows OEB, CER, NERC CIP (Validated)
- Four-capability delivery: configure, deploy, train, stay (Validated — it's what's in the service contract)

**Do not use on this page:**
- Specific customer names (Pending until approval)
- Plinko mentions (brand hierarchy rule — VersaFile brand only)
- Any Plinko-side stack mentions (Apollo, HeyReach, etc.)

---

## Voice and tone (from voice-and-guardrails.md)

| Dimension | Rating | What this means |
|---|---|---|
| Formality | 5 | Most formal of the four pages. Enterprise RFP-adjacent. |
| Technical density | 4 | Assumes domain fluency — ECM, document control, regulator names. |
| Assertiveness | 3 | Direct but not boastful. Claims are specific, not loud. |

**Voice test:** If this page could appear in a Canadian Crown corporation's RFP response without edits, the tone is right.

**Banned categorically on this page:**
- "Hey," "Let's chat," "We get it" — no peer talk
- "Cutting-edge," "world-class," "best-in-class"
- "Revolutionize," "transform," "unlock"
- Exclamation points (zero allowed on the page)

---

## Build order for sections

Recommended order within the page:

1. `hero.md` — lock first; all other sections calibrate against its voice
2. `pain.md` — establishes what buyer's world looks like (regulator pressure, fragmented docs)
3. `solution.md` — VersaFile's four capabilities (configure, deploy, train, stay)
4. `process.md` — what a real engagement looks like (timeline, ownership model)
5. `faq.md` — objections: why M-Files, why Canadian, why VersaFile specifically
6. `cta.md` — the final call-to-action block

---

## Open questions / blockers

- [ ] Customer logo section: do we have any published (written-approved) names we can list? If no, leave placeholder and ship without logos. No logos beats fake logos.
- [ ] Mailing address, phone, email for CASL footer — placeholder in HTML, needs real values before launch.
- [ ] Cal.com event type `/jonmc/versafile-intro` needs to exist and be configured before CTAs go live.

---

## Cross-reference

- Positioning: `shared/positioning.md` → Motion 1 (VersaFile Direct)
- Voice: `shared/voice-and-guardrails.md` → versafilecanada row
- Proof: `shared/proof-library.md` → VersaFile-tagged claims
- CTA: `shared/cta-rules.md` → versafilecanada column
