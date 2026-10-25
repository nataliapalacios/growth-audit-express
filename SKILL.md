---
name: growth-audit-express
description: Multi-market growth audit of a client website against one benchmark competitor. Use when asked for a growth audit, competitive audit, pre-sales audit, or "how does X compare to Y in FR/ES/EN". Outputs a gap matrix, an ICE-prioritized backlog and a 30-day test plan.
---

# Growth Audit Express

One job: turn two URLs and a list of markets into a pre-sales-grade growth audit in one run.

## Inputs
- **Required:** client URL, benchmark URL, markets. Default: FR, ES, UK. "EN" means the UK market unless the user says US or global English site.
- **Optional:** business focus (e.g. B2C lead gen, B2B self-serve sign-up, travel bookings), mystery-shopping evidence (emails/WhatsApp received after signing up as a lead), primary KPI, budget range.

If a required input is missing, ask once, then proceed.

## Phases
1. **Map** — Fix the unit of comparison (the core product both brands sell + any free or subsidized entry offer, compared separately), then find the localized URL for each brand × market. → `references/recon.md`
   **Checkpoint:** show the URL map table and wait for confirmation.
2. **Collect** — For each brand × market: home, top offer page, pricing page, conversion entry point (lead form, sign-up flow or booking flow), public ad libraries, AI answers. Add mystery-shopping evidence if provided (optional). → `references/recon.md`
3. **Score** — 7 dimensions, 1–5, one piece of evidence per score. → `references/dimensions.md`
4. **Prioritize** — ICE scoring. Top 3 quick wins per market + 1 cross-market bet. → `references/ice.md`
5. **Plan** — 30-day test-and-learn plan: hypothesis, channel, KPI, tracking needed, week. → `references/ice.md`
6. **Deliver** — Report following `references/output-template.md`, in the language the user asks for.

## Rules
- No evidence, no score. Write "n/a — not observable" instead.
- Never estimate competitor ad spend. Report signals only (active ads, formats, languages, offers).
- A missing localized version is a finding, not an error.
- Anonymize personal data in mystery-shopping evidence (names, phone numbers, emails).
- Separate presence from quality: a tag existing is not the same as it being good.
- Conflict of interest: if the auditor has any relationship with the client or the benchmark, use public information only and disclose the relationship in "Method & limits".
- GEO answers: log engine, date, language and prompt. One run is a directional signal, never a ranking.
- Zero ads in one library is not "no marketing". Name the libraries checked and the ones not checked.

## Self-improvement
After each run, append new edge cases and fixes to `references/edge-cases.md`.
