# Edge cases log

Append after each run: date, case, what happened, fix.

| Date | Case | What happened | Fix |
|---|---|---|---|
| 2026-10-25 | Public funding as acquisition lever (ES) | Client runs free courses funded by a public employment program (SEPE). Lead receives a "logic test" request before any human call. | Added dimension 7 (local acquisition levers) and "friction before human conversation" in dimension 6. |
| 2026-10-25 | IP-based redirects | Root URL may redirect by visitor location; fetch runs outside target market. | Always map explicit localized URLs in Phase 1. |
| 2026-10-25 | Unit of comparison mismatch | Client's public-funding course (30h) has no benchmark equivalent. | Phase 1 now fixes the unit: core paid product + public-funding entry funnel, compared separately. |
| 2026-10-25 | Ad libraries need a human | Meta Ad Library requires a browser; fetch fails. | User sends screenshots per brand × country; log counts + themes, never spend. |
| 2026-10-25 | Benchmark with 0 Meta ads everywhere | Looks like "no acquisition" but brand ranks #1–2 in AI answers. | Read zero paid + strong GEO as an organic/brand-led model, and flag Google Ads as unchecked. |
| 2026-10-25 | Language-version URLs (/es-en/, /es/france/) | Easy to mistake a language version for a localization failure. | Check the URL path before scoring Localization; we chose the language, the site didn't. |
| 2026-10-25 | Client or benchmark switched mid-run | The test case changed twice (fintech, then insurtech) before Phase 2; the first URL map was thrown away. | Confirm client, benchmark, markets and focus in one message before Phase 1. Restart Phase 1 cleanly when any of them changes. |
| 2026-10-25 | Benchmark not present in a requested market | A fintech client had no UK offer (/en-gb 404, /en = EU English) while the benchmark was UK-born. | Record "not present" in the map and offer to swap the market. |
| 2026-10-25 | Multi-line benchmark (B2C + B2B) | Neobank and incumbent-insurer benchmarks advertise mostly consumer products (auto, home, personal health); keyword search mixes them with business ads. | Classify each ad by audience (business / consumer) and score Paid on the unit of comparison only. Say so in "Method & limits". |
| 2026-10-25 | Benchmark is not the competitor AI engines name | The incumbent benchmark was cited in none of the 3 ChatGPT answers; each market had its own shortlist of local insurers. | Log the brands cited in GEO answers per market and propose them as next benchmarks. Do not change the benchmark mid-run. |
| 2026-10-25 | Bot protection and CAPTCHA | A neobank site returned 403 on some paths and its sitemap; an insurer's Spanish site served a CAPTCHA. | Never solve or bypass a CAPTCHA. Ask the user for a saved page (.html or .mhtml) and say which pages are missing. |
| 2026-10-25 | hreflang injected or missing in raw HTML | Two fintech sites showed no hreflang in the fetched HTML; the insurtech client did. | Do not score SEO 1 on raw HTML alone; check in a browser or mark "to verify live". |
| 2026-10-25 | Self-serve quote flow is a SPA | The client's quote URL returned an empty, noindex shell to fetch. | Use a browser, decline non-essential cookies, click through choice-only steps and stop at the first field asking for real data (e.g. a company registration number). |
| 2026-10-25 | Mystery shopping blocked by real company data | The B2B quote needed a real company registration number to go further. | Do not invent company data. Dimension 6 = n/a, say why in "Method & limits". |
| 2026-10-25 | Keyword search in Meta Ad Library inflates counts | A short brand name returned ~2,500 results including creators and other advertisers, vs 35–42 for the benchmark. | Search by advertiser page when possible; when keyword counts are used, report them as an upper bound. |
| 2026-10-25 | User reading of a capture differs from the capture | The user summary said the client had no LinkedIn ads; the capture showed an active celebrity campaign promoted by the client. | Read every screenshot, not only the user summary; flag discrepancies politely before scoring. |
| 2026-10-25 | Ads leak across markets | Client ads with French-only legal concepts (Madelin, prévoyance obligatoire) and French copy were served in BE and ES. | In Paid, check language and legal concepts of ads per region, not only volume. Cheap, high-confidence quick win. |
| 2026-10-25 | Personal data inside ad libraries | Local agent ads show name and phone; influencer partnerships show handles. | Do not quote names, phones or handles in the report; describe the role ("a local agent", "two creators"). |
| 2026-10-25 | Report language vs prompt language | BE is bilingual; the GEO prompt was run only in French. | For bilingual markets run one prompt per official language, or list the missing language as a limit. |
