# Bilingual Release Notes: Vessel v1.3

**Doc ID:** DOC-2026-02A
**Status:** V1.0
**Target Audience:** Players (EN and PT-BR); game version update communication
**Reading Level Target:** Plain language; accessible to casual gamers
**Changelog:**

| Version | Date | Change |
|---|---|---|
| V1.0 | May 2026 | Initial bilingual release notes sample |

---

## About This Sample

This sample shows localization judgment under a gaming-specific register: technical commit entries are converted into player-facing patch notes without losing compatibility, accessibility, or save-file risk information. Vessel is a fictional indie RPG used as a constructed example; the commit log below is invented source material.

---

## Source Material: Developer Commit Log (Internal)

> *This is the raw input. It is not published. It is reproduced here to show the translation process.*

```
Vessel v1.3 – May 2026
- Fixed crash on Sealed Area map entry when loading a Chapter 1 save file
- Added Chapter 2 opening cutscene (EN and PT-BR subtitle support included)
- Rebalanced encounter rate for first-time players in Act 1
- Resolved silent save file corruption when quitting during autosave
- Added accessibility option: reduce flashing effects during combat sequences
- Fixed audio desync on PT-BR subtitle track (Chapter 1, Scene 4)
- Updated minimum iOS version to 16.0; older devices will receive a compatibility warning
```

---

## Translation Process Notes

The table below documents the editorial decisions made when converting each commit entry to player-facing copy. This layer is not published, but it reflects the QA judgment behind each revision.

| Developer entry | User-facing decision | Rationale |
|---|---|---|
| "Fixed crash on Sealed Area map entry when loading a Chapter 1 save file" | "Fixed a crash that could happen when entering the Sealed Area with a Chapter 1 save." | The commit is precise for debugging purposes, but "on map entry when loading" is awkward in player copy. Restructured as a conditional ("that could happen when") to match how players describe problems: what they were doing, not what the system was doing. |
| "Added Chapter 2 opening cutscene (EN and PT-BR subtitle support included)" | "Chapter 2 is here. The opening cutscene is now available with subtitles in English and Portuguese." | Two user-relevant facts folded into one commit. Split into two sentences: the chapter arrival (high-priority for players who were waiting) and the subtitle detail. The parenthetical in the commit is internal notation; subtitle languages are named in full for players. |
| "Rebalanced encounter rate for first-time players in Act 1" | "Act 1 is now easier to get through on a first playthrough. Encounters are less frequent." | "Rebalanced encounter rate" is design vocabulary. The player-facing meaning is: Act 1 is less punishing now. Two short sentences instead of one technical phrase. "First-time players" becomes "first playthrough" (players think in runs, not identity labels). |
| "Resolved silent save file corruption when quitting during autosave" | "Fixed: save files were occasionally getting corrupted when closing the game during an autosave. This happened silently (no error message appeared)." | The word "silent" is the critical detail. The player never saw an error message, so they had no way to know something was wrong. Keeping that information in the user-facing note helps players understand why they might have lost progress and confirms the fix is real. "Resolved" becomes "Fixed" (plainer). "Quitting during autosave" becomes "closing the game during an autosave" (more natural in player language). |
| "Added accessibility option: reduce flashing effects during combat sequences" | "New in Settings → Accessibility: option to reduce flashing effects during combat." | Commit format (colon-separated feature flag) is internal shorthand. Player-facing version leads with where to find it, then names what it does. "Combat sequences" trimmed to "combat" (no precision lost). |
| "Fixed audio desync on PT-BR subtitle track (Chapter 1, Scene 4)" | "Fixed a sync issue with Portuguese subtitles in Chapter 1." (EN notes only; this was a PT-BR-specific fix) | "Audio desync" and "Scene 4" are technical and granular. Players need to know: subtitles in Chapter 1 were out of sync, now fixed. Scene-level precision is omitted (players do not navigate by scene number). This entry appears in EN notes for transparency, but the fix is only relevant to PT-BR players, so the PT-BR version leads with it more prominently. |
| "Updated minimum iOS version to 16.0; older devices will receive a compatibility warning" | "Vessel now requires iOS 16.0 or later. If your device runs an older version, it may no longer be supported after this update." | Breaking change. Must be communicated clearly and directly, not buried. The passive "older devices will receive a compatibility warning" is softened developer language. "May no longer be supported" puts the consequence on the player's device in plain terms. iOS version names stay in EN (brand standard). |

