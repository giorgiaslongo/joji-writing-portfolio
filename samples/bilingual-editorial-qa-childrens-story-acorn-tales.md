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

This document applies editorial QA to narrative content — a short children's story excerpt from the Projeto Verbly universe, target age 6–8. The five problems in Version 1 reflect the kind of issues that appear in educational content produced without QA review: vocabulary above grade level, passive constructions that slow young readers, a run-on sentence, a register shift that breaks the narrator's voice mid-excerpt, and a culturally specific school practice that would not survive localization into Brazilian Portuguese. Each problem is annotated with a decision and explanation before the edited version. The PT-BR localization that follows is not a translation of Version 2 — it is an adaptation that applies Brazilian children's narrative conventions.

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

A Grade 1–2 reader (ages 6–8) is unlikely to know any of these words, and the surrounding context does not support meaning inference for them. "Peculiar" and "contemplated" are the most significant flags: they belong in Grade 4+ text. "Contemplated" in particular does no work here that "looked at" cannot do better, and with less friction. "Mighty" stays in some children's content because it appears in read-aloud contexts where an adult can gloss it; here it reads as the narrator's word, not Leo's, so it goes. "Duly" in the final sentence also registers above level, but that sentence is being cut for other reasons (see A-04).

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
| 1 | "show and tell" (removed in V2) | Cultural adaptation | Replaced with neutral action in V2; rendered in V3 as *"mostrar o pinhão para os amigos da turma"* | "Show and tell" has no equivalent practice in Brazilian schools. The V2 edit neutralized the cultural reference; the PT-BR version reshapes the phrasing slightly to fit the natural rhythm of how a Brazilian child would describe sharing something with classmates. |
| 2 | Narrator warmth / close register | Register | Applied diminutive suffix throughout: *"pequenininho," "pinhãozinho," "coisinha"* | In Brazilian children's narrative, the diminutive suffix (-inho/-inha) signals affection and closeness — not just small size. Omitting diminutives in PT-BR children's text reads as cold or adult-formal. The forms used here (*pinhãozinho*, *pequenininho*) follow the same principle: they mark the narrator's tenderness toward Leo and his tiny seed, not just its size. |
| 3 | "acorn" / "oak tree" | Cultural adaptation | Rendered as *"pinhão"* and *"araucária"* in PT-BR | This is not a direct translation. *"Bolota"* is the technically correct PT-BR word for acorn, but acorns and oak trees are not part of everyday Brazilian life. The pinhão (seed of the araucária tree) is deeply familiar in southern Brazil (Paraná, Santa Catarina, Rio Grande do Sul), where it is a winter food and a cultural symbol. The localization team chose to adapt the seed and tree rather than translate them literally, because the target audience would recognize a pinhão falling from an araucária immediately and intuitively in a way they would not recognize an acorn falling from an oak tree. |
| 4 | Oak tree (*"carvalho"*) | Cultural adaptation | Adapted to *"araucária"* | Oak trees are not native to Brazil. Rather than retain *carvalho* for brand consistency, this localization made the adaptation transparent: the tree was changed to the araucária, the native Brazilian conifer whose seed is the pinhão. This is a conscious editorial decision, not a silent translator choice, and should be documented in the production notes. |
| 5 | *"small and brown, with a tiny cap on top — like a little hat"* | Visual adaptation | Description rewritten to match pinhão appearance (elongated, dark, smooth, pointed at both ends) | The cap is what makes an acorn visually distinctive. A pinhão has no cap. Carrying the cap description into the PT-BR version would describe something that does not exist. The entire visual description was rewritten to match the actual pinhão: dark, elongated, smooth-shelled, pointed at both ends, shiny. A Southern Brazilian child reading this would recognize it. |

---

## Version 3 — PT-BR Localization

*Acorn Tales: A Menor Semente*

A vovó de Leo deu para ele um pinhão numa manhã de sábado. Era pequenininho e escuro, comprido e brilhante, com uma casquinha lisa e pontinhas nas duas extremidades.

— O que ele faz? — Leo perguntou.

— Se você cuidar bem dele — disse a vovó —, ele vai virar uma araucária enorme um dia.

Leo olhou para o pinhãozinho. Não dava para acreditar que uma coisa tão pequenininha pudesse virar algo tão grande assim. Virou o pinhãozinho de um lado para o outro. Será que ele ia mesmo virar uma árvore? Uma árvore cheia de passarinhos?

Naquela tarde, Leo quis mostrar o pinhão para os amigos da turma. Colocou o pinhão com cuidado no bolso da jaqueta para não perder.

Na segunda-feira, Leo ficou de pé na frente da turma e ergueu o pinhãozinho bem alto.

— Essa coisinha aqui — ele disse — vai virar uma árvore enorme um dia.

Os colegas se aproximaram para ver de perto.

---

## Skills Demonstrated

The five problems in Version 1 are the kind that don't show up as spelling errors — vocabulary above level, passive constructions, a register break, a run-on, a culturally specific classroom practice. The annotations show why each one is a problem for this reader, not just that it is one.

"Show and tell" is the clearest example of what this document is demonstrating: it passes EN spell-check, reads fluently, and fails at localization. Catching it in the editorial stage — before a translator has to approximate it in PT-BR — is what makes the review useful. The pinhão/araucária adaptation makes the same point: some decisions need to surface, not be made silently.

Version 3 isn't a translation of Version 2. The dialogue punctuation, the diminutive register, and the sentence rhythm reflect how Brazilian children's narrative is actually written. The localization notes document why each non-literal choice was made.
