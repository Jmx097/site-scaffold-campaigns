# Landing Pages — 5 Outreach Domains

Five single-page landing sites, one per cold-sending domain. Each folder is independently deployable to its own Vercel project.

```
landing-pages/
├── versafilecanada/       → versafilecanada.com (VersaFile, Motion 4 brand-led, navy, enterprise)
├── energycontentcontrol/  → energycontentcontrol.com (VersaFile, Motion 5 value-prop-led, capability-first)
├── plinkoenergy/          → plinkoenergy.com (Plinko+VersaFile bridge, teal, mid-market)
├── tryplinko/             → tryplinko.com (Plinko MSP, orange, peer-to-peer)
└── dfyplinko/             → dfyplinko.com (Plinko MSP + OpenClaw/Cowork, dark mode, assertive)
```

**Motion allocation (2 Plinko + 1 Bridge + 2 VersaFile across 5 domains):** `versafilecanada` and `energycontentcontrol` target the same Canadian energy ICP with two narrative framings — brand-led vs. capability-led. They run in parallel on separate ScaledMail inbox pools; reply rate after 30 days decides which angle takes more volume in month 2. See `energycontentcontrol/brief.md` for the split hypothesis.

**Motion-language guardrail (enforced):** M-Files, energy, utilities, and regulator names (OEB, CER, NERC CIP, AER) appear ONLY on the 3 VersaFile-aligned domains (`versafilecanada`, `energycontentcontrol`, `plinkoenergy`). The 2 Plinko MSP domains (`tryplinko`, `dfyplinko`) do NOT mention M-Files, energy, or utilities. Cross-contamination of vocabulary kills credibility on both motions.

Each folder contains:
- `index.html` — the page (fully self-contained, no build step, inlined CSS/JS)
- `vercel.json` — security headers + clean URL config

## Before you deploy — fill in placeholders

Every page has `[MAILING ADDRESS]`, `[PHONE]`, `[EMAIL]`, and `[LINKEDIN URL]` in the footer and form error messages. Find/replace these in each `index.html` before publishing:

| Placeholder | versafilecanada.com | energycontentcontrol.com | plinkoenergy.com | tryplinko.com | dfyplinko.com |
|---|---|---|---|---|---|
| `[MAILING ADDRESS]` | VersaFile registered address | VersaFile registered address | Plinko Solutions address | Plinko Solutions address | Plinko Solutions address |
| `[PHONE]` | VersaFile mainline | VersaFile mainline | Plinko number | Plinko number | Plinko number |
| `[EMAIL]` | `jon@versafilecanada.com` | `jon@energycontentcontrol.com` | `jon@plinkoenergy.com` | `jon@tryplinko.com` | `jon@dfyplinko.com` |
| `[LINKEDIN URL]` | Jon's LinkedIn | Jon's LinkedIn | Jon's LinkedIn | Jon's LinkedIn | Jon's LinkedIn |

**CASL compliance:** the mailing address, phone, and email are required on every page. Don't publish without them — Smartlead's unsubscribe link handles the rest.

## Deploy each folder as its own Vercel project

### One-time Vercel setup

```bash
# From the LinkedIn Engine project root
cd "landing-pages/versafilecanada"
npx vercel link        # Create new project, name it "versafilecanada"
npx vercel --prod      # Deploy to production
```

Repeat for each of the 5 folders. Name the Vercel projects to match the domains: `versafilecanada`, `energycontentcontrol`, `plinkoenergy`, `tryplinko`, `dfyplinko`.

### Attach the custom domains

For each Vercel project (after `vercel link`):

1. Vercel dashboard → Project → Settings → Domains → Add
2. Enter the domain (e.g., `versafilecanada.com`)
3. Vercel shows the DNS records you need to add at Porkbun
4. At Porkbun → Domain Management → DNS → add the records Vercel specifies (typically an `A` record or `CNAME`)
5. Wait 10 min to 1 hour for propagation. Vercel auto-provisions SSL.

**Also add `www.` variants** and set one as the primary (Vercel handles the redirect):
- `www.versafilecanada.com` → redirect to apex, or vice versa
- Pick whichever matches the URL you'll put in email footers

## Environment variable: N8N form webhook

Each page's contact form POSTs to an n8n webhook to land form submissions in your CRM (Airtable for Plinko motions, D365 for VersaFile motions).

**Default URL in the code:** `https://n8n.openclaw.app/webhook/form-submit`

Update this in all 5 `index.html` files (search for `N8N_FORM_WEBHOOK`) or override per-page by setting `window.N8N_FORM_WEBHOOK` before the main script loads. Once the n8n `form-submit` workflow is built, I'll give you the actual webhook path.

**Motion routing at the form endpoint:** the n8n `form-submit` workflow switches on the `motion` field (see the motion tags table below) and lands the lead in the right CRM. Airtable for Plinko motions (`plinko-msp-try`, `plinko-msp-dfy`), Dynamics 365 for VersaFile motions (`versafile`, `versafile-ecc`), both for the bridge (`plinko-energy`).

## What the pages do (functional summary)

Each page:

1. **Captures UTM params from the URL** (`utm_source`, `utm_medium`, `utm_campaign`, `utm_term`, `utm_content`) and persists them in `sessionStorage` so they survive across navigation within the page.
2. **Appends UTMs + `source_domain` to Cal.com CTAs** so when a prospect books a meeting, Cal.com receives the attribution metadata and can forward it via webhook to n8n.
3. **Posts the contact form** to the n8n webhook as a JSON body containing: name, email, company, message, all captured UTMs, `source_domain`, `motion`, `referrer`, and `submitted_at`.

