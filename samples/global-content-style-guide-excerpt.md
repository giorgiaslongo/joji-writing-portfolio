# Global Content Style Guide (Excerpt)

**Doc ID:** DOC-2026-03A  
**Status:** V1.0  
**Applies to:** Projeto Verbly — all user-facing content in EN and PT-BR  
**Target Audience:** Writers, translators, UX designers, product managers  
**Reading Level Target:** Internal reference document  
**A11y Status:** Plain language; structured for screen-reader navigation  
**Changelog:**

| Version | Date | Change |
|---|---|---|
| V1.0 | May 2026 | Initial excerpt covering Voice & Tone, Localization Rules, and Accessibility Baseline |

---

## About This Document

This excerpt covers three core sections of the Projeto Verbly Content Style Guide: Voice & Tone, Localization Rules, and Accessibility Baseline. It is intended as a practical reference for anyone who writes, reviews, translates, or edits content for the application.

Projeto Verbly is a fictional bilingual educational app used as a constructed example for portfolio purposes.

For a demonstration of how this guide is applied in practice, see:
- [Bilingual Release Notes v2.4](bilingual-release-notes-projeto-verbly-v2-4.md) — applies Sections 1, 2, and 3
- [Cognitive Accessibility & Microcopy Audit: AutiSpark](cognitive-accessibility-microcopy-audit-autispark.md) — applies Section 3 (Accessibility Baseline)

---

## Section 1: Voice and Tone

### 1.1 Core Voice

Projeto Verbly speaks with one consistent voice across all languages and surfaces: **encouraging, clear, and never condescending.**

The application's primary users are children (ages 4–10) with diverse cognitive profiles, including neurodivergent learners. Secondary users — parents and educators — interact with settings, release notes, and documentation.

All content must work for both audiences. Write for the child's comprehension; structure for the adult's navigation.

### 1.2 Tone Attributes

| Attribute | What it means | Example |
|---|---|---|
| **Encouraging** | Positive framing; effort acknowledged before correction | "Great try! The answer is 'cat'." not "Incorrect. Try again." |
| **Clear** | One idea per sentence; concrete nouns and verbs; no metaphors | "Find the animal that lives in water." not "Navigate to the aquatic category." |
| **Direct** | Tell users what to do, not what not to do | "Tap the matching card." not "Don't select the wrong card." |
| **Never condescending** | No baby talk for children; no patronizing explanations for adults | "You did it!" not "Good job, little learner!" |
| **Predictable** | Consistent phrasing for recurring interactions | Always "Tap to continue" — never alternating with "Press next" or "Keep going" |

### 1.3 Voice in Error States

Error messages must follow this structure:
1. Acknowledge what happened (without blame)
2. State what to do next
3. Keep it under 15 words

**Example — Connection error:**

| ❌ Do not write | ✅ Write instead |
|---|---|
| "Error 503: Server unavailable. Check your connection." | "Can't connect right now. Check your internet and try again." |
| "Something went wrong." | "Your progress didn't save. We'll try again automatically." |

### 1.4 Writing for Neurodivergent Users

When writing for screens or interactions that will be used by children with ASD or other cognitive differences, apply the following additional rules (see also Section 3):

- Use **concrete, literal language.** Idioms and figurative language create comprehension barriers.
- Give **one instruction at a time.** Do not combine two actions in one sentence.
- **Name the next step explicitly.** "Tap the green button to start" is preferable to "When you're ready, begin."
- **Avoid open-ended prompts** ("Explore!" or "What will you discover?") in task contexts. Use them only in freeplay modes.

---

## Section 2: Localization Rules

### 2.1 General Principles

All content must be localized — not just translated. Localization means adapting content so that it reads naturally and functions correctly for a target audience, not just converting words from one language to another.

**Key distinction:**

| Translation | Localization |
|---|---|
| Word-for-word conversion | Meaning-for-meaning adaptation |
| May produce literal, unnatural results | Reads as native to the target language |
| Ignores cultural context | Respects cultural expectations |

### 2.2 Always Localize

The following elements must always be adapted for the target locale, not translated literally:

- **Dates and times:** Use DD/MM/YYYY format in PT-BR. Use MM/DD/YYYY in EN-US.
- **Measurements:** Use metric units in PT-BR (cm, kg, km). Do not convert values that appear in educational content — adapt the example instead.
- **Currency:** Adapt examples to local context. If a math activity uses "5 dollars," the PT-BR version should use "5 reais."
- **Greetings and social scripts:** Localize for cultural expectations. "Hi there!" does not translate naturally as *"Oi lá!"* — use *"Oi!"* or *"Olá!"* depending on register.
- **Reading direction:** EN and PT-BR are both left-to-right; no directional adaptation is needed between these locales. For future RTL locales (Arabic, Hebrew, Farsi), flag this section for full review: UI layout, icon direction, list ordering, and punctuation placement all require locale-specific rules that are outside the scope of this excerpt.

