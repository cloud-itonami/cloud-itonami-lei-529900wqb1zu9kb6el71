# cloud-itonami-lei-529900wqb1zu9kb6el71

> **Independent third-party archive/analysis. Not affiliated with, endorsed by, or sponsored by Compañia de Minas Buenaventura S.A.A..**

This repository archives the publicly published Privacy Policy of **Compañia de Minas Buenaventura S.A.A.** (PE), with source-url and retrieval-date provenance, per
ADR-2607110300 (`cloud-itonami-lei-corporate-tos-catalog`, `com-junkawasaki/root`).
Read-only reference/archive repository — not a governed Advisor/Governor actor.

- LEI: `529900WQB1ZU9KB6EL71` (GLEIF entity status ACTIVE, registration LAPSED)
- Source: https://buenaventura.com/privacy-policy
- Retrieved: 2026-07-25T06:44:12Z
- SHA-256 of archived text: `b3d9c68a35a9bd8b7b3e33b874becfa2c4f8b2d14191542f2ad7476ea6e3ed6b`

Acquired by `scripts/lei-acquire.cljs` as part of the worldwide-broadening
continuation that followed the 2026-07-25 coverage audit, which found the
catalog's real reach was 27 countries with the United States at 55%.

## Verified registry facts

`facts.edn` records what GLEIF publishes about this LEI — the entity record, its
managing LOU and that LOU's accreditation, the Peruvian public register that
corroborated it, its ISO 20275 legal form, both parent-reporting exceptions, a
count of its instrument identifiers and its one direct child — with
`:source/url` and `:source/retrieved-at` next to every value. Ten entities, nine
cited URLs, all fetched on every run.

Three things in this record are worth reading before drawing conclusions from it.

**The company is ACTIVE; its LEI registration is LAPSED.** Those are two
different GLEIF fields and they are recorded separately. The registration was
due for renewal on 2019-10-09 and has not been renewed, which is also why GLEIF
flags it `NON_CONFORMING`; the last update to the record was 2021-07-19. None of
that says the company stopped existing — `:company/status` is `ACTIVE` and the
national register entry GLEIF cites (`:company/registered-as` `20100079501`,
at the Superintendencia Nacional de Registros Públicos) is unchanged. A stale LEI
registration is a fact about the registration.

**The instrument-identifier count is zero, and that is a measured zero.** The
cited ISIN page was fetched and reported an empty collection, so there are no
`:fact/kind :security` entities to look for. `:source/note` says so, so a bare
zero is never ambiguous between "GLEIF maps no instruments to this entity" and
"nobody asked".

**It reports no parent and still has a child.** Both parent-reporting exceptions
are present with reason `NON_CONSOLIDATING` — no parent consolidates this
entity — while `direct-children` lists Sociedad Minera El Brocal S.A.A., which
this entity does consolidate. That is coherent, not contradictory: the
exceptions are about what sits above it.

Two recorded values are third-party websites GLEIF publishes
(`:issuer/website`, `:authority/website`), not sources this repository fetches.
They are facts about GLEIF's record and are checked against GLEIF like any other
value; whether those sites answer from any given network is a separate question
and not one this repository claims.

`kbb --backend sci scripts/verify-facts.cljk` re-fetches those sources and compares. It exits
`0` when the live registry still agrees, `1` when a citation is dead or a value
drifted, and `3` when it could not check at all (sources unreachable, `facts.edn`
missing or unreadable) — a run that could not answer must not look like a pass.
`--write` regenerates the file through the same builder the check uses, so it
cannot drift from its own generator.
