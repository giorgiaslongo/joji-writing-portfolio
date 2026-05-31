# Bilingual Release Notes: Project Acorn App v2.4

**Doc ID:** DOC-2026-02A  
**Status:** V1.0  
**Target Audience:** End-users (parents and educators); EN and PT-BR versions  
**Reading Level Target:** Flesch-Kincaid Grade 6 (EN); equivalent for PT-BR  
**A11y Status:** Plain language; no jargon; consistent terminology  
**Changelog:**

| Version | Date | Change |
|---|---|---|
| V1.0 | May 2026 | Initial bilingual release notes |

---

## About This Sample

This document demonstrates the process of translating raw developer commit log entries into user-facing release notes in both English (EN) and Brazilian Portuguese (PT-BR).

Project Acorn is a fictional bilingual educational app used as a constructed example. The developer log below is the raw input converted into clear, audience-appropriate communication.

---

## Source Material: Developer Commit Log (Internal)

> *This is the raw input. It is not published. It is reproduced here to show the translation process.*

```
v2.4 – May 2026
- Refactored auth token logic; migrated to OAuth 2.0
- Fixed null pointer exception on dashboard init for users on iOS 16.3
- Implemented dark mode toggle via system preference detection
- Deprecated legacy XML parser; migrated content pipeline to JSON
- Added subtitle support flag to video player component (off by default)
- Resolved race condition in progress sync on low-bandwidth connections
- Updated onboarding flow: removed Step 3 (redundant), reordered Steps 4–6
- Bumped minimum Android API to 26 (Android 8.0 Oreo)
```

---

## Translation Process: Notes

The table below documents the editorial decisions made when converting each commit entry to user-facing copy. This is the reasoning layer — it is not published, but it reflects the QA judgment behind each revision.

| Developer entry | User-facing decision | Rationale |
|---|---|---|
| "Refactored auth token logic; migrated to OAuth 2.0" | "Security improvements to keep your account safe" | Users do not need to know the protocol. The benefit is security and continuity. Naming OAuth 2.0 adds no value to a parent or educator. |
| "Fixed null pointer exception on dashboard init for iOS 16.3" | "Fixed a startup issue for users on iOS 16.3" | "Null pointer exception" is meaningless to this audience. "Startup issue" is accurate and actionable — users now know this affected them specifically. |
| "Implemented dark mode toggle via system preference detection" | "Dark mode is now supported. The app will follow your device's display settings automatically." | Translating the mechanism ("system preference detection") would mean nothing to a parent or educator. The decision was to reframe it as an outcome: "follows your device's display settings" tells the user what happens from their side, not how the app does it. "Automatically" carries the same reassurance without any technical vocabulary. |
| "Deprecated legacy XML parser; migrated content pipeline to JSON" | *(Not published)* | Backend infrastructure change. Zero user-facing impact. Omitting it avoids confusion without omitting meaningful information. |
| "Added subtitle support flag to video player (off by default)" | "Subtitles are now available for activity videos. Turn them on in Settings → Accessibility." | "Flag" and "off by default" are developer shorthand. Users need to know the feature exists and how to find it. The accessibility path is spelled out. |
| "Resolved race condition in progress sync on low-bandwidth connections" | "Progress now saves correctly on slower internet connections." | "Race condition" is jargon. The user-facing impact is: their progress was not saving reliably on slow connections. It now does. |
| "Updated onboarding flow: removed Step 3, reordered Steps 4–6" | "Setup is faster. We removed a step and simplified the process." | The step numbers ("Step 3," "Steps 4–6") are internal workflow labels, not user landmarks. The decision was to translate the structural change as a user benefit: "faster" and "simplified" are what the change means to someone setting up their child's account. The specific step count was dropped because it implies the user was tracking it — they were not. |
| "Bumped minimum Android API to 26 (Android 8.0 Oreo)" | "Minimum Android version: Android 8.0 (Oreo). Older devices may no longer be supported." | This is a breaking change for some users. It must be communicated clearly, with the version name users recognize (Oreo), not just the API number. |

---

