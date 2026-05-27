# Jio Education — Product Vision Cadence Tracker

**Owner:** Varsha Alok
**Cadence:** Weekly · starts week of 2026-05-25 · 45 min suggested
**Horizon:** 5–6 months, parallel tracks with staggered completion
**Purpose:** Bring visibility and structure to a currently reactive environment. Track five parallel verticals shaping Jio Education's product vision, and act as the bridge between strategy and engineering through structured program management.

> **Source context:** Strategy session, 2026-05-18 — *Classroom integration and product roadmap: data pipeline, tooling, and LMS coupling.*

---

## How this doc works

- Each vertical has a fixed block: target outcome, success measures, status, this-week / next-week, blockers, decisions needed, milestones.
- Update **in place** every week. Past weeks live in the change log at the bottom — don't spawn new files.
- Status colours: 🟢 on track · 🟡 at risk · 🔴 blocked / off track · ⚪ not started

---

## Snapshot — Week of 2026-05-18 (kickoff)

| # | Vertical | Owner / DRI | Status | Target outcome (5–6 mo) |
|---|----------|-------------|--------|--------------------------|
| 1 | **TeachLite 2.0** (Superr + Embibe, bundled with Jio — ERP must-have) | TBD | ⚪ | Bundled TeachLite 2.0 offering live, with Superr + Embibe + ERP integrated as a single Jio classroom package |
| 2 | **AI Pipeline** (Embibe + Superr + other curation paths) | TBD | ⚪ | Unified AI/curation pipeline leveraging Embibe's existing, Superr's, and external curation options — feeding all content surfaces |
| 3 | **Productivity Tools for Gap-Filling Content** | Varsha Gajjar | ⚪ | Tools enabling Embibe to gap-fill relevant, required content at speed — measurable reduction in content gaps |
| 4 | **Decoupling Superrboard** (must support IFP panels) | TBD | ⚪ | Superrboard runs from a decoupled core on IFP panels (and other non-original form factors) without forking |
| 5 | **Decluttering Embibe Apps & 360 Offerings** (standalone) | TBD | ⚪ | A clean, rationalised standalone Embibe product surface — fewer apps, sharper 360 offering |

**Top 3 things needed from kickoff meeting:**
1. Confirm DRI for each of the five verticals.
2. Lock the 5–6 month staggered timeline — which vertical lands first / last.
3. Agree success measures per vertical (the placeholders below need owner sign-off).

---

## Guiding principles (from 2026-05-18 strategy session)

- **Bundled is the wedge.** Jio sells TeachLite 2.0 as a package — Superr + Embibe + ERP — not as point products.
- **Curate what's curatable, defer what isn't.** NCERT-based CBSE 6/7 is curatable end-to-end; ICSE is not — don't block on it.
- **Plug-and-play across K-12** is the long-term shape: boards × books × quizzes seamlessly stitched.
- **No full AI video generation.** Tooling investments accelerate existing creator workflows; they don't replace creators.
- **Standalone Embibe needs decluttering, not extension.** The 360 offering wins by being sharper, not larger.
- **Parallel, staggered, 5–6 months.** Tracks run concurrently with different finish lines, not a single big-bang release.

---

## 1. TeachLite 2.0 — Superr + Embibe (Bundled Jio Offering)

- **Objective:** Deliver TeachLite 2.0 as a bundled Jio classroom package: Superr + Embibe + ERP, sold as one.
- **🎯 Target outcome (5–6 mo):** TeachLite 2.0 bundle live and sellable — a school can buy one SKU and get Superr, Embibe, and ERP working together out of the box.
- **Success measures:** Bundle SKU defined and priced · ERP integrated end-to-end · Embibe + Superr unified entitlement · ≥ 1 school onboarded on the bundle · sales-ready demo script
- **Owner / DRI:** TBD
- **Status:** ⚪
- **Why this matters:** This is the commercial wedge — bundled Jio is what differentiates against point-product competitors.

**Coupling stance**
| Component | Coupling | Notes |
|---|---|---|
| Superr | Must-have | Identity / entitlement layer |
| Embibe | Must-have | Content + learning surface |
| ERP | **Must-have** | Confirmed essential for bundle (not optional) |
| LMS | Essential (parallel) | Pursued under integration work |
| Security / SSO | Optional first wave | Revisit later |

**Milestones**
- [ ] Bundle scope + SKU defined
- [ ] ERP integration scoped with vendor(s)
- [ ] Superr ↔ Embibe entitlement flow live in staging
- [ ] First bundled school onboarded
- [ ] Sales playbook + demo

