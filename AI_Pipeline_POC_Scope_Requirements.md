# AI Content Pipeline POC — Scope Document

---

## Table of Contents

1. [Overview](#1-overview)
2. [POC Objectives](#2-poc-objectives)
3. [Experiments at a Glance](#3-experiments-at-a-glance)
4. [Input](#4-input)
5. [Output](#5-output)
   - 5.1 [Curation approach](#51-curation-approach-experiments-1-2-and-the-curation-pass-of-3--4)
   - 5.2 [Generation approach](#52-generation-approach-experiments-3-and-4)
6. [How We Evaluate Output](#6-how-we-evaluate-output)
   - 6.1 [Scoring steps](#61-scoring-steps)
   - 6.2 [Scorecard](#62-scorecard)
   - 6.3 [Publish-ready threshold & decision rules](#63-publish-ready-threshold--decision-rules)
7. [Resources Needed](#7-resources-needed)
8. [Execution Plan](#8-execution-plan)

<div style="page-break-after: always;"></div>

## 1. Overview

Embibe's content gap is heavily skewed toward non-STEM subjects, primary grades, and vernacular mediums — segments where manual production is slow, and hard to prioritize.

This POC runs four controlled experiments to test two AI-native production approaches side-by-side: one that curates existing open-source content, and one that generates original content from scratch.

The goal is to answer three questions:

1. **Is the output quality good enough to publish?**
2. **Does it actually fill the content gaps Embibe has today?**
3. **Is it faster and more cost-effective than how Embibe produces content today?**

<div style="page-break-after: always;"></div>

## 2. POC Objectives

This POC tests two production approaches:

- **Curation** — AI shortlists and packages existing open-source content (NCERT PDFs, vetted YouTube channels) against a specific chapter-topic combination.
- **Generation** — AI produces original Embibe-branded content end-to-end (script → video → voice → metadata).

The three objectives:

1. **Use Curation to cover the gaps we choose not to prioritize now** — primary grades, vernacular, and non-STEM subjects where manual production isn't commercially justified.
2. **Use Generation to expedite studio-quality production** — turn weeks of scripting, shooting, and post-production into days, so we can publish original Embibe-branded content for core CBSE middle-school subjects at a fraction of current time and cost, with full brand and IP control.
3. **Validate every output against a single quality scorecard** — every topic, every approach, scored the same way, so we have measurable evidence (not opinion) on where each approach works and where it doesn't.

<div style="page-break-after: always;"></div>

## 3. Experiments at a Glance

All experiments: CBSE board, 1 chapter × 3 topics each.

| #     | Approach       | Gr  | Subject         | Chapter — *Topics*                                                                                                                                                     | Lang |
| ----- | -------------- | --- | --------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- |
| **1** | Curation       | 5   | English         | **The Rainbow** (Santoor) — *Theme & meaning; New vocabulary; Poetic devices (rhyme, imagery)*                                                                         | En   |
| **2** | Curation       | 6   | Hindi           | **Malahar** — *Theme & imagery; Vocabulary & phrases; Poetic devices*                                                                                                  | Hi   |
| **3** | Gen + Curation | 6   | SST (History)   | **Timeline and Sources of History** — *Dating conventions (BCE/CE, timelines); Sources of history (literary, archaeological, oral); How historians construct the past* | En   |
| **4** | Gen + Curation | 8   | SST (Geography) | **Natural Resources and Their Use** — *Types of resources (renewable vs non-renewable, biotic vs abiotic); Distribution and human use; Conservation and sustainable use* | En |

For Experiments 3 and 4, we run the **same topics through both Curation and Generation** — so we can compare the two approaches side-by-side on identical input and see which one produces better output for the same chapter.

<div style="page-break-after: always;"></div>

## 4. Input

Every experiment starts with the same input, regardless of approach.

| Field               | Description                                                          |
| ------------------- | -------------------------------------------------------------------- |
| Board               | CBSE                                                                 |
| Grade               | 5 / 6 / 8                                                            |
| Subject             | As per experiment                                                    |
| Chapter + Topics    | 1 chapter, 3 topics scoped per experiment                            |
| Language            | English or Hindi                                                     |
| Learning objectives | 4–6 per topic, sourced from NCERT syllabus                           |
| Reference material  | NCERT textbook PDF for the chapter, NCFSE document, Youtube Channels |

<div style="page-break-after: always;"></div>

## 5. Output

### 5.1 Curation approach (Experiments 1, 2, and the curation pass of 3 & 4)

| Artifact         | Detail                                                                                      |
| ---------------- | ------------------------------------------------------------------------------------------- |
| Curated resource | 1 YouTube video segment (with start/end timestamps) **or** 1 NCERT PDF excerpt (page range) |
| Topic summary    | ~300-word explainer in target language                                                      |
| Key concepts     | 5–7 tagged terms with definitions, flowcharts and infographics (as relevant)                |
| Assessment       | 10 MCQs + 5 short-answer questions with model answers                                       |
| Metadata         | Learning objectives covered, prerequisites, difficulty, Bloom's level                       |
| Source record    | Original URL, creator, license type, attribution text                                       |

**YouTube source channels (starting allowlist — curation is restricted to vetted educational channels):**
- Magnet Brains
- LearnoHub — Class 6, 7, 8
- Next Toppers Juniors
- NCERT Official
- BodhaGuru Learning

### 5.2 Generation approach (Experiments 3 and 4)

| Artifact                 | Detail                                                                  |
| ------------------------ | ----------------------------------------------------------------------- |
| Explainer video          | Original, 8–12 min, AI cloned voice, 1080p, captions embedded           |
| Script                   | LO-aligned lesson with explanation, examples, check-for-understanding   |
| Visual assets            | Slides, diagrams, images; 1 simulation or 3D asset where topic warrants |
| Transcript + key moments | Timestamped transcript, 3–6 key moments for jump-to navigation          |
| Assessment               | 10 MCQs + 5 short-answer questions with model answers                   |
| Metadata                 | Learning objectives covered, prerequisites, difficulty, Bloom's level   |
| Provenance record        | Models used, voice-clone ID, generation timestamp                       |

<div style="page-break-after: always;"></div>

## 6. How We Evaluate Output

### 6.1 Scoring steps

**Step 1 — Automated scoring (LLM-as-judge)**
An LLM scores every topic against the scorecard below and flags factual errors, LO drift, and anything scoring low for human review.

**Step 2 — Human review (Content Quality reviewer)**
The Content Quality reviewer (human-in-loop) spot-checks every topic, validates the LLM scores, and makes the final pass/fail call.

### 6.2 Scorecard

Each criterion is scored 0–5 and combined via the weights below.

| Criterion | Wt. | Check |
|---|---|---|
| **Factual accuracy** | 25% | Every claim correct. One error = hard stop. |
| **Curriculum alignment** | 20% | Covers every input LO, stays on-syllabus. |
| **Pedagogical quality** | 15% | Opening, examples, check-for-understanding, recap. |
| **Age appropriateness** | 10% | Vocabulary and examples fit the grade. |
| **Engagement** | 10% | A student in that grade would stay through it. |
| **Production quality** | 10% | Clean audio, captions, visuals, working links. |
| **Language fidelity** | 5% | Natural phrasing, correct grammar (Hindi/regional only). |
| **Safety & bias** | 5% | No religious/political/gender/caste/commercial bias. |

*How each is checked:* LLM-as-judge scores every criterion against the NCERT reference (claims, LO coverage, structure, readability, pacing, audio/caption/link checks, bias classifier). The Content Quality reviewer validates LLM scores, spot-checks facts and clips, and makes the final call. Language fidelity uses a native-speaker reviewer; skipped for English-only (weight redistributed).

### 6.3 Publish-ready threshold & decision rules

**Publish-ready threshold:** weighted score ≥ **3.8 / 5.0 (76%)**, no single criterion below **3.0 / 5.0 (60%)**, zero factual errors.

**What counts as a factual error:**
- Incorrect dates, names, places, definitions, or formulae
- Misstated cause-effect, sequence, or relationships (e.g., wrong chronology, wrong branch of government)
- Hallucinated sources, quotes, or statistics
- Misalignment with NCERT/prescribed textbook content for the same topic
- Any claim that contradicts the reference material provided as input

**Decision:**
- ≥ 3.8 / 5.0 (76%), zero factual errors → green-light scale-up for that approach × gap type
- Below 3.8 / 5.0 (76%) → iterate and re-run, or drop the approach for that gap
- Any factual error → hard stop, do not publish

<div style="page-break-after: always;"></div>

## 7. Resources Needed

Lean POC team. 4–5 people total.

| Role                                | Count  | Scope / Skills                                                                                                                                                        |
| ----------------------------------- | ------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **POC lead (PM)**                   | 1      | End-to-end owner, weekly reviews, decision memo                                                                                                                       |
| **Engineer**                        | 2      | One runs the curation pipeline + NCERT PDF ingestion; one runs the generation stack (scripting, video, voice). Skills: LLM orchestration, video/voice tooling, Python |
| **Human-in-loop — Content Quality** | 1 or 2 | Validates LLM scorecard ratings, does final pass/fail review, flags factual errors                                                                                    |

**Tools & platforms**
- **Curation stack:** existing Superr backend (YouTube scraper, curriculum graph, tagging) + lightweight NCERT PDF ingestion module
- **Generation stack:** LLM for scripting, text-to-video, voice cloning (English + Hindi), image/diagram generation
- **Transcription:** Whisper for English; IndicWhisper or equivalent for Hindi; regional language models (Tamil, Bengali, Telugu, Marathi, etc.) to be added as scope expands
- **Evaluation:** LLM-as-judge pipeline running the scorecard; shared scoring sheet for human-in-loop validation
- **Storage:** existing Embibe content DB + object storage (GCS / S3 for video, PDF, and transcript artifacts)

<div style="page-break-after: always;"></div>

## 8. Execution Plan

### Phase 1 — Setup
*Get the inputs, tools, and scoring prompt ready so the team can actually start running experiments.*

1. Lock topic IDs, learning objectives, and reference NCERT PDFs for all 4 experiments (TOC)
2. Finalize the YouTube source channel list for curation
3. Build the NCERT PDF reader module so the curation pipeline can ingest textbook pages
4. Get the generation tools ready — pick and set up the LLM for scripting, the text-to-video tool, and the voice-cloning tool
5. Set up the automated scoring — write the scorecard as an LLM prompt and run it on a sample to confirm it scores sensibly

### Phase 2 — Calibration
*Run two trial topics, compare LLM scores against the reviewer's scores, and tune the LLM prompt until the two agree.*

6. Run 1 topic through the curation approach as a trial
7. Run 1 topic through the generation approach as a trial
8. Content Quality reviewer watches/reads both trial outputs end-to-end and fills a simple scoring sheet — one row per topic, one column per criterion, short notes on anything that looks off
9. Engineer runs the LLM on the same two outputs and drops its scores into the same sheet alongside the reviewer's
10. Reviewer, PM, and engineer walk through the sheet together — flag every place the LLM missed a factual error the reviewer caught, over-scored a criterion, or used signals the reviewer disagrees with
11. Update the LLM prompt for the flagged criteria (e.g., "also check for NCERT chronology", "weigh the opening more heavily for engagement")
12. Re-run the LLM on the same two outputs and walk through again, until the reviewer is comfortable the LLM flags what it should
13. Freeze the scoring sheet and the LLM prompt before Phase 3 begins

### Phase 3 — Run
*Produce content for all four experiments using the approach assigned to each.*

14. Run Experiments 1 and 2 through the curation approach
15. Run Experiments 3 and 4 through both curation and generation

### Phase 4 — Score
*Score every topic, LLM first and then human reviewer, to get one consistent quality read per output.*

16. LLM scores every topic and prepares the list for Content Reviewer
17. Content Quality reviewer (human-in-loop) validates, flags factual errors, and makes the final pass/fail call

### Phase 5 — Decide
*Look at the scores, pick which approach scales into which gap, and take the go/no-go to leadership.*

18. Per-experiment pass/fail against the 3.8 / 5.0 (76%) threshold
19. Recommendation on which approach scales into which gap type, with a phased roadmap
20. Leadership go/no-go
