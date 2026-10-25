# Recon & collection

## Unit of comparison (decide before mapping)
- **Core product**: the offer both brands sell in all audited markets, for the business focus. Examples: Data Analytics bootcamp (education), business account for freelancers (fintech), hotel booking in a city (travel).
- **Entry offer** (if any): the free, freemium or subsidized offer used to acquire customers. Examples: public-funded courses (SEPE/FUNDAE in ES, CPF/France Travail in FR, Skills Bootcamps in UK), free plan or trial (SaaS, fintech), loyalty sign-up or app-only deals (travel). Compare the funnel, not the offer, when the benchmark has no equivalent.
- State the unit at the top of the URL map so the user confirms both at the checkpoint.

## Phase 1 — Map localized URLs

For each brand × market, find:

| Brand | Market | Localized URL | How found | Notes |
|---|---|---|---|---|

How to find them, in order:
1. Read hreflang tags on the home page (`<link rel="alternate" hreflang="...">`).
2. Try common patterns: `/fr`, `/es`, `/en`, `fr.domain.com`, `domain.fr`.
3. Search: `site:domain.com` + a market keyword in the local language.

Watch out:
- **IP redirects.** The fetch runs from a server outside the target market. Never trust the root URL; always use the explicit localized URL.
- **"EN" defaults to the UK market.** Use the UK URL (`/uk`, `/gb`, `/en-gb`, `.co.uk`). Switch to US or global English only if the user says so.
- **Brand not present in a market** (no licence, no local offer) = finding. Record "not present", don't score it, and show it in the gap matrix.
- **No localized version** = finding. Record it, score 1 on Localization, move on.

**Checkpoint:** show the table and wait for confirmation before Phase 2.

## Phase 2 — Collect evidence

Per brand × market, capture:
- Home page
- Top offer page for the business focus (e.g. a bootcamp program, a pricing plan for freelancers, a destination or hotel page)
- Pricing page (plus financing or payment options when relevant)
- Conversion entry point. Identify the model first:
  - **Lead gen** (form → call): count fields, note any test or call required.
  - **Self-serve sign-up** (account, trial): count steps up to identity check (KYC) or payment, note what is asked and when. Stop before submitting real personal data or documents.
  - **Booking / checkout** (search → pay): steps from search to payment, price shown vs price paid (fees, taxes), payment methods. Stop before paying.

External sources:
- Meta Ad Library: https://www.facebook.com/ads/library/ (filter by country + advertiser)
- Google Ads Transparency Center: https://adstransparency.google.com/ (filter by region)
- B2B only: LinkedIn Ad Library: https://www.linkedin.com/ad-library/ (filter by advertiser + country)
- AI answers: at least 1 prompt per market, 3 recommended, in the local language (see `dimensions.md` §4)

If the user can't access a source, mark the dimension "n/a — not observable" instead of guessing.

### Fetch fallbacks
- Page returns empty HTML (SPA) → ask the user for a `.mhtml` save of the page.
- Cookie wall or bot block → ask for `.mhtml` or a screenshot of the relevant section.
- Ad libraries need a browser → if no browser tool is available, give the user the filtered URL and ask for a screenshot.

### Mystery-shopping evidence (optional, high value)
The audit runs without it (dimension 6 becomes "n/a — not observable"). Skip it when signing up would require real identity documents (KYC) or would take a subsidized seat from someone eligible.
Emails, WhatsApp messages or call notes received after signing up as a lead.
- Anonymize names, phone numbers and email addresses before quoting.
- Record: date of sign-up, date/time of first contact, channel, language, what is asked of the lead.

