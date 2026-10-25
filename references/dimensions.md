# Audit dimensions

Score each dimension 1–5 per brand × market.

| Score | Meaning |
|---|---|
| 1 | Absent |
| 2 | Present but generic or weak (translated, not localized) |
| 3 | Functional |
| 4 | Localized and strong |
| 5 | Clear competitive advantage |

Every score needs one evidence line: URL + what was observed.

---

## 1. Localization & value proposition
- Is the H1 / main promise written for this market or translated from another?
- Local proof: local currency and prices, local customers or logos, local reviews, local offices. (Education: local campuses, employers, salaries. Travel: local-language reviews, local payment and support.)
- Local regulation / certification mentioned when relevant.

## 2. Conversion (CRO)
Identify the conversion model first (see `recon.md` Phase 2): lead gen, self-serve sign-up or booking.
- Primary CTA above the fold, one clear next step.
- Lead gen: number of fields, required fields, friction (tests, calls).
- Self-serve sign-up: steps and time to an active account, when identity check (KYC) or payment is asked, free trial or free plan.
- Booking: steps from search to payment, fees or taxes added late, local payment methods.
- Price visible? Financing or payment options visible?
- Trust elements next to the CTA (reviews, ratings, customer count, outcome metric such as placement rate).

## 3. SEO (technical + local)
- hreflang present and consistent (reciprocal, correct codes).
- Localized title/meta per language, local keyword in H1.
- Localized pages indexable (no noindex, canonical not pointing to another language).
- Local landing pages per city/program.

## 4. GEO / AI visibility
- Build at least 1 prompt per market (3 recommended), in the market's language. Pick the template that fits:
  - Local product: "best {client category} in {main city of the market}".
  - Online product: "best {client category} for {target customer or use case}" (no city).
  - Education example: "meilleur bootcamp data analytics à Paris" / "mejor bootcamp de análisis de datos en Madrid" / "best data analytics bootcamp in London"
  - SaaS example: "meilleur logiciel de paie pour PME" / "mejor software de nóminas para pymes"
  - E-commerce example: "où acheter un vélo électrique en ligne" / "dónde comprar una bicicleta eléctrica online"
  - Fintech B2B example: "meilleure banque en ligne pour freelance" / "mejor cuenta bancaria para autónomos" / "best business bank account for freelancers in the UK"
  - Travel example: "meilleur site pour réserver un hôtel à Barcelone" / "mejor web para reservar hotel en París" / "best site to book a hotel in Paris"
- Run it in at least one engine (ChatGPT); add Perplexity and Gemini when possible.
- Record: engine, date, prompt, which brand is cited, in what position, with what caveat, and which sources the answer relies on.
- Answers vary between runs. Report this as a directional signal, not a ranking.

## 5. Paid (SEA + SMA)
- Meta Ad Library, filtered by country: number of active ads, languages, formats, offers.
- Google Ads Transparency Center: active advertiser, formats, regions.
- B2B: LinkedIn Ad Library, filtered by country: active ads, audiences named in the copy (job titles, company size), formats (lead gen forms, document ads, events).
- Signals only. Never estimate spend.

## 6. Lead nurture / onboarding (email / WhatsApp / CRM)
Optional evidence. For self-serve or booking models, look at onboarding or abandoned-booking emails instead of sales follow-up.
- Mystery-shopping evidence: time to first contact, channel, language, personalization.
- Friction before a human conversation (tests, forms, waiting).
- Sequence: number of touches, content, clear next step.
- If no evidence is provided: "n/a — not observable", and recommend running a mystery shop.

## 7. Local acquisition levers
Market-specific levers a brand can use to acquire customers. Pick the ones that fit the client's category:
- **Education / training:** public funding (ES: SEPE / FUNDAE · FR: CPF / France Travail / OPCO · UK: Skills Bootcamps), certifications (Qualiopi, RNCP).
- **B2B / SaaS:** local integrations (accounting, payroll, e-invoicing rules), local compliance badges, local partner and reseller networks.
- **Travel / hospitality:** local OTAs and metasearch, loyalty programs, local payment methods, language of reviews, local holidays and seasonality.
- **E-commerce / retail:** local payment methods (Bizum, Cartes Bancaires, Klarna), local marketplaces, delivery options, local review platforms.
- **Any category:** partnerships, local events, local offices or campuses, employer or corporate programs.
- Score whether the lever is used AND whether it is visible on the site and in the ads.
