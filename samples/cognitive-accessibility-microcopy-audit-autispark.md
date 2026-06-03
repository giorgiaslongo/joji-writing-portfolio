# Cognitive Accessibility & Microcopy Audit: AutiSpark Application

**Doc ID:** DOC-2026-01A  
**Status:** V1.3  
**Target Audience:** UX Writers, Content Reviewers, Accessibility Reviewers  
**Reading Level Target:** Flesch-Kincaid Grade 9 (professional report)  
**A11y Status:** WCAG-informed recommendations; screen-reader compatible formatting  
**Changelog:**

| Version | Date | Change |
|---|---|---|
| V1.0 | November 2025 | Initial draft from thesis research |
| V1.1 | May 2026 | Added microcopy before/after section |
| V1.2 | May 2026 | Formatting and skills section |
| V1.3 | June 2026 | Revised to QA scope: removed product strategy sections, refined Key Findings, added Audit Scope & Limitations close |

---

## Overview

This audit evaluates the AutiSpark mobile application's instructional language, interface microcopy, and cognitive accessibility for English as a Second Language (ESL) learners with Autism Spectrum Disorder (ASD).

**Application:** AutiSpark v6.0 — iPhone (iOS) (IDZ Digital Private Limited, 2025)  
**Audit basis:** Undergraduate thesis research conducted at UNESPAR, Campus União da Vitória, 2025. Advisor: Prof.ª Valéria Vaz Boni, Ph.D.  
**Methodology:** Single qualitative case study. One month of spontaneous application use in a domestic environment. Data collected via semi-structured questionnaire (10 questions) and researcher field diary. Analyzed using semi-inductive thematic content analysis (Bardin, 2016).  
**User profile:** 10-year-old participant, female, diagnosed with ASD Level 1, native Portuguese speaker, prior English knowledge acquired through digital media.

> **Scope note:** This is a single-participant qualitative case study. Findings are not statistically generalizable. They reflect the documented experience of one user and are intended to surface concrete usability and content gaps for product improvement.

---

## Key Findings

**1. Frictionless usability.** The participant rated the application "Easy to use" and navigated all activities autonomously. She highlighted colors and animations as the most engaging elements. The interface's visual architecture reduced cognitive barriers and functioned as effective Assistive Technology (Bersch, 2017), consistent with visual thinking patterns common in ASD (Grandin, 1995).

**2. Reinforcement, not acquisition.** The application did not introduce new vocabulary for this participant. Her questionnaire responses indicated that she already knew the target words, so the app functioned more as a confidence-building reinforcement tool than as a learning scaffold. This aligns with Harris et al. (2015), who caution that task repetition without difficulty progression can prevent deeper, generalized learning.

**3. Sociopragmatic impact over semantic acquisition.** The most significant engagement came from social scenario videos, not vocabulary games. The participant identified everyday social-situation videos as the most valuable content. For a learner who benefits from explicit social scripts, the app functioned as a safe, predictable environment for modeling interaction.

**4. Content ceiling reached: available activities did not match participant's proficiency level.** The participant explored the full free content in under 20 minutes and reported that the free tier felt too limited. The participant described the application as more appropriate for younger beginners, consistent with Finding 2, in which the same participant had already acquired the target vocabulary through prior digital media exposure.

---

## Microcopy & UX Language Audit

The following issues were identified through direct observation of the interface during the research period. Each entry documents a specific friction point and a targeted revision.

---

### M-01: Activity Selection Screen (No Age or Level Filter)

**QA finding. Issue type: Missing content hierarchy / navigation friction**

The parental control setup screen groups all activities in a single undifferentiated list with no age range, proficiency level, or content-type grouping. Parents cannot curate content for their child without previewing every activity individually.

**Current state**

Global on/off toggles only. Vocabulary matching games for early learners sit in the same list as social scenario videos that require higher reading ability and social comprehension.

**Observed impact:** The participant (age 10, intermediate English) found most activities too simple and described the app as more appropriate for younger beginners. The social videos, the content most appropriate for her level, were not visually distinguished or prioritized.

**Recommended revision**

This is a structural recommendation — the issue is missing categorization, not incorrect copy.

The parental setup screen currently has no grouping or labeling. Add three activity groups with names and one-line descriptors:

- **Starter · Ages 4–6 · Beginner English**: "Matching and sorting activities using animals, colors, and numbers."
- **Explorer · Ages 7–9 · Elementary English**: "Vocabulary games with simple sentences and picture recognition."
- **Social Skills Videos · All levels**: "Animated scenarios modeling everyday social interactions."