---

## Output: User-Facing Release Notes

### English (EN)

---

**Vessel: Version 1.3**
*May 2026*

**What's new**

- Chapter 2 is here. The opening cutscene is now available with subtitles in English and Portuguese.
- New in Settings → Accessibility: option to reduce flashing effects during combat.

**Fixes**

- Fixed a crash that could happen when entering the Sealed Area with a Chapter 1 save.
- Act 1 encounter rate reduced for first-time players.
- Save files are now protected from corruption when the game closes during an autosave.
- Fixed a subtitle sync issue in Chapter 1.

**Compatibility**

Vessel now requires iOS 16.0 or later. If your device runs an older version, it may no longer be supported after this update.

*Questions? support@vessel.game*

---

### Brazilian Portuguese (PT-BR)

---

**Vessel: Versão 1.3**
*Maio de 2026*

**Novidades**

- O Capítulo 2 chegou. A cutscene de abertura já está disponível com legendas em inglês e português.
- Nova opção em Configurações → Acessibilidade: reduzir efeitos piscantes durante o combate.

**Correções**

- Corrigido um crash que podia acontecer ao entrar na Área Selada com um save do Capítulo 1.
- Corrigido o problema de sincronização das legendas em português no Capítulo 1.
- A frequência de encontros no Ato 1 foi reduzida para quem está jogando pela primeira vez.
- Os saves agora estão protegidos contra corrupção ao fechar o jogo durante o salvamento automático. Antes, isso acontecia sem nenhuma mensagem de erro.

**Compatibilidade**

O Vessel agora requer iOS 16.0 ou versão mais recente. Se o seu dispositivo usa uma versão mais antiga, é possível que ele não seja mais compatível após essa atualização.

*Dúvidas? support@vessel.game*

---

## Localization Notes: EN → PT-BR

| Issue | Decision | Rationale |
|---|---|---|
| "What's new" | "Novidades" (not "O que há de novo") | In the educational app context (Projeto Verbly, same doc series), "O que há de novo" was the right call: the audience was parents and educators, and precision mattered over tone. Gaming patch notes are a different register. Players expect "Novidades": it is what they see in App Store updates, patch note threads, and gaming community posts in PT-BR. Using "O que há de novo" would read as formal in this context. |
| "Chapter" | "Capítulo" (not "Fase") | "Fase" is the conventional PT-BR term in platformers and mobile games, where stages are numbered levels. Vessel is a story-driven narrative RPG: chapters mark story milestones, not numbered stages. "Capítulo" is what PT-BR players use when talking about games in this genre. The distinction matters because the wrong term signals genre mismatch. |
| Silent save corruption | "Antes, isso acontecia sem nenhuma mensagem de erro." | The EN version uses the word "silently" to describe the corruption. "Silenciosamente" is grammatically correct in PT-BR, but it reads as cold and technical: closer to a system log than a player note. "Sem nenhuma mensagem de erro" is longer but natural, and it puts the player's experience first (they saw nothing, so they had no way to know). The meaning is preserved; the register is not. |
| "Encounter" | "Encontros" (not "batalhas" or "inimigos") | "Encontro" is the standard term in PT-BR RPG communities for what EN calls a random encounter: a triggered combat event in the game world. "Batalha" (battle) refers to the combat itself, not the trigger. "Inimigos" (enemies) would change the meaning of the sentence entirely. "Encontros" is the correct term for players who discuss games in PT-BR online spaces (forums, wikis, Discord servers). |
| "Chapter 1 save" | "save do Capítulo 1" (English "save" kept) | "Arquivo de save," "arquivo salvo," and "jogo salvo" all exist in PT-BR, but the gaming community overwhelmingly uses "save" as a loanword (as in: "perdi meu save," "faz o save antes de ir"). Translating it as "arquivo salvo" would sound overly formal and slightly out of place for players who talk about their saves in Portuguese the way they naturally do. Brand-adjacent nouns borrowed from gaming EN are kept as-is in PT-BR gaming copy. |

---

## Skills Demonstrated

- Translating internal technical language into player-facing communication without losing critical information
- Adapting PT-BR choices to gaming register instead of reusing educational-app phrasing
- Preserving compatibility, accessibility, subtitle, and save-file risk details in plain language
- Documenting audience-specific localization decisions rather than treating translation as word substitution