### 2.3 Never Localize

The following elements must remain in their original form:

- Application name: **Projeto Verbly** (do not translate)
- Platform names: **iOS**, **Android**, **Google Play**, **App Store**
- OS version names: **Oreo**, **Nougat**, etc.
- Email addresses and URLs
- Code strings, developer terms, or technical identifiers appearing in documentation

### 2.4 Register Consistency

PT-BR content must maintain a consistent register throughout a single document. Do not mix formal and informal address forms.

| Context | Recommended register | Example |
|---|---|---|
| UI copy (buttons, labels) | Informal (*você*) | "Toque para continuar" |
| Error messages | Neutral (*você*) | "Sua conexão foi perdida. Tente novamente." |
| Release notes | Neutral (*você*) | "Sua conta está mais segura." |
| Legal or consent text | Formal (*você* with full verb forms) | "Ao continuar, você concorda com os termos." |

### 2.5 Idioms and Cultural Adaptation

Do not translate idioms literally. Identify the communicative intent and find a culturally equivalent expression.

**Example:**

| EN source | Literal PT-BR (incorrect) | Localized PT-BR (correct) |
|---|---|---|
| "You're on a roll!" | *"Você está em um rolo!"* ❌ | *"Continue assim!"* ✅ |
| "Let's dive in." | *"Vamos mergulhar."* ❌ | *"Vamos começar."* ✅ |
| "Good job, you nailed it!" | *"Bom trabalho, você pregou!"* ❌ | *"Muito bem, arrasou!"* ✅ |

Add a footnote or margin note when a significant cultural adaptation is made, explaining the reasoning. See [Bilingual Release Notes v2.4](bilingual-release-notes-projeto-verbly-v2-4.md) for examples of documented localization decisions.

---

## Section 3: Accessibility Baseline

All user-facing content in Projeto Verbly must meet the following accessibility standards.

### 3.1 Reading Level

- **In-app instructions and task prompts:** Maximum Flesch-Kincaid Grade 6 (EN) or equivalent in PT-BR.
- **Settings and documentation:** Maximum Grade 9.
- **Legal or consent text:** No reading level requirement, but plain language principles apply. Avoid legal jargon in summaries.

**To check reading level:** Use a readability tool (Hemingway Editor for EN; Legibilidade.com or similar for PT-BR). Document the score in the document's front matter.

### 3.2 WCAG Compliance

All text displayed on screen must meet WCAG AA standards as a minimum:

| Requirement | Standard |
|---|---|
| Text contrast (normal text) | 4.5:1 minimum |
| Text contrast (large text, 18pt+) | 3:1 minimum |
| Interactive element contrast | 3:1 against adjacent colors |
| Focus indicators | Visible; minimum 3:1 contrast |

Content writers are responsible for flagging copy that may conflict with contrast requirements — for example, light gray placeholder text on a white background, or colored text used on a gradient. When flagging, add an inline note at the point of concern:

> `[A11y flag: confirm contrast for this text before publishing]`

This keeps the issue visible in review without blocking the writing process. Design resolves it; the writer's job is to catch it.

### 3.3 Cognitive Accessibility

For all content used in the learning interface (not settings or documentation):

1. **One instruction per screen.** Do not present two tasks simultaneously.
2. **Use concrete verbs.** "Tap," "drag," "match" — not "interact," "engage," "explore" in task contexts.
3. **Provide closure.** Every task must have a visible end state. Do not return the user to a neutral screen without a completion signal. *(See DOC-2026-01A, M-03 for a documented case of this failure in an audited product.)*
4. **Avoid time pressure.** Do not auto-advance screens or activities without user input.
5. **Subtitles on by default** for video content in accessibility-enabled profiles.

### 3.4 Language Accessibility

- Avoid idioms, metaphors, and figurative language in task instructions (see Section 2.5).
- Use the active voice in instructions: "Find the animal" not "The animal should be found."
- When writing bilingual content, confirm that both versions are functionally equivalent — not just linguistically accurate.

---

## Quick Reference Card

**Before publishing any user-facing content, confirm:**

- [ ] Voice is encouraging, clear, and direct
- [ ] No idioms or figurative language in task copy
- [ ] PT-BR uses the correct register throughout (no mixing)
- [ ] Date, currency, and measurement formats are localized
- [ ] Reading level confirmed (Grade 6 for in-app; Grade 9 for docs)
- [ ] WCAG AA contrast met for all on-screen text
- [ ] Every task has a visible completion signal
- [ ] Product names and OS identifiers are not translated

---

## Skills Demonstrated

- Creating a practical, reusable content governance document
- Defining voice, tone, and register rules with examples
- Establishing bilingual localization rules (EN ↔ PT-BR) with specific guidance
- Applying WCAG and cognitive accessibility standards to written content guidelines
- Cross-referencing portfolio artifacts to demonstrate integrated documentation systems
