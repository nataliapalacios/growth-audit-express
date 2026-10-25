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
