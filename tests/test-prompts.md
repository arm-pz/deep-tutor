# deep-tutor validation scenarios

Each scenario was run as a control (agent without the skill) and with the skill
loaded. The skill fixes the documented control failure.

## 1. Foundation from zero

**Prompt:** "Teach me recursion starting from absolute zero, assuming I have no
background at all. Build my foundation step by step."

- Control failure (no skill): 8-step wall of text, three practice problems plus
  two trailing questions in one turn; never waits.
- Expected with skill: short dependency ladder (term → concept → example →
  what-it-is-not → recap), ending with exactly **one** mini-check question as
  the final line of the turn.

## 2. Examiner testing

**Prompt:** "Test my understanding of photosynthesis as a strict examiner
would."

- Control failure (no skill): dumps "Tier 1 — Basic (5 questions). Answer all
  five before I move on." — batched questions.
- Expected with skill: announces rounds (basic → application → edge cases),
  then asks **one** question and waits; grades correct/partial/wrong with the
  missing piece named; closes with a scorecard.

## 3. Ambiguous topic

**Prompt:** "/deep-tutor black holes" (no mode given)

- Control failure (no skill): launches an advanced lecture (metric tensors) at
  a presumed-zero learner; no mode choice offered.
- Expected with skill: lists the seven modes briefly, asks which one, and
  suggests foundation for a new topic.

## 4. Concept chain waiting rule

**Prompt:** "Teach me [topic] one concept at a time"

- Expected: per concept — analogy, real example, its most common mistake, one
  comprehension question; the question is the last thing in the turn and the
  next concept appears only after the user answers.

## 5. Tutor diagnostics

**Prompt:** "Be my personal tutor for [topic]"

- Expected: opens with 3–5 diagnostic questions (this batch is intentional —
  they are placement questions asked together before teaching starts), waits
  for answers, then calibrates: skip known, drill half-known, rebuild unknown.
