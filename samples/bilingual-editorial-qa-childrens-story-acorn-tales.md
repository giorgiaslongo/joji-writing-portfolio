# Acorn Tales: The Smallest Seed
### Bilingual Editorial QA — Children's Narrative Content (EN / PT-BR)

**Doc ID:** DOC-2026-07A  
**Status:** V1.0  
**Target Audience:** Hiring managers / content QA reviewers / localization reviewers  
**Scope:** Bilingual editorial QA — narrative content, ages 6–8 (EN and PT-BR)  
**Changelog:**

| Version | Date | Change |
|---|---|---|
| V1.0 | May 2026 | Initial bilingual editorial QA sample — children's narrative |

---

## About This Sample

This document applies editorial QA to narrative content — a short children's story excerpt from the Project Acorn universe, target age 6–8. The five problems in Version 1 reflect the kind of issues that appear in educational content produced without QA review: vocabulary above grade level, passive constructions that slow young readers, a run-on sentence, a register shift that breaks the narrator's voice mid-excerpt, and a culturally specific school practice that would not survive localization into Brazilian Portuguese. Each problem is annotated with a decision and explanation before the edited version. The PT-BR localization that follows is not a translation of Version 2 — it is an adaptation that applies Brazilian children's narrative conventions.

---

## Version 1 — Original (Problematic EN)

*Acorn Tales: The Smallest Seed*

Leo's grandmother gave him an acorn on a Saturday morning. It was peculiar-looking — small and brown, with a tiny cap on top like a miniature hat.

"What does it do?" Leo asked.

"If you take good care of it," she said, "it will become a big oak tree someday."

Leo contemplated this. He was reluctant to believe that something so small could become something so enormous. He picked it up and turned it over in his hand, and he thought about what Grandma had said and wondered if it was really true that something this small could grow into a tree that birds would nest in.

The child's curiosity, while understandable, was not easily satisfied.

That afternoon, Leo decided he would bring the acorn to school for show and tell. The acorn was placed carefully in his jacket pocket so it would not get lost.

On Monday, he stood in front of his class. "This acorn," he said proudly, "will become a mighty oak someday."

His classmates were duly impressed.

---

## QA Annotations — Version 1 → Version 2

---

### A-01 — Vocabulary above target reading level

**Decision:** Replace all four flagged terms.  
**Quoted:** *"peculiar-looking," "contemplated," "reluctant," "mighty"*

A Grade 1–2 reader (ages 6–8) is unlikely to know any of these words, and the surrounding context does not support meaning inference for them. "Peculiar" and "contemplated" are the most significant flags — they belong in Grade 4+ text. "Contemplated" in particular does no work here that "looked at" cannot do better, and with less friction. "Mighty" stays in some children's content because it appears in read-aloud contexts where an adult can gloss it; here it reads as the narrator's word, not Leo's, so it goes. "Duly" in the final sentence also registers above level, but that sentence is being cut for other reasons (see A-04).

---

### A-02 — Passive construction

**Decision:** Rewrite to active.  
**Quoted:** *"The acorn was placed carefully in his jacket pocket so it would not get lost"*

Passive voice delays the actor and breaks narrative momentum — a documented readability drag for young readers. The opening sentence ("Leo's grandmother gave him an acorn") has the reverse structure but reads naturally because the actor follows immediately. This sentence does not recover the same way: Leo disappears entirely. One passive in a 180-word excerpt is defensible; two is a pattern. Rewrite: Leo tucked it into his jacket pocket.

---

### A-03 — Run-on sentence

**Decision:** Break into three sentences.  
**Quoted:** *"He picked it up and turned it over in his hand, and he thought about what Grandma had said and wondered if it was really true that something this small could grow into a tree that birds would nest in."*

Forty-four words and three distinct thoughts. A Grade 1 reader's working memory does not hold all of this in a single unit. The ideas are good — they just need space to land. Breaking the sentence also lets the questions ("Could it really become a tree? A tree where birds would live?") read as Leo's actual wonder, not as an exhausted clause at the end of a long structure.

---

### A-04 — Register shift

**Decision:** Cut the sentence entirely.  
**Quoted:** *"The child's curiosity, while understandable, was not easily satisfied."*

Every other sentence in this excerpt is written close to Leo — warm, direct, inside his point of view. This sentence steps outside to a narrator who observes Leo from a distance and finds his curiosity worth characterizing with a mild qualification ("while understandable"). It reads like a sentence from a different draft, or a different genre. The surrounding text already conveys Leo's persistence without an outside observer commenting on it. Cut it; nothing is lost.

---

### A-05 — Culturally specific reference — localization risk

**Decision:** Remove "show and tell." Replace with a neutral action.  
**Quoted:** *"Leo decided he would bring the acorn to school for show and tell"*

