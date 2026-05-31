# Cognitive Accessibility & Microcopy Audit: AutiSpark Application

**Doc ID:** DOC-2026-01A  
**Status:** V1.2  
**Target Audience:** Product Team, UX Writers, ESL Educators  
**Reading Level Target:** Flesch-Kincaid Grade 9 (professional report)  
**A11y Status:** WCAG-informed recommendations; screen-reader compatible formatting  
**Changelog:**

| Version | Date | Change |
|---|---|---|
| V1.0 | November 2025 | Initial draft from thesis research |
| V1.1 | May 2026 | Added microcopy before/after section |
| V1.2 | May 2026 | Formatting and skills section |

---

## Overview

This audit evaluates the AutiSpark mobile application's instructional language, interface microcopy, and cognitive accessibility for English as a Second Language (ESL) learners with Autism Spectrum Disorder (ASD).

**Application:** AutiSpark v6.8 (IDZ Digital Private Limited, 2025)  
**Audit basis:** Undergraduate thesis research conducted at UNESPAR, Campus União da Vitória, 2025. Advisor: Prof.ª Valéria Vaz Boni, Ph.D.  
**Methodology:** Single qualitative case study. One month of spontaneous application use in a domestic environment. Data collected via semi-structured questionnaire (10 questions) and researcher field diary. Analyzed using semi-inductive thematic content analysis (Bardin, 2016).  
**User profile:** 10-year-old participant, female, diagnosed with ASD Level 1, native Portuguese speaker, prior English knowledge acquired through digital media, hyperfocus interest in animals.

> **Scope note:** This is a single-participant qualitative case study. Findings are not statistically generalizable. They reflect the documented experience of one user and are intended to surface concrete usability and content gaps for product improvement.

---

## Key Findings

**1. Frictionless usability.** The participant rated the application "Easy to use" and navigated all activities autonomously. She highlighted colors and animations as the most engaging elements. The interface's visual architecture reduced cognitive barriers and functioned as effective Assistive Technology (Bersch, 2017), consistent with visual thinking patterns common in ASD (Grandin, 1995).

**2. Reinforcement, not acquisition.** The application did not introduce new vocabulary for this participant. When asked what she learned, she selected "Other" and wrote "EVERYTHING" — but when asked directly "Did you learn anything new?", she answered "No." She explained: *"I already knew all the words."* The app functioned as a confidence-building reinforcement tool rather than a learning scaffold. This aligns with Harris et al. (2015), who caution that task repetition without difficulty progression can prevent deeper, generalized learning.

**3. Sociopragmatic impact over semantic acquisition.** The most significant engagement came from social scenario videos — not vocabulary games. The participant specifically highlighted *"the videos that teach you what to do when a visitor comes"* as the most valuable content. For a child who reported she *"never knows what to do"* in social situations, the app functioned as a safe, predictable environment for modeling social interaction. This suggests AutiSpark's greatest value may lie in pragmatic language development rather than vocabulary.

**4. Monetization as an accessibility barrier.** The participant explored the full free content in under 20 minutes: *"The free game should be more complete — I explored everything in less than 20 minutes."* The subscription model limits access for families who most need sustained use.

---

## Microcopy Before and After

The following issues were identified through direct observation of the interface during the research period. Each entry documents a specific friction point and a targeted revision.

---

### M-01: Activity Selection Screen — No Age or Level Filter

**QA finding — Issue type: Missing content hierarchy / navigation friction**

The parental control setup screen groups all activities in a single undifferentiated list — no age range, proficiency level, or content-type grouping applied. Parents cannot curate content for their child without previewing every activity individually.

**Current state**

Global on/off toggles only. Vocabulary matching games for early learners sit in the same list as social scenario videos that require higher reading ability and social comprehension.

**Observed impact:** The participant (age 10, intermediate English) found most activities too simple. She recommended the app for children *"up to 8 years old, especially those just starting to read."* The social videos — the content most appropriate for her level — were not visually distinguished or prioritized.

**Recommended revision**

The parental setup screen currently has no grouping or labeling. Add three activity groups with names and one-line descriptors:

- **Starter · Ages 4–6 · Beginner English** — "Matching and sorting activities using animals, colors, and numbers."
- **Explorer · Ages 7–9 · Elementary English** — "Vocabulary games with simple sentences and picture recognition."
- **Social Skills Videos · All levels** — "Animated scenarios modeling everyday social interactions."

This allows parents to make informed selections without previewing every activity individually. The Social Skills group in particular needs to be visible at the top level — it is the highest-value content for older users but currently requires manual discovery.

