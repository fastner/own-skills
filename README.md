# own-skills

Personal agent skills, distributed through Dalo.

## Effective Skeptic

[`effective-skeptic`](skills/effective-skeptic/SKILL.md) reviews another session's results against
the user's goal. It challenges evidence, tests, alternative explanations and
delivery assumptions, and records conclusions that survive scrutiny.

Examples:

- `$effective-skeptic <Session-Link>` — reads the session and recovers its goal;
  asks the user if the goal cannot be established.
- `$effective-skeptic Prüfe den aktuellen Stand von <Session-Link>. Führt das zum Ziel?
  Sind die Tests aussagekräftig? Keine Dateien ändern und nichts senden.`
- `$effective-skeptic Teile diese Prüfung mit <Session-Link>, damit der Plan überarbeitet
  wird. Bewahre die begründeten bestehenden Entscheidungen.`
- `$effective-skeptic Prüfe nach der Überarbeitung einmal, ob die beanstandeten Punkte
  geschlossen sind.`
- `$effective-skeptic Prüfe diesen Plan auf wiederkehrenden Umsatz bei begrenzter
  Betreuung: <Plan>` — free text works without any session link.

Assessment is read-only by default. Sending a correction requires the user's
authorization. The skill works with available session tools or supplied
artifacts; it does not require Effective Flow, another skill, or a fixed model.

Select `skills/effective-skeptic` from this repository with Dalo's catalog workflow,
review and approve `own-skills:effective-skeptic`, then reconcile the linked targets.
Updates follow the configured Dalo source policy.

The approach draws on Effective Flow's `investigate` skeptic: attempt to refute
conclusions, distinguish weakened from not-refuted claims, and state the checked
scope. It generalizes that method to plans, experiments and session steering.

[Comparison with other skeptic skills and design choices](docs/skeptic-design.md).
