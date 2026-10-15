# topic-primer

An agent skill that turns any topic into world-class teaching — from absolute zero to expert — through eight structured modes.

## What it does

| Mode | Ask with… | Delivers |
|------|-----------|----------|
| foundation | "teach me X from zero" | Step-by-step basics, every term defined, plain language |
| curriculum | "curriculum/roadmap for X" | 4–6 beginner→expert stages with practice and readiness gates |
| concepts | "teach X one concept at a time" | Explain → example → common mistake → check loop |
| tutor | "be my personal tutor for X" | Diagnostic-first adaptive teaching until demonstrated competence |
| models | "how do experts think about X" | The mental models and decision rules professionals use |
| pitfalls | "common mistakes learning X" | Mistakes ranked by damage, with exact corrections |
| examiner | "quiz/test me on X" | Basic-to-advanced questions, honest grading, scorecard |
| eli5 | "explain like I'm 5", "plain English" | Ultra-simple analogies from everyday objects, no jargon, one idea per turn |

## Core principle

Real understanding, not the illusion of it. The skill asks **one question at a time and waits for your answer** before continuing, grades honestly instead of praising, defines every term before using it, and never fabricates facts or resources. If your answer is close but wrong, it names the exact gap.

## Install

Copy the `skills/topic-primer/` directory into the skills directory supported by your AI agent:

```text
.claude/skills/topic-primer/
.agents/skills/topic-primer/
.cursor/skills/topic-primer/
.qoder/skills/topic-primer/
```

Or install via the Skills CLI:

```bash
npx skills add arm-pz/topic-primer --skill topic-primer
```

## Usage

```
/topic-primer black holes            # topic only → shows the mode menu
/topic-primer recursion foundation   # explicit mode
```

Or just ask naturally:

- "Teach me Kubernetes from absolute zero"
- "Design a curriculum to master data structures"
- "Test my understanding of photosynthesis like a strict examiner"
- "What mistakes do people make learning statistics?"

## Full-mastery path

For complete mastery of one topic, the modes chain: foundation → curriculum → concepts → tutor → models → pitfalls → examiner.

## Tests

`tests/test-prompts.md` contains the scenarios the skill was validated with (mode routing, one-question-and-wait compliance, ambiguous-topic menu).

## License

MIT
