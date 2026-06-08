# 📝 mathtest — A Teacher-Style Practice Test Generator

A personal Claude Code skill that generates style-matched practice tests for a specific
high school math class by learning from past quizzes, then grades attempts using the
teacher's rubric and tracks mastery over time.

## The problem

Generic practice problems don't match how individual teachers actually write tests. My
Accelerated Algebra II teacher (Mr. Wallis) has a distinctive style — conjugate-pair
traps, "use your answer above" chain questions, optimization word problems with silly
named characters, a "no calculator / no `e` / no `ln`" constraint, multi-part questions
with conceptual sub-prompts. Studying generic problems from a textbook leaves you
unprepared for the style of the actual quiz.

## What it does

**Given:**

- Past quizzes (photos, PDFs, or typed) from the teacher
- A topic list for the upcoming quiz
- *(Optional)* class problems for the current unit

**It produces:**

- A practice test that matches the teacher's format, phrasing, difficulty curve, and trick patterns
- A grading pass on the student's completed attempt using the teacher's **C / S / D / M / N** rubric
- A diagnostic report identifying specific weak spots and what to drill before quiz day
- A mastery tracker that mirrors the teacher's spiraled gradebook system

## How it works

**Mode A — Generate:**

```
/mathtest <topic>
```

The skill reads all past tests in `past-tests/`, analyzes them against `style-notes.md`
(an evolving scouting report on the teacher), and produces a practice test in
`generated/` with the right mix of:

- ~30% homework-similar problems (confidence builders)
- ~50% concept combos (2–3 ideas in unfamiliar setups)
- ~20% harder applied problems / word problems

**Mode B — Grade:** Drop a photo of your attempt. The skill assigns a C/S/D/M/N letter
per question (matching the teacher's holistic rubric), shows the full worked solution,
identifies the specific gap, and gives ranked study recommendations.

## Architecture

```
math-tests/accel-alg-2/
├── past-tests/         # input: photos/PDFs of real quizzes, organized by quiz #
├── topic-lists/        # input: what the upcoming quiz will cover
├── class-work/         # optional input: in-class problems for the current unit
├── style-notes.md      # auto-updated scouting report on the teacher's style
├── generated/          # output: practice tests + graded versions
├── taken/              # archived attempts
└── mastery-tracker.html  # interactive sortable tracker with 65/35 weighted formula
                          # matching the teacher's gradebook
```

The slash command itself lives at `~/.claude/skills/mathtest/SKILL.md`.

## Notable features

- **Style-aware generation** — recognizes signature question patterns (e.g., "rational coefficients only" → conjugate-pair trap on polynomials)
- **Per-teacher constraints baked in** — no-calculator + no-`e` + no-`ln` means generated answers are always in exact form (`log_(1.015)(2)/4`, `⁵√2 − 1`, etc.)
- **Mastery tracker with Canvas-verified anchoring** — uses a 65/35 weighted rolling formula (matching the teacher's actual gradebook) and supports Canvas anchor values that override the model's estimate when real data is available
- **Spiral-aware** — recognizes that old topics will reappear and includes "throwback section" questions in practice tests

## Results

Across one semester of use (Quizzes 1–7 in Accelerated Algebra II):

- Mastery climbed from a starting B+/A− mix to an overall **A− (90.9/100)** at semester end
- Polynomials jumped from B to A− on the CYO (choose-your-own) final quiz, exactly as predicted from the practice test
- Identified specific recurring gaps (compound interest formula, rational expression sign tricks) and drilled them before they hit a real quiz

## Tech

- Claude Code skill (Markdown `SKILL.md` + agent instructions)
- HTML/CSS/JS for the printable test sheets and mastery tracker (no build step — opens directly in browser)
- macOS `sips` for HEIC → JPEG conversion when feeding in phone photos
