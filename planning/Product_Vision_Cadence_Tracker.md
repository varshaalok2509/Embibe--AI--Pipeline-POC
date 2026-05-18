# Jio Education — Product Vision Cadence Tracker

**Cadence:** Weekly · starts week of 2026-05-25 · 45 min suggested
**Horizon:** 5–6 months, parallel tracks with staggered completion
**Purpose:** Bring visibility and structure to a currently reactive environment. Track five parallel threads shaping Jio Education's product vision, and act as the bridge between strategy and engineering through structured program management.

> **Source context:** Strategy meeting, 2026-05-18 — *Classroom integration and product roadmap: data pipeline, tooling, and LMS coupling.*

---

## How this doc works

- Each track has a fixed block: status, this-week / next-week, blockers, decisions needed, milestones.
- Update **in place** every week. Past weeks live in the change log at the bottom — don't spawn new files.
- Status colours: 🟢 on track · 🟡 at risk · 🔴 blocked / off track · ⚪ not started

---

## Snapshot — Week of 2026-05-18 (kickoff)

| # | Track | Owner / DRI | Status | Target outcome (5–6 mo) |
|---|-------|-------------|--------|--------------------------|
| 1 | Superr+ ↔ Embibe Integration | TBD | ⚪ | Superr+ user accesses Embibe via unified SSO/entitlement — live for ≥ 1 segment |
| 2 | Embibe Hardware Decoupling (IFPD, Smart TV, tablet, projector) | TBD | ⚪ | Single codebase running on ≥ 2 non-tablet form factors in a real classroom pilot |
| 3 | Data Pipeline for Non-Video Content Curation | TBD | ⚪ | Full CBSE 6 plug-and-play live (board + book + quiz); pattern proven for CBSE 7 |
| 4 | Productivity Tools for Content Creation Teams | Varsha Gajjar | ⚪ | ≥ 2 tools shipped; measurable throughput uplift vs baseline |
| 5 | Full Integration into Educational Ecosystem (LMS / ERP / Attendance) | TBD | ⚪ | Live LMS + TeachLite demo in a real school — "slots into what you have" |

**Top 3 things needed from kickoff meeting:**
1. Confirm DRI for each of the 5 tracks.
2. Lock the 5–6 month staggered timeline (which track lands first / last).
3. Agree success metrics per track.

---

## Guiding principles (from 2026-05-18 strategy session)

- **Ship what's curatable, defer what isn't.** NCERT-based CBSE 6/7 content is curatable end-to-end; ICSE is not — don't block on it.
- **Plug-and-play across K-12** is the long-term shape: boards × books × quizzes seamlessly stitched.
- **No full AI video generation.** Tooling investments accelerate existing creator workflows, they don't replace creators.
- **LMS is a coupling requirement, security is optional** for the first integration wave — pick the fights that unlock schools.
- **Parallel, staggered, 5–6 months.** Tracks run concurrently with different finish lines, not a single big-bang release.

---

## 1. Superr+ ↔ Embibe Integration

- **Objective:** Define and deliver the integration surface between Superr+ and Embibe.
- **🎯 Target outcome (5–6 mo):** A Superr+ user accesses Embibe content and learning flows from inside Superr+ through unified sign-on, entitlement, and UX — live in production for at least one user segment.
- **Success measures:** SSO success ≥ 95% · ≥ 1 segment live in prod · weekly Embibe sessions originating from Superr+ trending up
- **Owner / DRI:** TBD
- **Status:** ⚪
- **Why this matters:** Foundational coupling — many downstream tracks (ecosystem, hardware) assume this exists.

**Open questions to close in week 1**
- What does "integration" mean here — entitlement, content, UX shell, all three?
- Which side owns the user identity / session?
- Hard deadline driven by any Superr+ release?

**Milestones**
- [ ] Integration scope doc signed off
- [ ] Tech approach agreed with engineering
- [ ] First end-to-end flow in staging
- [ ] Pilot live

**This week** —
**Next week** —
**Blockers / risks** —
**Decisions needed** (who · by when) —
**Dependencies:** Feeds Track 5 (ecosystem) and Track 2 (hardware shell).

---

## 2. Embibe Hardware Decoupling — IFPD, Smart TV, Tablet, Projector