This gives you attribution at two endpoints (Cal.com bookings and form submits), both routed through n8n to the correct CRM.

## Motion tags (for n8n routing)

Each page sends a `motion` field to the webhook so n8n can route to the right CRM:

| Page | `motion` value | Target CRM |
|---|---|---|
| versafilecanada.com | `versafile` | Dynamics 365 (VersaFile) |
| energycontentcontrol.com | `versafile-ecc` | Dynamics 365 (VersaFile) — same pipeline as `versafile`, tagged for A/B attribution |
| plinkoenergy.com | `plinko-energy` | Both — Airtable (Plinko) + D365 (VersaFile, partner visibility) |
| tryplinko.com | `plinko-msp-try` | Airtable (Plinko) |
| dfyplinko.com | `plinko-msp-dfy` | Airtable (Plinko) |

The n8n `form-submit` workflow switches on this field. Build spec coming in the reply-triage / attribution workflows I'm rebuilding for Smartlead.

## Offer per motion (tightened)

Each motion has **exactly one offer** — the low-friction artifact the email promises in exchange for a reply. The landing page CTA (`Book your 15-minute fit call`) is the *second* step for readers who land from somewhere other than a cold email. The offer itself lives in `outbound-copy.md` and is rendered into each Smartlead campaign's sequence. **Do not stack offers across motions** — buyers notice, and the copy architecture breaks.

| Motion | Offer | What the prospect gets | Lives in |
|---|---|---|---|
| VersaFile (`versafilecanada`, `energycontentcontrol`) | **Three-Findings Note** | One-page, Jon-signed PDF with three specific observations about the prospect's records/compliance posture, drawn from public info (annual reports, OEB/CER filings, RFPs, job postings). No product pitch. | `offers/vf-three-findings-template.md` |
| tryplinko | **Outbound Mini-Audit Loom** | 15-minute async Loom. Jon opens the MSP's LinkedIn + website and narrates three things he'd change about their outbound this week. No call required. | `offers/tryplinko-loom-script.md` |
| dfyplinko | **Free n8n Workflow** | Production-ready n8n JSON specific to the signal — weekly-ops-digest for new-COO prospects, pipeline-to-investor report for PE-backed prospects. Import and run immediately. | `offers/dfyplinko-n8n-samples/` |
| plinkoenergy (bridge) | Either VF three-findings or tryplinko audit — chosen per lead based on persona on first reply. | Same assets above. | — |

**Why this framing works:** Each offer reframes the 15-min call from "sales demo" to "follow-up on the thing I already sent you." The ask in the cold email is *only* "want me to send it?" — a binary yes/no, no calendar commitment. The landing page exists to convert the subset of prospects who'd rather self-serve straight to the call.

**Maintenance:** If you edit offer copy or subject lines, change it in `outbound-copy.md` first — that's the source of truth the `email-loader-smartlead` workflow and Smartlead templates pull from. Don't rewrite landing page CTAs to reference the offer until the offer has survived 4–6 weeks of live sends.

## Iteration after launch

Copy is not sacred. Once campaigns run 4-6 weeks, expect to revise:

- **Hero headlines** (the biggest conversion lever)
- **"Who this is for" sections** (as reply data narrows the ICP)
- **Proof — logos, testimonials, stats** (as you generate them)

**Don't touch without re-deploying carefully:**
- Mailing address, phone, email (CASL)
- Cal.com link (attribution breaks)
- Footer CASL block (compliance)

## Rendering check before first cold send

- **Mobile:** Pages are responsive down to 320px wide. Open each in Chrome DevTools mobile mode before shipping. Enterprise buyers often open cold email on phone, skim the landing page, then revisit on desktop if interested.
- **Preview in slack/email:** send yourself the URL in Slack and Outlook to check OG preview rendering (uses the `og:title` and `og:description` meta tags in each page).
- **Spam check:** run each landing URL through `mail-tester.com` or send a test cold email from one of your warmed Smartlead inboxes with the landing link in the body. If the test email lands in spam, the landing domain may need more age before real sends.

## Not yet included (pending upstream decisions)

- **Favicon:** add a small `.ico` file in each folder. Take 5 min in Figma or use a generator.
- **Logos:** wordmarks only right now. Drop actual Plinko and VersaFile logo files into each folder and reference in `<header>` if you want image marks.
- **Customer logos:** `versafilecanada.com` has a section placeholder for "publishable customer names." Add 3-5 logos only if explicit approval exists. No logos beats fake logos. Same rule applies to `energycontentcontrol.com` — the two VF-direct pages share the proof pool.
- **Cal.com inline embed:** currently a button link. Conversion lifts if you switch to Cal.com's inline embed snippet, but it adds a third-party script. Consider after 4 weeks of data.

## Quick sanity check

After deploying, for each domain verify:

- [ ] HTTPS loads (green padlock)
- [ ] Mobile renders cleanly
- [ ] Cal.com CTA opens the correct booking page
- [ ] Form submit succeeds (or at least fails gracefully with the error message)
- [ ] UTM params survive the page (add `?utm_source=test` to URL, click the Cal.com CTA, confirm `utm_source=test` is in the Cal.com URL)
- [ ] OG preview looks correct in Slack/Outlook
- [ ] `X-Frame-Options`, `Strict-Transport-Security`, and other headers are present (check DevTools → Network → response headers)
