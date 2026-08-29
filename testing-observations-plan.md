---
title: Testing Observations — Remediation Plan
---

# The Dark Index — Testing Observations & Remediation Plan

Compiled from initial hands-on testing, 2026-07-25. This tracks known gaps and bugs
against the current build, grouped into epics with suggested sequencing. Severity
reflects impact on core cataloguing workflows, not effort.

## Epic A: Shelving & Library Status (Critical)

The core "put a book somewhere and know what state it's in" loop is incomplete.

| # | Item | Severity | Notes |
|---|---|---|---|
| A1 | Shelving doesn't exist — no way to assign a book to a shelf at all | Critical | Blocks A2 and most of Epic B. This is the root gap. |
| A2 | Can't select a default shelf | High | Depends on A1 shipping first (default shelf needs shelf assignment to point at). |
| A3 | "Acquired" incorrectly means "added to library" | High | Data-model/semantics fix: acquisition (own it) and library membership (catalogued) are different states and need to be decoupled — likely a schema change, not just UI copy. |

**Sequencing:** A1 → A3 (fix status semantics before building default-shelf logic on top of them) → A2.

## Epic B: Organizational Structure — Rooms (High)

| # | Item | Severity | Notes |
|---|---|---|---|
| B1 | Can't add or remove rooms | High | Rooms appear to be a fixed/seeded list currently; needs CRUD. Likely shares data-model work with Epic A (rooms → shelves → books hierarchy). |

**Sequencing:** Can proceed in parallel with Epic A once the shelving data model is settled, since rooms likely sit one level above shelves.

## Epic C: Metadata & Discovery (High)

| # | Item | Severity | Notes |
|---|---|---|---|
| C1 | No series info / can't mark a book as part of a series | High | New metadata field + relation (series name, number in series). |
| C2 | No genre / thematic tags / general metadata | High | Needs a tagging system — likely many-to-many tags plus a distinct genre field. |
| C3 | Can't edit a book's format | Medium | Sounds like an existing field that's missing from the edit flow — smaller fix than C1/C2. |

**Sequencing:** C3 first (quick win, likely just an edit-form gap). C1 and C2 are bigger data-model additions and pair well with Epic D since scan-based catalogue lookups should populate series/genre/tags automatically once they exist.

## Epic D: ISBN Backend Catalogue (Critical)

| # | Item | Severity | Notes |
|---|---|---|---|
| D1 | Build a backend ISBN catalogue; scans currently don't auto-populate any book info | Critical | Scoped as **building an owned backend catalogue**, not just calling a third-party API at scan time. Implies: a service to ingest/store ISBN → book metadata, a sync/update strategy, and the scan flow calling into it. |

**Notes / open questions to resolve before scoping D1 further:**
- Data source strategy for seeding the catalogue (bulk import from a public dataset vs. building it up from user scans vs. a hybrid) — needs a decision before implementation starts.
- Given the app is described as "private-first," confirm how a scan (which implies an outbound lookup against your own backend) fits the privacy posture — may be worth a line in the privacy policy once this ships.
- This should populate title/author/format/genre/series where available, so it has a dependency on Epic C's fields existing first.

**Sequencing:** Data model from Epic C (esp. C1/C2) should land before D1's ingestion pipeline is finalized, so scans have somewhere to write series/genre/tags into.

## Epic E: UI / Theming / Polish (Medium)

| # | Item | Severity | Notes |
|---|---|---|---|
| E1 | No light theme — existing themes are too dark to be usable | Medium | Accessibility/usability issue, not just preference. |
| E2 | Android/iOS pages feel incomplete, need bottom buffer/padding | Low–Medium | Likely safe-area/inset handling on scrollable screens; check against notch/gesture-bar regions on both platforms. |

**Sequencing:** Independent of other epics — can run in parallel at any point, good candidate for a quick release alongside Epic C's edit-form fix (C3).

## Suggested Overall Sequencing

1. **Epic A** (A1 → A3 → A2) — unblocks core cataloguing, nothing else really works without this.
2. **Epic B** (rooms CRUD) — parallel with late Epic A once shelving data model settles.
3. **Epic C** (C3 quick win now; C1/C2 alongside/after Epic D planning).
4. **Epic D** (ISBN backend catalogue) — biggest lift, depends on Epic C fields existing.
5. **Epic E** (theme + mobile polish) — parallel track, no blocking dependencies.

## Next Steps

- [ ] Confirm this sequencing against actual app repo/codebase (this policies repo has no app source — plan should be filed as issues in the app repo once available).
- [ ] Decide ISBN catalogue seeding strategy for D1.
- [ ] Confirm data model changes needed for A3 (acquired vs. added) don't require a migration for existing users' data.
