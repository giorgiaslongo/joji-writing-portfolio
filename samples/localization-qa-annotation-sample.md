# Localization QA Annotation Sample: Projeto Verbly (EN → PT-BR)

**Doc ID:** DOC-2026-05A  
**Status:** V1.0  
**Target Audience:** Localization QA reviewers / hiring managers  
**Scope:** UI strings — onboarding, labels, error states, button text  
**Language pair:** English (EN-US) source → Brazilian Portuguese (PT-BR) review  
**A11y Status:** Plain language; no jargon  
**Changelog:**

| Version | Date | Change |
|---|---|---|
| V1.0 | May 2026 | Initial localization QA annotation sample |

---

## About This Sample

This document shows a localization QA review of a set of Projeto Verbly UI strings that were submitted for PT-BR translation. Each string was reviewed against the source, flagged for error type, and corrected with an annotation explaining the issue and the fix rationale.

Projeto Verbly is a fictional bilingual educational app used as a constructed example. For context on voice, register, and localization rules that govern this content, see:
- [Global Content Style Guide (Excerpt)](global-content-style-guide-excerpt.md) — localization rules at Section 2
- [Bilingual Release Notes v2.4](bilingual-release-notes-project-acorn-v2-4.md) — applied bilingual output

The strings reviewed here represent the kind of content a localization QA reviewer typically receives: short labels, onboarding messages, button text, and error states. Across the five, the error types are: a false friend that makes a welcome message read as negative (*rolo*), a register mismatch in a settings label (*Controles Parentais*), a truncation that cuts an error message mid-sentence, an unlocalized date format, and a pronoun ambiguity introduced by a third-person shift mid-onboarding flow.

The review format is: **EN source → submitted PT-BR → QA annotation → corrected PT-BR.**

---

## String Review: Annotated

---

### String 01 — Onboarding welcome message

**Context:** First-launch screen, displayed to the parent or educator setting up a child's profile. Below the app logo, above a "Get started" button.

| Field | Content |
|---|---|
| EN source | `You're on a roll! Let's set up your child's first lesson.` |
| Submitted PT-BR | `Você está em um rolo! Vamos configurar a primeira aula do seu filho.` |

**QA annotation — Error type: Literal idiom translation**

