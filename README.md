# Accel Algebra II — Test Generator & Mastery Tracker

A personal study system for my Accelerated Algebra II class. It learns the *style* of
my class's past quizzes and generates **original** practice tests that feel like the
real thing — then grades my attempts with the same rubric my teacher uses and tracks
which learning targets I've actually mastered over time.

It is not a copy of any answer key. It generates new problems in the teacher's format
so I can practice under realistic conditions before an assessment.

---

## The idea

Most practice problems don't match how my class is actually assessed — wrong format,
wrong difficulty, calculators allowed when mine aren't, decimals accepted when my
teacher demands exact form. So instead of generic worksheets, this system studies my
real quizzes and rebuilds *that* experience with fresh problems.

```
  past quizzes + teacher's released materials
                │
                ▼
        ┌───────────────┐
        │  style model  │   →  style-notes.md  (a living "scouting report")
        └───────────────┘
                │
                ▼
        generate practice test  ──►  take it on paper
                │                          │
                ▼                          ▼
         grade with the class rubric  ◄────┘
                │
                ▼
        mastery-tracker.html  (per-topic mastery over time)
```

---

## What it's "trained" on

The system isn't a model with weights — the "training data" is my own class material,
which it reads to build a style profile. Two sources:

1. **My previous quizzes** (`accel-alg-2/past-tests/`) — photos of the real graded
   quizzes 1–6, including the teacher's red-pen feedback and per-topic letter grades.
   This is where it learns format, phrasing, difficulty curve, and how work is scored.
2. **The teacher's released materials** (`accel-alg-2/topic-lists/`, plus stated class
   policies) — the topic lists handed out before each quiz, the no-calculator rule, the
   "justify all answers" requirement, and the grading philosophy. These tell it *what's
   coming* and *how it'll be judged*.

The more quizzes I feed in, the sharper the match. After 2–3 real quizzes the generated
tests start to feel genuinely like my teacher wrote them.

---

## How the "training" works

Every time new material goes in, the system updates **`style-notes.md`** — a living
scouting report on how this class is assessed. It currently captures things like:

- **Format DNA** — header style (`A2A S2Q#`), 7–8 multi-part questions, name field,
  no-calculator notice on every quiz.
- **Signature question types** — reverse-engineering polynomials from constraints,
  "find all complex zeros," compound-interest with a different unknown each time,
  optimization word problems with silly named characters.
- **Trick patterns** — hidden complex-conjugate requirements, double roots stated as
  words, "solve without same-exponent rules" forcing the log method, a conceptual
  "would this be positive or negative, and why?" tacked onto a computation.
- **Hard constraints** — no calculator, no `e` / no `ln`, all answers in exact form
  (`4000(1.015)^20`, not a decimal).
- **My weak spots** — across quizzes, *algebra simplification* and *functions/inverses*
  score lowest, so the generator deliberately over-weights those.

That file is the actual "model." Generated tests are produced from it.

---

## The workflow (a walkthrough)

1. **Feed it past tests.** Drop quiz photos into `past-tests/`.
2. **Add the topic list** for the next quiz into `topic-lists/` (whatever the teacher
   released).
3. **Generate** a practice test:
   ```
   /mathtest logs, exponentials, and inverses
   ```
   A new test lands in `generated/` — no answer key, realistic length and mix:
   - ~30% close to homework (confidence builders)
   - ~50% combinations of 2–3 concepts in unfamiliar setups
   - ~20% harder/applied versions
4. **Take it on paper**, timed, showing all work (since bare answers don't score well).
5. **Get graded.** I paste my answers or a photo of my work, and it marks each part,
   shows full worked solutions, and tells me exactly what to study harder.

See [`accel-alg-2/`](accel-alg-2/) for the live files and its
[README](accel-alg-2/README.md).

---

## Grading — it scores like the class does

My class doesn't use percentages. It uses a **mastery rubric**, and the grader mirrors
it:

| Code | Meaning |
|------|---------|
| **C** | Complete — correct, fully justified, strong grasp |
| **S** | Substantial — solid grasp, minor slip or detail missing |
| **D** | Developing — decent understanding, didn't fully land it |
| **M** | Minimal — some evidence, didn't put it together |
| **N** | Nothing yet |

Key consequences it respects:
- A **correct answer with no work shown caps at D** — the work is the point.
- A **wrong answer with strong work** can still earn S or C.
- Every attempt is also judged on **precision, clarity, and efficiency**, like the real
  rubric.

---

## Mastery tracking

`accel-alg-2/mastery-tracker.html` maps each topic to a mastery level
(**Flexible Mastery → Proficient → Developing → Beginning → No data**) and updates as I
take more practice tests. Because the class **spirals** topics (recent scores weighted
most), a weak early topic can recover — and the tracker shows whether it actually has.

---

## Repo layout

```
accel-alg-2/
├── README.md            how to use the generator for this class
├── style-notes.md       the living style model ("training")
├── mastery-tracker.html the per-topic mastery dashboard
├── past-tests/          real graded quizzes (input / training data)
├── topic-lists/         what each upcoming quiz covers (input)
├── generated/           practice tests + graded versions (output)
├── class-work/          extra in-class problems fed in for style
└── taken/               photos of my handwritten attempts (archive)
```

---

*Built as a personal exam-prep tool. Generated tests contain original problems written
to match my class's assessment style — they are not reproductions of any test.*
