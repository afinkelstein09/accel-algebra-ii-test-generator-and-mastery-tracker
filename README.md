# math-tests

A style-matched practice-test generator and grade tracker for my math classes.

Feed it photos of past tests, and it generates new practice tests that match the
teacher's style and difficulty mix — then grades my attempts and diagnoses what to
study before the real thing.

## Classes

- **[`accel-alg-2/`](accel-alg-2/)** — Accelerated Algebra II. See its
  [README](accel-alg-2/README.md) for how the generator and mastery tracker work.

## How it works (short version)

1. Drop past tests into `past-tests/` (photos or typed).
2. Generate a practice test with the `/mathtest` workflow.
3. Take it on paper, then get it graded with full worked solutions and a
   "study this harder" diagnostic.
4. Track progress over time in `mastery-tracker.html`.