This allows parents to make informed selections without previewing every activity individually. The Social Skills group in particular needs to be visible at the top level. It is the most relevant content for older and intermediate users but currently requires manual discovery.

**A11y note:** Group labels must meet WCAG AA contrast (4.5:1 minimum). Use icons alongside text labels to support non-reading caregivers.

---

### M-02: Task Instructions (Audio-Only Delivery, No Text Fallback)

**QA finding. Issue type: Accessibility gap, no fallback modality**

**Current state**

Task instructions are delivered by an in-app voice, spoken once, with no closed captions or text equivalent displayed on screen.

**Problem**

When the audio plays once and disappears, there is nothing to fall back on. A learner who prefers lower volume, or needs more time to process spoken directions, has no way to replay or read the instruction.

**Observed impact:** The participant preferred low volume during play. Without a text fallback, audio-only instructions created time pressure to process spoken directions in real time, which is more demanding for learners who rely on visual input. Many autistic learners prefer visual information over auditory input as a self-regulation strategy (Grandin, 1995).

**Recommended microcopy revision — example activity:**

| Before (audio only) | After (audio + subtitle) |
|---|---|
| *\[Voice\]: "Find the animal that lives in water."* | *\[Voice\]: "Find the animal that lives in water."* |
| *(no text displayed)* | **On-screen text:** "Find the animal that lives in water." |

**Implementation note:** Subtitles should be toggleable in parental settings and persist as a session preference. Default to ON for first-time users.

**Secondary benefit:** Connecting spoken audio to written text supports phonics development for learners in early literacy stages — a benefit that extends beyond the ASD user base.

---

### M-03: Task Completion Screen (No Closure or Progress Signal)

**QA finding. Issue type: Missing closure signal / state feedback**

**Observed impact:** The participant reported sensory overload from the volume of options on the activity screen. She exhausted the free content in under 20 minutes partly because there was no signal telling her what she had already done.

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

## Audit Scope & Limitations

### Scope

This audit covers **content, microcopy, and structural labeling gaps** observable in the application interface. It does not cover product roadmap decisions, monetization strategy, market positioning, or curriculum design.

| In scope | Out of scope |
|---|---|
| Microcopy text quality and clarity | Pricing model or subscription structure |
| Content hierarchy and labeling | Difficulty progression or curriculum design |
| Accessibility gaps (WCAG-informed) | Product strategy or feature roadmap |
| Structural UX friction (navigation, feedback signals) | Market positioning or competitor analysis |

### Findings Summary

| ID | Issue type | Severity | Status |
|---|---|---|---|
| M-01 | Missing content hierarchy / navigation friction | High | Open |
| M-02 | Accessibility gap, no fallback modality | High | Open |
| M-03 | Missing closure signal / state feedback | Medium | Open |

### Implementation Checklist

Items derived from the three QA findings above, ordered by implementation dependency:

- [ ] **[M-01]** Add three labeled activity groups to the parental setup screen: Starter (ages 4–6), Explorer (ages 7–9), Social Skills Videos (all levels).
- [ ] **[M-01]** Ensure group labels meet WCAG AA contrast (minimum 4.5:1). Pair icons with text labels.
- [ ] **[M-02]** Add on-screen text subtitles for all audio task instructions.
- [ ] **[M-02]** Add subtitle toggle to parental settings; default to ON for first-time users.
- [ ] **[M-03]** Insert a brief completion message after each activity ("Great job! 🌟 Play again, or choose a new activity.").
- [ ] **[M-03]** Add a checkmark badge and dimmed visual state to completed activity tiles in the selection grid.

### Methodology Note

All findings derive from a single-participant qualitative case study (one month of spontaneous use, semi-structured questionnaire, researcher field diary). The findings are sufficient to inform a content and UX revision pass and flag concrete usability gaps. They are not statistically generalizable and should be validated with a broader user sample before committing to structural or architectural changes.

---

## Skills Demonstrated

The audit moves from qualitative thesis findings to typed QA findings to specific microcopy revisions. Each M-section documents a different kind of failure: missing content hierarchy in Activity Selection, missing fallback modality in Task Instructions, missing closure signal in Task Completion. Three different problems, three different solutions, not variations on the same recommendation.

The research base is a single-participant case study. That scope is stated once in the overview and not revisited.