> `"Você está em um rolo!"` is a word-for-word rendering of "You're on a roll!" The idiom does not carry over. In PT-BR, *rolo* refers to a physical roll (of paper, fabric, dough) or colloquially to a problem or messy situation — making this read as either meaningless or negative. A first-launch welcome screen with a phrase that could be interpreted as "you're in trouble" is a trust risk.
>
> The communicative intent is encouragement: the user has started something and should feel momentum. The PT-BR equivalent that fits the register of this screen is *"Ótimo começo!"* (Great start!) or *"Vamos lá!"* (Let's go!). The second clause is accurate and can stay.

| Field | Content |
|---|---|
| Corrected PT-BR | `Ótimo começo! Vamos configurar a primeira aula do seu filho.` |

---

### String 02 — Settings label

**Context:** Settings screen, section header for parental controls. Used in a list alongside "Notifications," "Language," and "Account."

| Field | Content |
|---|---|
| EN source | `Parental Controls` |
| Submitted PT-BR | `Controles Parentais` |

**QA annotation — Error type: Unnatural term / false cognate pressure**

> *Controles Parentais* is structurally correct and will be understood, but it reads as a direct import of the EN label rather than natural PT-BR UI copy. The standard term used in Brazilian Portuguese OS and app interfaces — across Android, iOS, and major local apps — is *Controle dos Pais* or *Restrições para Crianças*, depending on the platform's scope.
>
> *Parentais* exists in formal PT-BR (e.g., licença parental, responsabilidade parental) but is uncommon in everyday product copy. A parent navigating app settings would not expect this register here. Using the established UI convention reduces friction and builds trust that the app was localized by someone who knows the market.
>
> *Controle dos Pais* is the recommended form. It matches the phrasing in Google Family Link, Apple Screen Time (PT-BR), and comparable educational apps available in Brazil.

| Field | Content |
|---|---|
| Corrected PT-BR | `Controle dos Pais` |

---

### String 03 — Error state message

**Context:** Inline error displayed when a sync fails during a lesson activity. Appears below the progress bar. Character limit on this component is 60 characters.

| Field | Content |
|---|---|
| EN source | `Your progress didn't save. We'll try again automatically.` |
| Submitted PT-BR | `O seu progresso não foi gravado. Nós vamos tentar novamente de forma automática.` |

**QA annotation — Error type: UI length / truncation risk + register inconsistency**

> Two issues, both blocking.
>
> **1. Length:** The submitted string is 80 characters. The component limit is 60. At 80 characters, this string will truncate in-app, cutting off at approximately *"Nós vamos tentar novamente de"* — which leaves the user mid-sentence with no resolution. The EN source is 57 characters and fits within the limit. The PT-BR translation must be brought under 60.
>
> **2. Register:** *"Nós vamos tentar novamente de forma automática"* is verbose and formal for an inline error state. The style guide (Section 2.4) specifies neutral *você* register for error messages, with concise phrasing. *"De forma automática"* is the kind of phrase that would appear in a technical manual, not a child-facing educational app. *"Automaticamente"* conveys the same meaning in one word.
>
> The corrected version brings the string to 59 characters and uses the appropriate register.

**Character count check:**

| String | Characters |
|---|---|
| EN source | 57 ✅ |
| Submitted PT-BR | 80 ❌ (limit: 60) |
| Corrected PT-BR | 59 ✅ |

| Field | Content |
|---|---|
| Corrected PT-BR | `Seu progresso não foi salvo. Vamos tentar novamente.` |

> **Additional note:** *Gravado* (recorded) was used where *salvo* (saved) is the correct term for app data. *Gravar* is used for audio/video recording in PT-BR product copy; *salvar* is the standard for saving files, progress, or settings. This is a secondary error — a false application of a cognate-adjacent term.

---

### String 04 — Date display in activity history

**Context:** Activity history screen, timestamp label below each completed lesson entry. Displayed as a short inline label next to the lesson title.

| Field | Content |
|---|---|
| EN source | `Completed: 05/14/2026` |
| Submitted PT-BR | `Concluído: 05/14/2026` |

**QA annotation — Error type: Date format not localized**

> A locale format validator would flag this — but a human reviewer catches something the validator does not: a Brazilian user reading *05/14/2026* is likely to follow the local DD/MM/YYYY convention and try to parse *14* as the day, which is an invalid date. That misread produces confusion, not just recognition of an unlocalized string.
>
> The date 05/14/2026 in EN-US is May 14, 2026. In PT-BR format, this is 14/05/2026. Per the Projeto Verbly Style Guide (Section 2.2): *"Use DD/MM/YYYY format in PT-BR."* No other change is needed — the label *Concluído* is correct and the year format is fine.

| Field | Content |
|---|---|
| Corrected PT-BR | `Concluído: 14/05/2026` |

---

### String 05 — Onboarding step instruction

**Context:** Step 2 of 4 in the parent onboarding flow. Instruction text displayed above two profile-photo option buttons: "Take a photo" and "Choose from library."

| Field | Content |
|---|---|
| EN source | `Add a photo so your child recognizes their profile.` |
| Submitted PT-BR | `Adicione uma foto para que a criança reconheça seu perfil.` |

**QA annotation — Error type: Register inconsistency / pronoun ambiguity**

> Two issues in one string.
>
> **1. Register shift:** The EN source uses *your child* — direct address to the parent in second person. The submitted PT-BR switches to third person: *a criança* (the child). This is a register inconsistency: the rest of the onboarding flow addresses the parent directly with *você* and *seu/sua*, and this string breaks that pattern mid-flow. A reviewer reading only this string might not catch it, but in sequence it reads as a voice shift — as if a different writer or a different document took over.
>
> **2. Pronoun ambiguity:** *Seu perfil* in the corrected context should refer to the child's profile. But because *seu* in PT-BR can refer to either the subject of the sentence or to *você* (the parent), the submitted version creates a genuine ambiguity: whose profile — the parent's or the child's? The EN source resolves this with *their profile* (referring unambiguously to the child). The PT-BR must do the same.
>
> The corrected version restores direct address to the parent and disambiguates the possessive.

| Field | Content |
|---|---|
| Corrected PT-BR | `Adicione uma foto para que seu filho reconheça o próprio perfil.` |

> **Rationale for *o próprio perfil*:** *O próprio* (literally "their own") is the natural PT-BR way to make clear the child is recognizing their own profile — not the parent's, and not a generic profile. It is a common construction in product copy where reflexive clarity is needed without grammatical awkwardness.

---

## Error Type Summary

| # | String | Error type | QA risk if unresolved |
|---|---|---|---|
| 01 | Onboarding welcome | Literal idiom translation | Meaningless or negative reading on first launch; trust risk |
| 02 | Settings label | Unnatural term | Register mismatch; product feels untranslated to local users |
| 03 | Error state | UI truncation + register inconsistency | String cut off in-app; incomplete error message shown to user |
| 04 | Activity history date | Date format not localized | Date misread or flagged as unlocalized; style guide violation |
| 05 | Onboarding instruction | Register shift + pronoun ambiguity | Voice inconsistency mid-flow; ambiguous possessive |

---

## Skills Demonstrated

- Identifying localization errors that differ in type and severity — not just "translation is wrong"
- Anchoring every annotation to specific text, explaining why the error matters in context
- Applying PT-BR register and terminology conventions correctly (UI copy vs. formal vs. error state)
- Running a character-count check against a component limit and catching truncation before it reaches production
- Recognizing ambiguity introduced by translation even when the source sentence is unambiguous
- Cross-referencing style guide rules (Section 2.2, 2.4) and citing them in review notes
- Correcting without over-correcting — each fix changes only what needs to change
