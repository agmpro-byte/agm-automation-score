# Reframe changes — 2026-09-09 (branch `reframe-2026-09-09`, NOT pushed)

Brief: `docs/alden_briefs/2026-09-09_alden_website_messaging_update_handoff.md` (main repo).
Branch cut from `origin/main` @ `4bc41af` (local `main` was 2 commits behind; local `main` left untouched).
Structure check: tag sequence of every edited file is byte-identical before/after — only text nodes changed.

## Per file

- `index.html` — "Who is AGM Pro Tools?" footnote: vendor list (Jobber, FieldRoutes, Salesforce) replaced with the three integration categories and the promise line; "then do it" → "where supported, put approved follow-up into motion"; "our live clients" → "the businesses we operate and work with". Hero sub: "exactly how much revenue slips" → "an estimate of how much revenue may be slipping"; "the one thing to fix first" → "the first thing to fix". Aside: "is leaking money — and exactly what to fix first" → "may be leaking money — and what to fix first"; "#1 system to fix first — ranked by revenue impact" → "first system to fix — ranked by estimated revenue impact". Email gate: "revenue impact analysis" → "estimated revenue impact". Report gap page: "recoverable revenue your business is leaving on the table" → "an estimate, based on your answers, of revenue your business may be leaving on the table". Report CTA: "automates the exact gaps … Live in under 10 minutes" → "turns the gaps … into management priorities and, where supported, approved follow-up workflows … We confirm scope during setup"; "Works with the software you already run" → "Keep the software you already run".
- `jobber/index.html` — **NOT edited.** On `origin/main` (commit `6df0b6b`, live since Sep 7) it is an 892-byte redirect stub (`meta refresh` + `location.replace` to the root, keeps UTM query). The 93KB variant the task counted 17 mentions in existed only on the stale local `main`. Left as-is.

## Remaining Jobber mentions — `index.html`

| Line | Text | Kind |
|---|---|---|
| 1078–1087 | `if (window.CAS_VARIANT === 'jobber')` hero-swap block incl. the string "You run your jobs in Jobber…" | code reference, not copy (dead branch — nothing sets `CAS_VARIANT` now that `/jobber` redirects) |
| 1368 | `options: ["Jobber", "Housecall Pro", …]` | code reference — quiz answer option value (data, feeds the lead record) |
| 1478–1481 | `CAS_VARIANT === 'jobber'` pre-answer | code reference, not copy |
| 2289 | "…and Jobber industry benchmarks." in the report's statistics-source note | copy — a source citation, not positioning; left in place, flagged below |
| `jobber/index.html` line 10 | JS comment in the redirect stub | code reference |

## Omitted / retained claims awaiting evidence (not edited — inside JS data or pricing copy)

- Gap-card `fix:` strings (lines 2097–2117) carry unverified numbers: "recovers 15-30% of quotes", "convert at 3-5x", "double their review count within 90 days", "recovers 10-20% of stale quotes", "never miss an inbound call. One setup, runs forever", "No human needed". These render into the report. Inside JS data → left per the no-JS rule. **Needs Troy:** approve rewording (then it is a 5-string edit) or supply sources.
- Report "90-Day ROI Projection" table ("Projected recovery at 60%") — a projection with an unsourced 60% assumption. Left; label already says "Projected".
- "No setup fee" (report CTA) and "Cancel anytime" — pricing claims retained as-is, not verified against the live Stripe product.
- Hero stat "23 Questions" — matches commit `4bc41af`; not re-counted against the live quiz.
- Line 2289 "Jobber industry benchmarks" citation — keep only if the benchmark source is documented.

## Needs Troy

1. Ruling on the five gap-card numeric claims above (reword vs. source).
2. Confirm the report CTA price "$297/mo" + "No setup fee" match the live checkout product.
3. Merge/push decision — a push publishes live.
