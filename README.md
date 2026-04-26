# Unreasonable Hospitality Lens

> A Claude Code skill that audits software products through Will Guidara's *Unreasonable Hospitality* principles.

A hospitality audit, not a UX review. It surfaces where a product delivers competent service (black and white) but fails to make people feel something (colour).

## What it does

Evaluate any software artefact — a flow, UI, PRD, codebase, or single error message — against ten principles drawn from Guidara's book and translated into software evaluation criteria. The skill diagnoses gaps in Guidara's vocabulary (one-inch violations, canelé thinking, monologue hospitality) and produces a structured audit with priority fixes.

This skill is **evaluative only**. For generative work (writing onboarding, error copy, welcome flows), use the companion skill `hospitality-design-partner`.

## When to use it

Trigger phrases:
- "hospitality audit"
- "Guidara lens"
- "hospitality check"
- "where's the colour missing"
- "audit for hospitality"

Also useful for:
- Reviewing a client's product for emotional gaps
- Preparing a hospitality teardown as a sales tool
- Pre-launch review of a feature or flow
- Auditing error states, empty states, or onboarding

## The ten principles

1. Service vs Hospitality (Black and White vs Colour)
2. The One-Inch Rule
3. The Rule of 95/5
4. Their Perception Is Our Reality
5. Canelé vs Granola (Serving Yourself vs Serving the User)
6. Make the Charitable Assumption
7. Earning Informality
8. Hospitality Is a Dialogue, Not a Monologue
9. The Welcome
10. The Way You Do One Thing Is the Way You Do Everything

Each principle is defined in [SKILL.md](SKILL.md) with software-specific diagnostic criteria and language.

## Inputs accepted

- A URL (fetched and audited live)
- Screenshots or images
- Code (React components, HTML, full apps)
- A PRD or product spec
- A description of a product, feature, or flow
- A single error message or notification

## Output

Every audit follows the same structure:

1. **Overall Assessment** — one paragraph framing the hospitality posture
2. **Principle-by-Principle Findings** — verdict, finding, and location for each applicable principle
3. **The Hospitality Score** — 1-10 on Service and 1-10 on Hospitality (the gap is the opportunity)
4. **Priority Fixes** — top 3-5 changes ranked by impact, with effort estimates
5. **The 5% Opportunity** — one "unreasonable" idea: the sled moment

## Installation

Drop the skill folder into your Claude Code skills directory:

```
~/.claude/skills/unreasonable-hospitality-lens/
└── SKILL.md
```

Claude Code auto-discovers skills on startup. Once installed, invoke with `/unreasonable-hospitality-lens` or any of the trigger phrases above.

## Companion skills

- **`hospitality-design-partner`** — generative counterpart. Use when you want to *write* the welcome sequence, error copy, empty states, or offboarding flow rather than audit existing ones.

## Credit

Built on the principles in *Unreasonable Hospitality* by Will Guidara. The book is the source; this skill is the lens.