**A11y note:** Group labels must meet WCAG AA contrast (4.5:1 minimum). Use icons alongside text labels to support non-reading caregivers.

---

### M-02: Task Instructions — Audio-Only Delivery With No Text Fallback

**QA finding — Issue type: Accessibility gap — no fallback modality**

**Current state**

Task instructions are delivered by an in-app voice, spoken once, with no closed captions or text equivalent displayed on screen.

**Problem**

When the audio plays once and disappears, there is nothing to fall back on. A learner who prefers lower volume — or needs more time to process spoken directions — has no way to replay or read the instruction.

**Observed impact:** The participant preferred low volume during play. Without a text fallback, audio-only instructions created time pressure to process spoken directions in real time — cognitively demanding for learners who benefit from visual processing. Many autistic learners prefer visual information over auditory input as a self-regulation strategy (Grandin, 1995).

**Recommended microcopy revision — example activity:**

| Before (audio only) | After (audio + subtitle) |
|---|---|
| *\[Voice\]: "Find the animal that lives in water."* | *\[Voice\]: "Find the animal that lives in water."* |
| *(no text displayed)* | **On-screen text:** "Find the animal that lives in water." |

**Implementation note:** Subtitles should be toggleable in parental settings and persist as a session preference. Default to ON for first-time users.

**Secondary benefit:** Connecting spoken audio to written text supports phonics development for learners in early literacy stages — a benefit that extends beyond the ASD user base.

---

### M-03: Task Completion Screen — No Closure or Progress Signal

**QA finding — Issue type: Missing closure signal / state feedback**

**Observed impact:** The participant reported sensory overload from the volume of options on the activity screen — she exhausted the free content in under 20 minutes partly because there was no signal telling her what she had already done.

**Current state**

After completing an activity, the interface returns directly to the activity selection grid. No completion message, checkmark, or progress indicator is displayed. The selection screen looks identical before and after a task is completed.

**Problem**

Without a visible completion signal, learners have no clear indication that their effort was registered. The activity grid continues to display the full set of options with no visual differentiation between completed and available tasks. This is exactly the condition the participant described: she moved through all free content in under 20 minutes, with nothing telling her she had already been there.

**Recommended microcopy revision:**

*After task completion, before returning to the activity grid:*

| Before (current state) | After (recommended) |
|---|---|
| *(direct return to activity grid, no message)* | Brief full-screen message: **"Great job! 🌟 Play again, or choose a new activity."** |
| *(activity grid: all tiles look the same)* | Completed activity tiles show a checkmark badge and slightly dimmed state. |

**Copy guidelines for the completion message:**
- Use a concrete, specific verb: "Great job" over "Well done" (more literal, easier to process)
- Offer exactly two choices: repeat or continue (not three or more)
- Keep the message under 8 words
- The emoji is intentional: visual reward reinforces the Affordance signal (van Lier, 2004)

---

## Product & Strategy Recommendations

**Adaptive difficulty.** Introduce difficulty tiers that adjust as the user progresses. The current fixed-difficulty model is appropriate for beginners but creates an engagement ceiling for learners with prior knowledge. Difficulty tiers extend the product's useful lifespan per user.

**Sociopragmatic content track.** Social scenario videos generated the highest engagement for this participant. Creating a dedicated "Social Skills" track — surfaced prominently for the 7–10 age group — would align the product's positioning with its demonstrated strength.

**Monetization flexibility.** The free tier was exhausted in under 20 minutes. A lifetime purchase option (in addition to the subscription) would reduce the barrier for families who cannot commit to recurring costs. This is particularly relevant in LATAM markets where subscription fatigue is high and purchasing power varies.

---

## Audit Notes

For neurodivergent learners, the most valuable function of an educational app may not be the one printed on the marketing page. AutiSpark is marketed as a vocabulary and learning tool — but for this participant, its most meaningful use was as a safe space to practice social behavior. The instruction *"find the animal that lives in water"* was easy. The model of *"what to do when a visitor comes"* was genuinely useful.

This distinction — between semantic content (what words mean) and pragmatic content (how language functions in social context) — is one that product teams and UX writers often overlook when designing for neurodiverse users. It should inform how the app is described, how its content is organized, and which features are prioritized for development.

---

## Skills Demonstrated

- Translating academic research findings into actionable product and copy recommendations
- Identifying microcopy friction by type (missing fallback, unclear affordance, absent closure signal)
- Writing before/after copy revisions with rationale grounded in user behavior
- Applying accessibility considerations (WCAG, cognitive load, sensory sensitivity) to content review
- Honest framing of research limitations (single case study scope)
- Structuring a technical audit document for a product-team audience