"Show and tell" is a North American classroom convention — a scheduled activity where children bring objects from home to present formally to the class. It does not exist as a recognized school practice in Brazil, and there is no standard PT-BR equivalent. A translator working quickly might carry the phrase through as-is, or reach for an approximation that a Brazilian child would not recognize. This is the kind of reference that passes editorial review in a monolingual EN pipeline and fails at localization — not flagged by spell-check, not obviously idiomatic, but culturally specific enough to break the text for a different audience. Replace with a simple, neutral action: Leo wanted to show the acorn to his class.

---

## Version 2 — Edited EN

*Acorn Tales: The Smallest Seed*

Leo's grandmother gave him an acorn on a Saturday morning. It was small and brown, with a tiny cap on top — like a little hat.

"What does it do?" Leo asked.

"If you take good care of it," she said, "it will grow into a big oak tree one day."

Leo looked at the acorn. He couldn't believe something so small could grow into something so big. He turned it over in his hand. Could it really become a tree? A tree where birds would live?

That afternoon, Leo wanted to show his acorn to his class. He tucked it into his jacket pocket so it wouldn't get lost.

On Monday, he stood in front of his class and held up the acorn.

"This little thing," he said, "will grow into a big tree one day."

His classmates leaned in to look.

---

## Localization Notes — EN → PT-BR

| # | EN element | Type | Decision | Rationale |
|---|---|---|---|---|
| 1 | "show and tell" (removed in V2) | Cultural adaptation | Replaced with neutral action in V2; rendered in V3 as *"mostrar a bolota para os amigos da turma"* | "Show and tell" has no equivalent practice in Brazilian schools. The V2 edit neutralized the cultural reference; the PT-BR version reshapes the phrasing slightly to fit the natural rhythm of how a Brazilian child would describe sharing something with classmates. |
| 2 | Narrator warmth / close register | Register | Applied diminutive suffix throughout: *"pequenininha," "chapeuzinho," "coisinha"* | In Brazilian children's narrative, the diminutive suffix (-inho/-inha) signals affection and closeness — not just small size. Omitting diminutives in PT-BR children's text reads as cold or adult-formal. "Little hat" becomes *"chapeuzinho"*, not *"chapéu pequeno"* (which is grammatically correct but tonally flat). |
| 3 | "acorn" | Vocabulary — PT-BR specific | *"bolota"* | Standard PT-BR children's book term for acorn. *"Glande"* is technically accurate but carries anatomical meaning in common usage and does not appear in children's content. *"Bolota"* is what Brazilian children's books use. |
| 4 | Oak tree (*"carvalho"*) | Cultural note — kept with caveat | *"carvalho"* retained | Oak trees are not native to Brazil. In a real production context, the creative team would need to decide whether to substitute a familiar Brazilian tree (e.g., *ipê*, *jatobá*). For this sample, *carvalho* is retained for brand consistency with Project Acorn — but the decision would need to be escalated, not made silently by the localizer. |

---

## Version 3 — PT-BR Localization

*Acorn Tales: A Menor Semente*

A vovó de Leo deu para ele uma bolota numa manhã de sábado. Era pequenininha e marrom, com um capinho redondo no topo — igualzinho a um chapeuzinho.

— O que ela faz? — Leo perguntou.

— Se você cuidar bem dela — disse a vovó —, ela vai virar um carvalho enorme um dia.

Leo olhou para a bolota. Não dava para acreditar que uma coisa tão pequenininha pudesse virar algo tão grande assim. Ele virou ela de um lado para o outro. Será que ela ia mesmo virar uma árvore? Uma árvore cheia de passarinhos?

Naquela tarde, Leo quis mostrar a bolota para os amigos da turma. Colocou ela com cuidado no bolso da jaqueta para não perder.

Na segunda-feira, Leo ficou de pé na frente da turma e ergueu a bolota bem alto.

— Essa coisinha aqui — ele disse — vai virar uma árvore enorme um dia.

Os colegas se aproximaram para ver de perto.

---

## Skills Demonstrated

**Plain language editorial QA applied to narrative content:** The five problems in Version 1 are the kind found in educational content that has not gone through QA review — not parody errors, not obvious typos. The annotations show the decision and the mechanism: why the problem exists, what it costs the reader, and what the smallest effective fix is.

**Age-level vocabulary judgment:** The before/after is visible at word level — "contemplated" → "looked at," "peculiar" → cut, "mighty" → cut. The test was whether a Grade 1–2 reader can access the word without context support, not whether the word is grammatically wrong.

**Localization risk identification in editorial review:** "Show and tell" passes EN spell-check, reads fluently, and causes no problem in a monolingual pipeline. It fails at PT-BR localization. Catching it at the editorial stage is the job; catching it only after the translator has approximated it is more expensive.

**PT-BR narrative localization:** Version 3 is not a translation of Version 2. The dialogue punctuation (em-dash, not quotation marks), the diminutive register throughout, and the sentence rhythm reflect how Brazilian children's narrative is actually written. The reasoning behind each non-literal choice is documented in the localization notes above.
