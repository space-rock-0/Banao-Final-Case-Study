# Client B, Structural Steel — FDE submission

Everything the brief asks for is in this folder. Nothing else is needed to submit.

## What to submit

| # | File | Brief requirement | Status |
|---|---|---|---|
| 1 | `case-study.pdf` | Case study, at most 6 pages plus appendix | 5 body pages + appendix on pages 6-7 |
| 2 | `client-note.pdf` | One page, non-technical, forwardable | 1 page |
| 3 | `submission-form.md` | Submission form, filled in | All 11 questions answered |
| 4 | `prototype/index.html` | Optional, only if it proves a point | Self-contained, no build step |

`*.docx` are the same three documents as editable Word files, in case the
submission needs a different format. They are not required — the PDFs are the
deliverables.

## The three deliverables in one line each

**Case study.** You cannot optimise steel you have never measured. Widen nesting
to material yield, measure the loss by replaying 40 past nests from your own
Strumis history in four weeks without cutting steel, then build a remnant-aware
Yield Advisor that a nester approves. Fixed INR 55 lakh over 16 weeks, with a
stop gate at week 4 for INR 22 lakh. Conservative case INR 1.46 crore a year.

**Client note.** One page, no jargon. What we propose, what we need from them,
what it costs, and when they see a result — written so the Cost Control engineer
can forward it to management unedited.

**Submission form.** All eleven questions, with the arithmetic shown.

## Optional: the prototype

Open `prototype/index.html` in a browser. No install, no build step, no network.

It runs the real deterministic packer from `analysis/packer.js` inside the page
and lays the same 15 synthetic parts on one 3000 × 2000 × 12 mm plate under three
capability settings, letting you switch between them.

It is deliberately **not** a nesting optimiser. It disproves the hypothesis it
was built to test: better packing returns 0.000 t, and all 0.172 t of gain comes
from logging the offcut rather than nesting more tightly. That reversal is
reported in the case study, because it changed the recommendation.

## Everything else

The build sources — the case-study HTML, the assumptions model, the packer, the
test suite — are one level up in `../`. They are included so the arithmetic is
checkable, not because they are part of the submission.