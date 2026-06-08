# Teacher style notes — Accel Alg II

*Living scouting report. Built from quizzes 1–5.*

## Test format
- Header: `A2A S2Q[#]` (Algebra 2 Accelerated, Semester 2, Quiz #). Mini quizzes labeled `A2A S2mini [topic] quiz`.
- Name field top-left.
- **No calculator** policy on every quiz. Exact wording: *"No Calculator — you must fully justify all answers to receive full credit."*
- Length: typically **7–8 questions** per full quiz; mini quizzes ~3 questions.
- Heavy use of **multi-part questions** (a, b, c, d, sometimes through h). One setup, multiple skills.
- Topic-by-topic grading on the cover/back: teacher writes letter grades per concept area (e.g., "Algebra B / Functions C / Quadratics A / Polynomials B"). **Each question maps to a tracked topic.**

## Question phrasings the teacher favors
- *"Write values in standard complex form"*
- *"Find all complex zeros of f(x) = …"*
- *"Find all roots of … if f(c) = 0"* (gives one root, asks for the rest — forces polynomial division + complex conjugate logic)
- *"Write an equation of a degree X polynomial with [zeros/roots/y-intercept/constraint]"* — reverse-engineering polynomials
- *"Fully factor f(x) = …"*
- *"Provide a sketch of the equation below and provide the requested information. Label any points you use."*
- *"Find the requested information of the function f(x) given below"* (then a sub-list: degree, leading coeff, equation, intervals inc/dec, rel max/min, solve f(x)>0, transformations)
- *"Sketch and write the equation of a quadratic function f(x) that has a maximum value of … and zeros of …"*
- *"Be sure to include at least 3 points"* (graphing requirement)
- *"What is the domain and range of …?"*
- *"Find the inverse function of the following"*
- *"Graph each function from parts a and b and its inverse on the graphs below"*
- *"Simplify each such that there is only positive exponents"*
- *"Solve the following equations exactly"*
- *"Rewrite the following equation into the form b^x = a. Then provide a reasonable estimate for x."*
- *"Solve (without same exponent rules)"* — explicitly forces the harder log-based method
- *"Would the solution be positive or negative and why?"* — **conceptual prompts** that test understanding, not just computation
- *"Guess and check will receive no credit, you must justify and show work"* — appears on optimization word problems

## Common twists / trick patterns
- **Hidden complex conjugate pair requirement:** "rational coefficients only" or "real coefficients only" forces student to add a conjugate root that wasn't listed (e.g., zeros of -2 and 3i means you also need -3i).
- **Double / multiple roots that aren't explicitly called multiplicities:** problem says "double root at -15" or "double root at 1/2" — student has to translate that into multiplicity and adjust degree counting.
- **Inequalities by sign chart:** polynomial inequalities (x+8)³(x+5)(x-7)² < 0 — multiplicities matter for sign-flipping behavior.
- **Inverse + graph combo:** find inverse algebraically, then also graph both f and f⁻¹ on the same axes (mirror across y=x).
- **Functional value chains:** g(g⁻¹(2)) and similar nested compositions. Tests whether you understand the inverse undoes the function.
- **Two methods, one problem:** "Solve (without same exponent rules)" right after a same-base problem — forcing log method on something that looks like it could be done with bases.
- **Conceptual sub-question stuck onto a computation:** after solving for x, a follow-up like "would the answer be positive/negative and why?"
- **Mixed standard form requirements:** complex numbers must end in a + bi form, not left as fractions over (1+i) etc.

## Calculator policy
- **No calculator on every full quiz.** Exact arithmetic required. This is a structural constraint that shapes the problems — numbers are chosen to factor cleanly, exponents resolve to small integers, log arguments are powers of the base.
- **NO `e` and NO `ln` allowed** — confirmed from Quiz 6. Only base-b log notation: `log₂`, `log₁₀`, `log_(1.015)`, etc. The base of the log matches the base of the exponential.
- **All answers are expressions, not decimals.** Final compound interest answer is something like `4000(1.015)^20` — student does NOT compute this to a number. Same with logs: `log_(1.015)(2)/4` is the answer, not a decimal value.

### How application problems work without calculator / e / ln
Confirmed pattern from class problems:
- **Forward (find amount):** Leave as `P(1 + r/n)^(nt)` plugged in. Don't simplify the power.
- **Solve for time t** (variable in exponent): use base-b log. `t = log_(1.015)(2) / 4` form. The base of the log = the base of the exponential. NO ln, NO change-to-natural-log.
- **Solve for rate r** (variable in base): use nth root or fractional exponent. `r = 2^(1/5) - 1` or equivalently `⁵√2 - 1`. NO logs here — wrong tool.
- **Half-life / decay problems:** answer for "exact decay rate" looks like `1 - (1/2)^(1/4)`. Express as a constant; don't evaluate.
- **Doubling/tripling time:** `t = log_(growth factor)(2)` — base of log = the base inside the parentheses, NOT 10 and NOT e.

## Problem setup tendencies
- **Word problems are the signature.** Almost every quiz has 1–2:
  - **Optimization** (max area of a rectangle / pen / triangle, max height of projectile)
  - **Projectile-style with silly context** (asteroids, astronauts — h(t) = -2t² + 8t + 24)
  - **Geometry-into-function** (rectangle dimensions in terms of x, triangle with h and b given as expressions in x)
  - Often named characters ("Jimbo is creating rectangular pens for his 4 animals") — teacher likes a bit of personality
- **Symbolic > word for routine concepts.** Algebra/factoring/simplifying tends to be straight symbolic.
- **Reverse engineering is favored over forward computation.** "Build a polynomial that fits these constraints" rather than "given this polynomial, compute X."
- **Multi-representation:** a single concept (e.g., functions) is tested algebraically, graphically, and from a table of values within the same quiz.

## Difficulty curve
- **Quizzes ramp up.** Q1 is usually computational warm-up (simplify a complex expression, simplify with positive exponents). Final 1–2 questions are word problem + harder reverse-engineering or sign-analysis problem.
- **Word problems sit late.** Almost always in the back half of the quiz.
- **The conceptual "why" question is usually a sub-part on a later problem.**

## Grading rubric (per-question, holistic)

Teacher uses a letter scale on every graded question:

| Code | Meaning | What it looks like |
|------|---------|-------------------|
| **C** | **Complete response** | Solution complete, correct, convincing. Work shown in full. Strong grasp. |
| **S** | **Substantial response** | Minor details missing or argument not fully convincing. Impulsive calc errors or didn't follow directions, but solid grasp. |
| **D** | **Developing response** | Pretty good understanding but didn't fully solve OR didn't communicate well. Significant room for improvement. |
| **M** | **Minimal response** | Some evidence of understanding, but didn't put it together. Limited grasp; needs deeper study. |
| **N** | **Nothing yet** | No understanding demonstrated. Blank / virtually unworked. |

**Critical implications:**
- **Correct answer with little/no work = M to D max.** Bare answers don't score above developing.
- **Wrong final answer with strong work shown = S or even C.** The work is the point.
- The teacher explicitly cares about *feedback over points*. Educational research basis — focus on what to learn, not the score.

The +/- modifiers seen on actual quizzes (S+, M+, D+) are within-band fine-tuning.

## Mathematical principles (graded separately)

In addition to content targets, every assessment is graded on:
1. **Attention to detail and precision**
2. **Clarity and organization**
3. **Efficiency**

These show up in the gradebook alongside content targets.

## Gradebook system

- No overall grade per assessment — instead, **Learning Target Mastery levels** updated per topic.
- Mastery levels: **Flexible Mastery → Proficient → Developing → Beginning → No data** (color-coded green/yellow/red).
- **Proficient ≈ B+/A- range** (not 75%/C — the scale isn't traditional).
- Assessments are **spiraled** — same learning targets reappear across quizzes. Most recent scores weigh **65%**, so growth recovers from a bad early result.
- End-of-semester grade = average of all Learning Mastery Targets.

## On assessment day (teacher's stated policy)

Teacher will only answer:
- Clarification questions (if wording is unclear)
- Possible typo flags

For anything else, expect:
- *"Part of what I'm assessing is your ability to understand the question"*
- *"Just do your best and write any assumptions you made"*
- *"I can't answer that question"*

**Implication for practice:** if a problem feels ambiguous, write down your assumption and proceed. The teacher won't bail you out, and noting the assumption is part of the rubric (clarity/organization).

## Class-work observations (Quiz 6 unit — Logs/Exp/applications/Polynomials/Transformations)

From class problems Andrew shared, this teacher's current unit focus is wider than the topic list suggests. Specific patterns:

### Equivalent-form rewriting is heavily drilled
Class problems repeatedly ask to rewrite an exponential or log expression in **multiple equivalent forms**. Examples seen:
- `3(1/2)^(x-1) + 1` → `6·(1/2)^x + 1` → `6·2^(-x) + 1`
- `-2·3^(2-x) + 1` → `-2·(1/3)^(x-2) + 1` → `-18·3^(-x) + 1` → `-18·(1/3)^x + 1`
- `log_2(4/(x+3))` → `log_2(4) - log_2(x+3)` → `-log_2(x+3) + 2`
- `4^(-1/2(x+1))` → `(1/2)^(x+1)`

**Implication for test generation:** include at least one "rewrite this in equivalent form" or "show two equivalent expressions for…" problem. The teacher likes seeing manipulation across exponent rules and log properties.

### Compound interest is a major application focus
Multiple class problems on compound interest with different unknowns:
- Given P, r, n, t → find A
- Given A, r, n, t → find P
- Given P, A, r, n → solve for t (using logs)
- Given P, A, n, t → solve for r (using nth root)

Format used: A = P(1 + r/n)^(nt), with periods including quarterly, monthly. **The teacher likes asking the same problem with different unknowns** — students see the formula 4 ways.

**Implication for test generation:** at least one compound interest problem is highly likely on Quiz 6. Should include a non-trivial unknown (solve for t or r), not just plug-and-chug.

### Exact hourly/unit rates in decay/growth
Class problems explicitly demand the **exact hourly decay rate** (or growth rate) when given a periodic half-life or doubling time. Example: "drug has 45-min half-life, find exact hourly decay rate" → answer is `1 - (1/2)^(4/3)` exactly, not a decimal.

**Implication:** when generating decay problems, ask for the **exact rate per unit time**, not just the function. This forces the student to manipulate the exponent properly.

### "When are two quantities equal?" word problems
Recurring problem type:
- "In 1980, 170M vehicles increasing 4%/yr, 227M people increasing 1%/yr. When equal?"
- Setup: 170(1.04)^t = 227(1.01)^t → solve using log of ratio

**Implication:** include one "intersection of two exponential models" word problem if space permits.

### Inverses of exp/log function pairs
Class explicitly works through inverses of:
- `f(x) = -3·2^(x+4) + 1` (exponential → inverse is log)
- `g(x) = log_3(4x) - 2` (log → inverse is exp)
- `j(x) = -log_(1/2)(x/3)` (log with reflection)

Two-method approach shown: standard "swap x and y" method, plus "x = expr, then solve for y" method. Both methods yield the same answer.

**Implication:** at least one inverse-of-exp/log problem is mandatory. The current test has Q7d and Q10, which is good coverage.

### Graphing log/exp transformations
Class graphs include reflection, vertical shift, horizontal shift, and stretches — applied to both exp and log parents. Asymptote labeling is required (y = c for exp, x = c for log).

**Implication:** Q7 in current test (transformations of log_2) covers this well.

## Other observations
- Teacher writes feedback in red pen. Letter codes per sub-part = the C/S/D/M/N rubric above.
- Andrew's actual grades across the 5 quizzes (from cover sheets):
  - Quiz 1: Com A / Alg B+ / Quad A- / Fun B+
  - Quiz 3: Alg B / Func C / Quad A / Poly B
  - Quiz 5: TransFormations A / Functions A / Quadratics B- / Exponents A- / Logs A-
- **Weak spot signal across multiple quizzes: Algebra (simplifying/solving) and Functions tend to score lowest.** Quadratics and topic-specific units (exponents/logs) tend higher.
- Teacher seems to value: (1) showing every step of work, (2) exact form (no decimals), (3) recognizing implicit constraints (conjugate pairs, multiplicities), (4) using the correct method when specified.

## Other observations
- Teacher writes feedback in red pen. Letter codes per sub-part (S+, S, M+, M, C, D+, D, A) appear to be a step-level rubric.
- Andrew's actual grades across the 5 quizzes (from cover sheets):
  - Quiz 1: Com A / Alg B+ / Quad A- / Fun B+
  - Quiz 3: Alg B / Func C / Quad A / Poly B
  - Quiz 5: TransFormations A / Functions A / Quadratics B- / Exponents A- / Logs A-
- **Weak spot signal across multiple quizzes: Algebra (simplifying/solving) and Functions tend to score lowest.** Quadratics and topic-specific units (exponents/logs) tend higher.
- Teacher seems to value: (1) showing every step of work, (2) exact form (no decimals), (3) recognizing implicit constraints (conjugate pairs, multiplicities), (4) using the correct method when specified.

## Implications for test generation
- Always include a no-calculator notice in the header (`A2A practice — no calculator. You must fully justify all answers to receive full credit.`).
- Use multi-part question structure — single setup, build complexity across (a)(b)(c).
- Include 1–2 word problems per test, typically optimization or projectile, in the back half. Use a silly named character occasionally.
- Reverse-engineering problems ("write the equation of a polynomial with these zeros…") are signature — at least one per test.
- Drop in a conceptual sub-question ("explain why" / "would this be positive or negative") on a later problem.
- Bias the "needs more practice" topic mix toward Andrew's weak spots: **algebra simplification + functions** (especially inverses).
- Numbers should resolve cleanly without a calculator.

## Implications for grading Andrew's attempts
- Use the **C/S/D/M/N rubric** per question, not raw right/wrong.
- A correct boxed answer with no work shown earns at most **D** — flag this in feedback.
- A wrong final with strong, mostly-correct work earns **S** (sometimes C) — explain *why* the work was good even though the answer missed.
- Also evaluate the three **mathematical principles** at the end of each grading pass:
  - **Attention to detail / precision** — sign errors, misread question, incomplete final form
  - **Clarity / organization** — easy to follow? Steps labeled? Final answer boxed?
  - **Efficiency** — did he take the shortest reasonable path, or get tangled?
- Translate to the gradebook scale at the end: **C → Proficient/Flexible Mastery, S → Proficient, D → Developing, M → Beginning, N → No data**.
- Remember: the teacher's *spiraled* model means a topic graded weakly today is worth re-testing in the next practice run.