- **Objective:** Make Embibe deployable across classroom hardware (IFPDs, smart TVs, tablets, projectors) without forking the product, with multi-language support expansion.
- **🎯 Target outcome (5–6 mo):** Embibe runs from a single codebase on **at least two non-tablet form factors** (IFPD + Smart TV minimum) in a real classroom pilot, with multi-language support enabled.
- **Success measures:** ≥ 2 non-tablet form factors live · ≥ 1 school pilot completed · zero hardware-specific forks in codebase · ≥ N languages supported
- **Owner / DRI:** TBD
- **Status:** ⚪
- **Why this matters:** Schools have heterogeneous hardware. A single decoupled core unblocks classroom rollout.

**Target form factors**
| Form factor | Stage (scoping / build / pilot / live) | Owner | Notes |
|---|---|---|---|
| IFPD |  |  | Primary classroom surface |
| Smart TV |  |  |  |
| Tablet |  |  | Existing baseline |
| Projector |  |  |  |

**Workstreams**
- [ ] Reference architecture for hardware-agnostic layer
- [ ] Multi-language support expansion plan
- [ ] First non-tablet pilot (IFPD likely)
- [ ] Rollout playbook for schools

**This week** —
**Next week** —
**Blockers / risks** —
**Decisions needed** —
**Dependencies:** Track 5 (TeachLite-board schools are the pilot site).

---

## 3. Data Pipeline for Non-Video Content Curation

- **Objective:** Build a pipeline that ingests, tags, and curates non-video learning content at scale — flagship use case being **full CBSE Grade 6 integration on NCERT**.
- **🎯 Target outcome (5–6 mo):** A fully curated **CBSE Grade 6 plug-and-play experience** live in product — board + book + quiz seamlessly stitched — with the pattern proven repeatable for CBSE Grade 7.
- **Success measures:** 100% of CBSE 6 NCERT chapters curated · quizzes auto-generated from curated content · CBSE 7 ingestion started · pipeline cycle time per chapter documented
- **Owner / DRI:** TBD
- **Status:** ⚪
- **Why this matters:** Unlocks seamless quiz/book/board interactions; the curation backbone for every classroom surface.

**Scope decisions already made**
- ✅ NCERT enables curation for CBSE 6th and 7th — start here.
- ❌ ICSE content not available for curation — deferred, not in scope this horizon.
- 🎯 Flagship deliverable: **plug-and-play CBSE 6 experience** — board + book + quiz integrated.

**Pipeline stages — health check**
| Stage | Status | Notes |
|---|---|---|
| Source / ingest (NCERT) |  |  |
| Normalisation & tagging |  |  |
| Quiz generation from curated content |  |  |
| QA / review |  |  |
| Publish to product surfaces |  |  |

**Milestones**
- [ ] POC: CBSE 6 chapter end-to-end through pipeline
- [ ] Full CBSE 6 curated set
- [ ] Extend to CBSE 7
- [ ] Pattern documented for next board

**This week** —
**Next week** —
**Blockers / risks** —
**Decisions needed** —
**Dependencies:** Track 4 (creator tooling output feeds this); Track 2 & 5 (consume on classroom surfaces).

---

## 4. Productivity Tools for Content Creation Teams (Varsha Gajjar & team)

- **Objective:** Accelerate the content creation team's existing workflows with targeted tools. **Not building full AI video generation** — that path was ruled out as unfeasible.
- **🎯 Target outcome (5–6 mo):** Varsha Gajjar's team produces measurably more content per unit time, using ≥ 2 in-house productivity tools, with a documented baseline-vs-uplift comparison.
- **Success measures:** ≥ 2 tools shipped and adopted · target ≥ 30% reduction in time-per-asset (set with team) · weekly throughput trending up vs baseline
- **Owner / DRI:** Varsha Gajjar
- **Status:** ⚪
- **Why this matters:** Creator throughput is the rate-limiter on every content-dependent track. Tools must speed humans, not replace them.

**Scope guardrail**
- ❌ End-to-end AI video creation — not pursuing.
- ✅ Workflow accelerators — scripting aids, asset prep, review/QA tooling, repetitive-step automation.

