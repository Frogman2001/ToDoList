# PRD Quality Review — ToDoList (Project 1)

## Overall verdict
A tight, hobby-scale PRD with a clear thesis (date-driven display over plain data, fast capture) and testable requirements. The main risks are a missing cross-cutting requirements section for a multi-user production app, and a few date-edge behaviors that the PRD leaves implicit.

## Decision-readiness — strong
Decisions are stated as decisions (Monday week start, next week/month meaning, drag-reschedules). Assumptions are tagged and indexed.

## Substance over theater — strong
One persona-style journey pair, no furniture sections. The vision is specific to this product.

## Strategic coherence — strong
Features follow from the thesis. SM-2 tests the real motivation. No counter-metric, which is a deliberate choice (no feature cap).

## Done-ness clarity — adequate
### Findings
- **medium** No cross-cutting requirements (§4). Multi-user production data and two clients share date rules. *Fix:* add a short cross-cutting section: users' data isolated from each other; sign-in required for any data access; both clients show identical results for the same data (same Today, week, ordering).
- **low** FR-7 Hide completed does not say whether the choice persists across views or sessions. *Fix:* state it or leave to UX.
- **low** UJ-1 says items are captured "in seconds" without a bound. *Fix:* acceptable at hobby scale, or add a target.

## Scope honesty — strong
Non-goals and out-of-scope are explicit. Open-items density is low (2 assumptions, 1 UX note).

## Downstream usability — adequate
### Findings
- **low** Midnight rollover and time zone are not addressed: what happens when the date changes while the app is open, or a user travels. *Fix:* defer to architecture or add one line to FR-4.
- **low** Rescheduling "next week" on a Sunday lands on tomorrow. Correct under the stated rule; worth a UX note.

## Shape fit — strong
Hobby/solo shape, light journeys, capability-first features.

## Mechanical notes
- Fixed: section numbering (2.3 → 2.2).
- Fixed: "add box" vs "add control" drift; both now "add control", added to Glossary. "Overdue item" added to Glossary.
- Fixed: Assumptions Index now matches inline tags (FR-4, FR-9, FR-12).
- IDs: FR-1 to FR-13, UJ-1 to UJ-2, SM-1 to SM-2 contiguous. Cross-references resolve.