## Output: User-Facing Release Notes

### English (EN)

---

**Project Acorn — Version 2.4**  
*May 2026*

**What's new**

- **Dark mode support.** The app now follows your device's display settings automatically. No extra steps needed.
- **Subtitles for activity videos.** Subtitles are now available for all learning videos. Turn them on in **Settings → Accessibility**.
- **Faster setup.** We removed a step from the setup process and simplified the flow.

**Fixes**

- Fixed a startup issue for users on iOS 16.3.
- Progress now saves correctly on slower internet connections.
- Security improvements to keep your account safe.

**Important: Android compatibility update**

This update requires Android 8.0 (Oreo) or later. If your device runs an older version of Android, it may no longer support Project Acorn after this update. Please check your device settings if you experience any issues.

*Questions? Contact us at support@projectacorn.app*

---

### Brazilian Portuguese (PT-BR)

---

**Project Acorn — Versão 2.4**  
*Maio de 2026*

**O que há de novo**

- **Suporte ao modo escuro.** O aplicativo agora acompanha automaticamente as configurações de exibição do seu dispositivo. Sem etapas adicionais.
- **Legendas nos vídeos das atividades.** As legendas já estão disponíveis em todos os vídeos de aprendizado. Ative-as em **Configurações → Acessibilidade**.
- **Configuração mais rápida.** Removemos uma etapa do processo de configuração e simplificamos o fluxo.

**Correções**

- Corrigido um problema de inicialização para usuários com iOS 16.3.
- O progresso agora é salvo corretamente em conexões de internet mais lentas.
- Melhorias de segurança para manter sua conta protegida.

**Importante: atualização de compatibilidade com Android**

Esta atualização exige o Android 8.0 (Oreo) ou versão mais recente. Se o seu dispositivo utiliza uma versão anterior do Android, é possível que o Project Acorn não seja mais compatível após esta atualização. Verifique as configurações do dispositivo caso encontre algum problema.

*Dúvidas? Entre em contato pelo e-mail support@projectacorn.app*

---

## Localization Notes: EN → PT-BR

The following notes document choices made during translation that go beyond direct conversion.

| Issue | Decision | Rationale |
|---|---|---|
| "What's new" | *"O que há de novo"* (not *"Novidades"*) | *Novidades* is more informal and common in marketing copy. *O que há de novo* is clearer and more literal — appropriate for a release note context where precision matters. |
| "Fixes" | *"Correções"* (not *"Consertos"* or *"Reparos"*) | *Correções* is the standard term in Brazilian Portuguese software contexts. *Consertos* and *Reparos* are used for physical repairs and would sound incongruous. |
| "Turn them on in Settings" | *"Ative-as em Configurações"* | The verb *ativar* (to activate) is the correct register for app settings in PT-BR. *Ligar* (to turn on) is used for physical switches and sounds informal in UI copy. |
| "No extra steps needed." | *"Sem etapas adicionais."* (not *"Nenhuma ação adicional é necessária."*) | The literal translation is grammatically correct but reads as translated rather than native. *Sem etapas adicionais* is shorter, more conversational, and consistent with how PT-BR product copy handles confirmation statements. |
| "Questions?" | *"Dúvidas?"* | Direct translation of "Questions?" would be *"Perguntas?"*, which sounds formal and academic in PT-BR. *"Dúvidas?"* is the standard, natural choice for customer-facing support prompts. |
| iOS/Android version names | Kept in EN (*Oreo*, *iOS 16.3*) | Brand names and OS version identifiers are not localized. Translating them would create confusion when users check their device settings, which display the original names. |
| Emoji and punctuation | No changes | Emoji usage is consistent across EN and PT-BR audiences. Punctuation conventions (period, comma) are the same in both. |

---

## Skills Demonstrated

- Converting developer commit logs into plain-language, user-facing release notes
- Applying a consistent editorial standard (omitting backend changes, flagging breaking changes clearly)
- Bilingual content production with documented localization rationale
- Understanding register differences between EN and PT-BR in a UI/software context
- Structuring a bilingual document for professional review