**This week** —
**Next week** —
**Blockers / risks** —
**Decisions needed** —
**Dependencies:** Vertical 4 (Superrboard hardware) for classroom delivery; Vertical 2 (AI pipeline) for content feeding the bundle.

---

## 2. AI Pipeline — Embibe + Superr + Other Curation Paths

- **Objective:** Build one AI/curation pipeline that leverages Embibe's existing pipeline, Superr's capabilities, and external curation options — feeding every content surface.
- **🎯 Target outcome (5–6 mo):** A unified pipeline in production, ingesting from at least three sources (Embibe's own, Superr's, one external), with CBSE 6 NCERT end-to-end as the proof point.
- **Success measures:** ≥ 3 curation sources integrated · CBSE 6 plug-and-play live (board + book + quiz) · pipeline cycle time per chapter documented · CBSE 7 ingestion started
- **Owner / DRI:** TBD
- **Status:** ⚪
- **Why this matters:** Content is the rate-limiter for everything else. Pipeline duplication across orgs is the cost we're cutting.

**Source inventory**
| Source | Type | Stage (scoping / build / live) | Notes |
|---|---|---|---|
| Embibe existing pipeline |  |  | Brownfield — what works, what to keep |
| Superr's pipeline |  |  | What's reusable; integration approach |
| External curation (e.g. NCERT) |  |  | CBSE 6/7 flagship |
| Other |  |  |  |

**Scope decisions already made**
- ✅ NCERT enables curation for CBSE 6/7 — flagship use case.
- ❌ ICSE content not available for curation — deferred.

**Milestones**
- [ ] Audit of Embibe + Superr pipelines (what to keep, merge, retire)
- [ ] Unified pipeline architecture signed off
- [ ] CBSE 6 POC end-to-end
- [ ] CBSE 6 full curated set live
- [ ] Extend to CBSE 7

**This week** —
**Next week** —
**Blockers / risks** —
**Decisions needed** —
**Dependencies:** Vertical 3 (productivity tools) feeds gap-fill content into this pipeline.

---

## 3. Productivity Tools for Gap-Filling Content (Varsha Gajjar & team)

- **Objective:** Build tools that let Embibe **gap-fill the relevant, required content** the curriculum needs — fast. Not full AI video generation (ruled out); workflow accelerators that close content gaps.
- **🎯 Target outcome (5–6 mo):** Measurable reduction in identified content gaps for the priority boards/grades — driven by ≥ 2 in-house productivity tools shipped to Varsha Gajjar's team.
- **Success measures:** Content-gap baseline measured · gap closure rate per month tracked · ≥ 2 tools shipped and adopted · time-per-asset reduction documented (target set with team)
- **Owner / DRI:** Varsha Gajjar
- **Status:** ⚪
- **Why this matters:** Embibe's coverage gaps are the gating risk for the bundled offering. Tools must enable the team to close those gaps faster than manual production allows.

**Scope guardrail**
- ❌ End-to-end AI video creation — not pursuing.
- ✅ Workflow accelerators: scripting aids, asset prep, review/QA tooling, repetitive-step automation.

**Gap → tooling bets**
| Identified content gap | Proposed tool | Stage | Owner |
|---|---|---|---|
|  |  |  |  |
|  |  |  |  |

**Milestones**
- [ ] Content-gap audit complete (priority boards/grades)
- [ ] Baseline throughput + gap inventory documented
- [ ] First tool shipped
- [ ] Gap closure rate measured
- [ ] Second tool shipped

**This week** —
**Next week** —
**Blockers / risks** —
**Decisions needed** —
**Dependencies:** Output feeds Vertical 2 (AI pipeline). Gap inventory should reuse existing Embibe content-gap analysis where possible.

---

## 4. Decoupling Superrboard — IFP Panel Support

- **Objective:** Decouple Superrboard from its original hardware so it runs on IFP panels (and other classroom form factors) from a single codebase.
- **🎯 Target outcome (5–6 mo):** Superrboard live on IFP panels in a real classroom pilot, with zero hardware-specific forks in the codebase.
- **Success measures:** IFP panel pilot live · ≥ 1 additional non-original form factor supported · zero forks · multi-language support enabled
- **Owner / DRI:** TBD
- **Status:** ⚪
- **Why this matters:** Schools have heterogeneous hardware. IFP panels are the dominant classroom surface — Superrboard has to meet them where they are.

**Target form factors**
| Form factor | Stage (scoping / build / pilot / live) | Owner | Notes |
|---|---|---|---|
| **IFP panel** |  |  | **Must-have** |
| Smart TV |  |  |  |
| Tablet |  |  | Existing baseline |
| Projector |  |  |  |

