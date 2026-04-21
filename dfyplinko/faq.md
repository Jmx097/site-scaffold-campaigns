# FAQ — dfyplinko.com

## Intent

The highest-leverage section for AI-search ranking. 9 questions tuned for the target AI-search queries: "done-for-you Claude Cowork setup," "OpenClaw for MSPs," "Claude Cowork for MSPs," "AI automation agency for MSPs." Flat `<h3>` + `<p>` structure for crawlers. Each answer 2-5 sentences — informative, liftable.

---

## Draft (new — AI-search tuned)

> **What is Claude Cowork for MSPs?**
>
> Claude Cowork is Anthropic's collaboration platform for teams that work with AI agents. For an MSP, it means a workspace where Claude has context about your specific business — your client list, service catalog, ticketing data, past proposals, internal runbooks — and helps your team work through tasks that previously required a human to read everything and synthesize. Ticket triage, onboarding document generation, proposal drafting, and internal reporting are the four MSP use cases that pay back the setup fastest. For MSP owners, the value is having AI that actually knows your business, not a chatbot that starts from zero every time.
>
> **How does OpenClaw help an MSP?**
>
> OpenClaw is an orchestration layer built on n8n. For an MSP, it means the automations between your PSA, your CRM, your email, your proposal tool, and Claude Cowork all run on one platform. Instead of glueing together seven SaaS tools with Zapier and brittle integrations, OpenClaw hosts the workflows, runs them on your schedule, and gives you a single place to audit what's happening. We use OpenClaw + Claude Cowork to run our own outbound engine and our landing page drafting — it's the same infrastructure we install for MSP clients.
>
> **What does a done-for-you AI automation engagement look like?**
>
> Two workstreams running in parallel. First, the outbound engine — Apollo firmographics, Hunter for emails, HeyReach for LinkedIn, Smartlead for sending, all orchestrated on n8n. Second, Claude Cowork setup — workspace provisioning, context loading, and three to five internal automations built on OpenClaw. 90 days target from kickoff to full routine running. Weekly reporting on both workstreams on the same dashboards.
>
> **What's included in the 90-day DFY engine?**
>
> Outbound side: warmed sending infrastructure, signal-triggered campaigns, weekly signal sweep, reply triage, qualified meetings booked to your calendar. Automation side: Claude Cowork workspace, three to five OpenClaw automations (typically ticket triage, client onboarding, proposal drafting), weekly reporting. Both sides run on the same n8n infrastructure so they're one system, not two.
>
> **Do you really run your own outbound on the same stack?**
>
> Yes. Every Monday, an n8n workflow pulls target accounts from Apollo, scores them, and queues them into HeyReach and Smartlead. The landing page you're reading now was drafted using Claude Cowork. Our internal reporting uses the same n8n attribution layer we install for MSP clients. This is the "drink our own champagne" part — we run this every week, and you can see the exact stack on the pages we wrote for our motion.
>
> **What if we already have a BDR or an outbound tool?**
>
> Depends on your setup. If you have a BDR producing a predictable number of meetings, we can often augment them with the automation layer rather than replacing. If you have a Smartlead or Instantly account running and it's delivering, we can pick up from that infrastructure rather than starting over. If your BDR is struggling and your tool stack is siloed, we typically install the full stack fresh — trying to rebuild from a broken setup takes longer than starting clean. We'll tell you which applies on the fit call.
>
> **Is this for MSPs under 10 employees?**
>
> No. MSPs under 10 employees usually get more leverage from founder-led sales and a lightweight tool than from a done-for-you engine. We also don't serve MSPs over 100 employees through this offer — at that scale, the right play is an internal SDR team plus custom AI infrastructure, which is a different engagement. The 90-day DFY engine is built for 10 to 100 employee MSPs.
>
> **How long until the first meeting is booked?**
>
> Target is 4-6 weeks from kickoff. Depends on ICP fit (how cleanly we can define your target accounts), inbox warmup (warmed domains take 14-21 days before we send at volume), and signal availability (some MSP ICPs have clearer public signals than others). If week 6 passes without a meeting, we re-target together. We share progress weekly so there's no "month-end surprise."
>
> **What's the commitment?**
>
> 90-day initial window to prove the engine works on your ICP. Month-to-month after that. No year-long lock-in. If the trajectory is off by week 6, we re-target. If week 10 still isn't there, you can walk — no penalty.

---

## Critique

- **Nine questions matching sitemap intent.** Good.
- **Every question is a natural-language phrase a user would type.** AI-search crawler-friendly. Good.
- **Named entity density across FAQ:**
  - Claude Cowork: ×7 (strong — multiple hits across questions)
  - OpenClaw: ×6
  - MSP / MSPs: ×17
  - n8n: ×5
  - Apollo, HeyReach, Smartlead: each ×3
  - Done-for-you / DFY: ×4
  - Matches brief.md entity density targets for the FAQ section.
- **Question 1 ("What is Claude Cowork for MSPs?") mentions Anthropic once** — authority signal for AI search. Good.
- **Question 2 ("How does OpenClaw help an MSP?") defines OpenClaw as "orchestration layer built on n8n"** — clear definition, crawler-liftable.
- **Question 5 ("Do you really run your own outbound on the same stack?") is the champagne moment in Q&A form** — reinforces the proof without duplicating the process.md block verbatim.
- **Question 7 ("Is this for MSPs under 10 employees?") — anti-ICP stated plainly.** Matches brief.md requirement.
- **"Target is 4-6 weeks"** — hedged language. Matches sitemap.
- **"We'll tell you which applies on the fit call"** — reinforces the fit-call framing and the "honest anti-sell" guardrail.
- **Voice check:** Formality 3, assertiveness 5. Direct, structural. Declarative sentences throughout. Good.
- **No voice-and-guardrails violations** — no AI-hype, no superlatives, no hedging of the core offer.
- **Pending claim handling:**
  - "90 days target" — hedged (not "guaranteed")
  - "Three to five automations" — needs validation but structural to offer design
  - No "first MSP to combine" claim
  - No specific ACV or ROI numbers
  - Good.
- **AI-search legibility test:** If passed through Perplexity's "summarize this FAQ," it would produce clean 3-sentence summaries with Claude Cowork + OpenClaw + MSP entities in prominent positions. Passes.
- **Consider:** Should there be one more question on "Can we start with just the outbound side or just the automation side?" Currently unstated. Useful for buyers not ready to commit to both. Flag for rewrite.

---

## Rewrite

_Pending collaborative rewrite pass. Possible addition: "Can we start with just one workstream?"_

---

## Locked

_Not yet locked._

---

## Cross-reference

- Sitemap section 5
- Brief: "AI-search legibility is highest-leverage section"
- Voice: formality 3, assertiveness 5
- Proof library: multiple Validated and hedged claims — check each against library during rewrite
- Schema.org `FAQPage` markup mirrors this section exactly during HTML implementation
