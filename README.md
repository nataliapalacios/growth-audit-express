# growth-audit-express

**A Claude Code skill that turns two URLs and a list of markets into a pre-sales growth audit.**

Give it a client, one competitor and the markets you care about. It returns what a growth consultant would bring to a first client meeting:

- a **gap matrix**: 7 dimensions × each market × client vs benchmark, scored 1–5, each score backed by one piece of evidence
- an **ICE-prioritized backlog**: top 3 quick wins per market + 1 cross-market bet
- a **30-day test-and-learn plan**: hypothesis, channel, KPI and the tracking needed
- a **report** in the language you ask for (Markdown, plus an optional one-page visual HTML version)

Built for multi-market work (e.g. FR / ES / UK), where the interesting gaps hide between countries.

---

## What it audits

| # | Dimension | What it looks at |
|---|---|---|
| 1 | Localization | Is the promise written for this market or translated? Local proof, currency, language |
| 2 | Conversion (CRO) | CTA, friction in the lead form, sign-up or booking flow, visible price, trust next to the CTA |
| 3 | SEO | hreflang, localized titles, indexable local pages |
| 4 | GEO / AI visibility | Who ChatGPT / Perplexity / Gemini recommend, in what position, citing which sources |
| 5 | Paid (SEA + SMA) | Meta Ad Library, Google Ads Transparency and LinkedIn Ad Library (B2B): volume, themes, formats. Signals only, never spend |
| 6 | Lead nurture / onboarding | Optional mystery-shopping: time to contact, channel, friction before a human conversation or an active account |
| 7 | Local acquisition levers | Public funding, local payment methods, local integrations, partnerships |

## How it works

1. **Map.** Fix the unit of comparison, then find the localized URL for each brand × market. *Checkpoint: you confirm the URL map.*
2. **Collect.** Pages, financing, lead forms, ad libraries, AI answers, optional mystery-shopping evidence.
3. **Score.** 1–5 per dimension. No evidence, no score.
4. **Prioritize.** ICE = (Impact + Confidence + Ease) / 3.
5. **Plan.** 30-day test-and-learn plan.
6. **Deliver.** Report following `references/output-template.md`.

## Install

```bash
git clone https://github.com/nataliapalacios/growth-audit-express.git
mkdir -p ~/.claude/skills
cp -r growth-audit-express ~/.claude/skills/
```

Then open Claude Code in any folder and ask for an audit.

## Use it on your own case

Minimum prompt:

```
Run growth-audit-express.
Client: https://client.com
Benchmark: https://competitor.com
Markets: FR, ES, UK
```

Better prompt (more context = sharper audit):

```
Run growth-audit-express.
Client: https://client.com
Benchmark: https://competitor.com
Markets: FR, ES, UK (UK = London, not the global English site)
Focus: B2C lead generation for <main product>
Primary KPI: cost per qualified lead
Report language: French
I'll send ad library screenshots and AI answers when you ask for them.
```

### Example cases it fits

| Category | Client vs benchmark (illustrative) | Typical local levers |
|---|---|---|
| Education / bootcamps | a school vs a competing school | Public funding (CPF, SEPE, Skills Bootcamps), certifications |
| B2B SaaS | a payroll or invoicing tool vs the local leader | Local integrations, e-invoicing compliance, reseller networks |
| E-commerce | a DTC brand vs a marketplace seller | Local payment methods, delivery options, review platforms |
| Travel / hospitality | an operator vs an OTA | Local OTAs, language of reviews, seasonality by market |

### What you may need to provide

Some sources need a human with a browser. The skill will ask for them:

- **Ad library screenshots** (Meta Ad Library, Google Ads Transparency) filtered by country
- **AI answers**: run the suggested prompt per market in ChatGPT (and ideally Perplexity / Gemini), paste or export the answer
- **.mhtml saves** of pages that block automated fetching
- **Mystery-shopping evidence** (optional, high value): emails or WhatsApp messages received after signing up as a lead. Personal data is anonymized in the report.

## Rules the skill follows

- No evidence, no score: unobservable cells are marked `n/a`.
- Never estimates competitor ad spend.
- A missing localized version is a finding, not an error.
- One AI answer is a directional signal, not a ranking.
- Zero ads in one library is not "no marketing": the report names what was and wasn't checked.
- If the auditor has a relationship with the client or the benchmark, public information only, and it's disclosed.

## Example output

[`examples/`](examples/) contains a full run: **Ironhack vs Le Wagon across France, Spain and the UK** (Data Analytics bootcamp + public-funding funnels), in English, in French, and as a one-page visual report.

**[View the visual report (FR) →](https://nataliapalacios.github.io/growth-audit-express/examples/audit-ironhack-lewagon-fr.html)**

The headline it found: the client wins Spain through paid social and public funding, but loses France and the UK, where the benchmark wins without a single Meta ad, through public funding and AI visibility.

It's one example of the method. Swap the URLs and markets to audit any category.

## Structure

```
growth-audit-express/
├── SKILL.md                    # trigger, phases, rules
├── references/
│   ├── recon.md                # URL mapping, unit of comparison, evidence collection
│   ├── dimensions.md           # the 7 dimensions and how to score them
│   ├── ice.md                  # ICE scoring and 30-day plan format
│   ├── output-template.md      # report structure
│   └── edge-cases.md           # what broke in real runs and how it was fixed
└── examples/                   # full sample audit
```

## Self-improvement

After each run, new edge cases are appended to `references/edge-cases.md`. The skill gets sharper with every audit.

## License

MIT