**Milestones**
- [ ] Reference architecture for hardware-agnostic Superrboard core
- [ ] IFP panel pilot in one school
- [ ] Multi-language support live
- [ ] Rollout playbook documented

**This week** —
**Next week** —
**Blockers / risks** —
**Decisions needed** —
**Dependencies:** Vertical 1 (TeachLite 2.0 bundle uses Superrboard as the classroom delivery surface).

---

## 5. Decluttering Embibe Apps & 360 Offerings (Standalone)

- **Objective:** Rationalise the standalone Embibe product surface — fewer apps, sharper 360 offering, less duplication. This is the **non-bundled** play, distinct from TeachLite 2.0.
- **🎯 Target outcome (5–6 mo):** A consolidated standalone Embibe offering — clear app inventory, decisions on what to merge/retire/keep, and at least one visible decluttering milestone shipped to users.
- **Success measures:** App / surface inventory documented · keep/merge/retire decisions made for each · ≥ 1 user-visible consolidation shipped · 360 offering narrative agreed and signed off
- **Owner / DRI:** TBD
- **Status:** ⚪
- **Why this matters:** Standalone Embibe is the consumer/independent-school play. It wins by being sharper, not larger — and current sprawl is hurting both UX and brand clarity.

**Inventory — surfaces under review**
| App / surface | Current state | Proposed action (keep / merge / retire) | Notes |
|---|---|---|---|
|  |  |  |  |
|  |  |  |  |

**Milestones**
- [ ] Full inventory of Embibe apps and 360 offering components
- [ ] Keep / merge / retire decisions
- [ ] First consolidation shipped
- [ ] 360 offering narrative finalised
- [ ] Comms / migration plan for any retirements

**This week** —
**Next week** —
**Blockers / risks** —
**Decisions needed** —
**Dependencies:** Largely independent of the other verticals. Watch for content/feature reuse with Vertical 1 (bundle) so consolidation doesn't break bundle commitments.

---

## Cross-vertical view

### Dependency map
- **Vertical 2 → Vertical 1 & 3:** AI pipeline output feeds the bundle (V1) and is fed by gap-fill tools (V3).
- **Vertical 4 → Vertical 1:** Superrboard on IFP panels is the classroom delivery for the TeachLite 2.0 bundle.
- **Vertical 3 → Vertical 2:** Productivity tools produce content that the pipeline ingests.
- **Vertical 5:** Mostly independent — but consolidation decisions must respect bundle commitments.

### Shared risks
- **Engineering bandwidth** across 5 parallel verticals — staggered completion is the mitigation; explicit sequencing required.
- **Content availability outside NCERT** — bounded for this horizon but will resurface.
- **DRI ambiguity** — 4 of 5 verticals still TBD at kickoff.
- **Bundle vs standalone tension** (V1 vs V5) — decluttering must not undermine the bundle's value prop.

### Resourcing conflicts
-

---

## Decisions log

| Date | Decision | Vertical | Decided by | Notes |
|---|---|---|---|---|
| 2026-05-18 | Full AI video creation is out of scope | 3 | Strategy session | Pivot to workflow accelerators for gap-filling |
| 2026-05-18 | NCERT-based CBSE 6/7 is the curation flagship | 2 | Strategy session | ICSE deferred |
| 2026-05-18 | LMS coupling = essential; security = optional first wave | 1 | Strategy session |  |
| 2026-05-18 | ERP is a **must-have** for the TeachLite 2.0 bundle | 1 | Strategy session | Upgraded from "in scope" to "must-have" |
| 2026-05-18 | Five parallel verticals over 5–6 months, staggered | All | Strategy session | Weekly cadence starts w/o 2026-05-25 |
| 2026-05-18 | Standalone Embibe to be decluttered, not extended | 5 | Strategy session | Sharper, not larger |

---

## Parking lot / open questions

- ICSE curation pathway — revisit once NCERT flagship lands.
- Security / SSO coupling depth for LMS integration.
- Which board comes after CBSE 6/7?
- Program-management bridge to engineering — formal RACI?
- Retirement comms / migration plan format for Vertical 5 consolidations.

---

## Change log (weekly snapshots)

### Week of 2026-05-18 — Kickoff
- **Headline:** Five verticals locked: TeachLite 2.0 (bundle), AI Pipeline, Gap-fill Productivity Tools, Superrboard Decoupling, Embibe Decluttering. Scope guardrails set (no full AI video, NCERT-first, ERP must-have for bundle, standalone gets sharper not larger).
- **Action:** Varsha to share initial thoughts by 2026-05-19; this week's meeting finalises strategy; regular cadence starts w/o 2026-05-25.
- **Open:** DRIs for Verticals 1, 2, 4, 5.
