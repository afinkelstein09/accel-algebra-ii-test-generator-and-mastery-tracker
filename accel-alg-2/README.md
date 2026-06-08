# Math test generator — Accel Alg II

## How to use

### 1. Feed it past tests
Drop past tests in `past-tests/` — photos (HEIC/JPG/PNG), PDFs, or typed `.md` files all work. The more, the better the style match.

### 2. Drop in the topic list (optional but helps)
When your teacher tells you what the next test will cover, save it in `topic-lists/` (photo or typed). Filename can be anything — `unit5-topics.md`, `IMG_1234.jpeg`, etc.

### 3. Generate a practice test
Run `/mathtest <topic>` — e.g.
```
/mathtest quadratics and complex numbers
```
A test appears in `generated/` as `test-YYYY-MM-DD-<topic>.md`. **No answer key yet.**

### 4. Take it on paper
Set a timer if you want realism. Show your work.

### 5. Get graded + diagnostic
Paste your answers in chat, or share a photo of your work. Claude will:
- Mark each question right/wrong
- Show full worked solutions
- Tell you exactly what to study harder before the real test

A graded copy is saved to `generated/test-YYYY-MM-DD-<topic>-graded.md`.

## Folders

- `past-tests/` — your real past tests (input)
- `topic-lists/` — what the next test will cover (input)
- `style-notes.md` — Claude's evolving notes on your teacher's style (auto-updated)
- `generated/` — practice tests + graded versions (output)
- `taken/` — optional: dump photos of your handwritten attempts here for archival

## Question mix (per generated test)

- ~30% close to homework — confidence builders
- ~50% combos of 2–3 concepts in unfamiliar setups
- ~20% harder/applied versions of homework

## Tip

The first generated test will be okay. After 2–3 past tests are in `past-tests/`, the style match gets noticeably better. Keep feeding it.
