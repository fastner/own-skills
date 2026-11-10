# Effective Skeptic: comparison and design choices

Research date: 10 November 2026. This compares published instructions, not their
empirically measured effectiveness. No third-party skill was installed or run.
The instructions here are independently written.

| Source | Approach | Decision for Effective Skeptic |
| --- | --- | --- |
| [ng/adversarial-review](https://github.com/ng/adversarial-review/blob/main/skills/codex-review/SKILL.md) | Optimizer and Skeptic passes; checks false positives and risky fixes | Challenge our own findings and remedies. Preserve unresolved disagreement. Omit fixed models, confidence percentages, automatic repairs and default PR comments |
| [Tribunal](https://github.com/SpecialITWeapons/tribunal-claude-skill/blob/master/skills/tribunal/SKILL.md) | Advocacy, critique, judgment, then a challenge to that judgment; bounded reconsideration and clarification of missing facts | Preserve the strongest reasonable case and challenge the conclusion. Resolve a missing goal before judging it. Keep orchestration optional |
| [Codex-Devil-Advocate](https://github.com/wavehs/Codex-Devil-Advocate/blob/main/skills/adversarial-review/SKILL.md) | Strict code-review protocol ties conclusions to snapshots, bounded loops and verifiable reviewer metadata | Make stale-version limits explicit. Keep bounded follow-up. Do not require runtime attestation for ordinary session reviews or claim prompts enforce isolation |
| [Devil-advocate proposal, mattpocock/skills issue 699](https://github.com/mattpocock/skills/issues/699) | Checks contradictions, gaps, sequencing and already-answered objections | Add cross-section checks and discard resolved objections. This is a community proposal closed as not planned, not an adopted official skill |

Existing strengths remain: read-only assessment by default, explicit user
authorization for steering, evidence-scoped verdicts, surviving conclusions,
proportionate blocking and no compulsory independent reviewer.

## Input contract

- A session reference alone is enough: recover the goal from user instructions
  and accepted changes. Ask only if that goal remains unclear.
- A session plus natural language preserves the requested emphasis and limits.
- Free text or an artifact works without a session. Use its stated goal or
  established chat context; do not search unrelated sessions.
- A missing or ambiguous goal requires a concise question before a goal-based
  verdict or steering. Do not invent intent.

## Validation limits

The format validator and Dalo's deterministic audit check packaging and static
findings. They do not demonstrate goal-discovery quality or resistance to false
positives. Those require observation in actual reviews or a separately scoped
behavioral evaluation.
