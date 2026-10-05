# deep-tutor

An agent skill that turns any topic into world-class teaching — from absolute zero to expert — through seven structured modes.

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

## Core principle

Real understanding, not the illusion of it. The skill asks **one question at a time and waits for your answer** before continuing, grades honestly instead of praising, defines every term before using it, and never fabricates facts or resources. If your answer is close but wrong, it names the exact gap.

## Install

Copy the `skills/deep-tutor/` directory into the skills directory supported by your AI agent:

```text
.claude/skills/deep-tutor/
.agents/skills/deep-tutor/
.cursor/skills/deep-tutor/
.qoder/skills/deep-tutor/
```

Or install via the Skills CLI:

```bash
npx skills add arm-pz/deep-tutor --skill deep-tutor
```

## Usage

```
/deep-tutor black holes            # topic only → shows the mode menu
/deep-tutor recursion foundation   # explicit mode
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