**Pain points → tooling bets**
| Pain point | Proposed tool | Stage | Owner |
|---|---|---|---|
|  |  |  |  |
|  |  |  |  |

**Milestones**
- [ ] Pain-point audit with Varsha Gajjar's team
- [ ] Baseline throughput measured (units / week, time-per-asset)
- [ ] First tool rolled out
- [ ] Throughput uplift measured vs baseline

**This week** —
**Next week** —
**Blockers / risks** —
**Decisions needed** —
**Dependencies:** Output feeds Track 3 pipeline.

---

## 5. Full Integration into Educational Ecosystem

- **Objective:** Position Embibe as a connected layer in the school ecosystem — LMS, ERP, attendance — with a credible demo for schools that already run an LMS + TeachLite boards.
- **🎯 Target outcome (5–6 mo):** A live, demo-able school deployment where Embibe is integrated with the school's existing LMS and running on TeachLite boards — proving the "slot into what you already have" story for sales conversations.
- **Success measures:** ≥ 1 LMS integration live in a real school · TeachLite board demo working end-to-end · ERP and attendance integration scoping signed off · LMS shortlist documented
- **Owner / DRI:** TBD
- **Status:** ⚪
- **Why this matters:** Schools won't adopt point products. The win is "Embibe slots into what you already have."

**Coupling stance (locked 2026-05-18)**
| System | Coupling | Notes |
|---|---|---|
| LMS | **Essential** | Research top platforms; build for compatibility |
| ERP | In scope | Depth TBD |
| Attendance tracking | In scope | Depth TBD |
| Security/SSO etc. | Optional (first wave) | Revisit later |

**Workstreams**
- [ ] Research top LMS platforms in the Indian school market — shortlist for first integrations
- [ ] Define LMS integration contract (data model, auth, content handoff)
- [ ] Demo: school with existing LMS + TeachLite board running Embibe seamlessly
- [ ] ERP / attendance integration scoping

**This week** —
**Next week** —
**Blockers / risks** —
**Decisions needed** —
**Dependencies:** Touches all other tracks; particularly Track 1 (Superr+) and Track 2 (hardware).

---

## Cross-track view

### Dependency map
- **Track 3 → Track 2 & 5:** No curated content = no classroom demo. Pipeline output must be ready before hardware pilots get a real story.
- **Track 4 → Track 3:** Creator tools determine the rate at which the pipeline gets fed.
- **Track 1 → Track 5:** Superr+ integration is a building block of the ecosystem story.
- **Track 2 ↔ Track 5:** TeachLite-board schools are the natural pilot for both.

### Shared risks
- **Content availability outside NCERT** (e.g. ICSE) — bounded for this horizon, but will resurface.
- **Engineering bandwidth** across 5 parallel tracks — staggered completion is the mitigation; needs explicit sequencing.
- **DRI ambiguity** — 4 of 5 tracks still TBD as of kickoff.

### Resourcing conflicts
-

---

## Decisions log

| Date | Decision | Track | Decided by | Notes |
|---|---|---|---|---|
| 2026-05-18 | Full AI video creation is out of scope | 4 | Strategy session | Pivot to workflow accelerators |
| 2026-05-18 | NCERT-based CBSE 6/7 is the curation flagship | 3 | Strategy session | ICSE deferred — content not curatable |
| 2026-05-18 | LMS coupling = essential; security = optional (first wave) | 5 | Strategy session |  |
| 2026-05-18 | Five-track parallel program over 5–6 months, staggered | All | Strategy session | Weekly cadence starts w/o 2026-05-25 |

---

## Parking lot / open questions

- ICSE curation pathway — revisit once NCERT flagship lands.
- Security / SSO coupling depth for LMS integration.
- Which board comes after CBSE 6/7?
- Program-management bridge to engineering — formal RACI?

---

## Change log (weekly snapshots)

### Week of 2026-05-18 — Kickoff
- **Headline:** Five tracks identified; strategy session locked scope guardrails (no full AI video, NCERT-first curation, LMS essential).
- **Action:** Varsha to share initial thoughts by 2026-05-19; this week's meeting finalises strategy; regular cadence starts w/o 2026-05-25.
- **Open:** DRIs for tracks 1, 2, 3, 5.
