---
name: idea-board
description: Stress-test a business, product or project idea before building it. Use when the user shares an idea and asks "is this worth building", wants a go/no-go, or wants to know which assumptions to test first.
---

# Idea board

Review an idea through three independent lenses, then give one verdict and a short test plan.
Read `lenses.md` in this folder before scoring. Be direct. A polite "maybe" helps nobody.

## Inputs

If any of these is missing, ask for it once, in one message. If the user does not answer, state your assumption and continue.

1. What is it, in one sentence?
2. Who pays, and for what outcome?
3. How will the first ten customers hear about it?
4. What does the user have to spend: money, hours per week, existing skills or audience?

## Steps

1. Restate the idea in two sentences. If you cannot, say what is unclear and stop.
2. Score the idea through each lens in `lenses.md`: Offer, Monopoly, Focus. Each gets a score from 1 to 5, the single biggest risk, and one sentence of evidence. No evidence, no score above 3.
3. List the assumptions the idea depends on. Mark each as `known` (shown by data), `likely` (reasonable but untested) or `blind` (a guess).
4. Pick the vote:
   - `build`: all three scores are 4 or higher and no `blind` assumption would kill the idea.
   - `build if`: at most one score is below 4, and you can name the exact condition.
   - `test first`: any `blind` assumption would kill the idea if wrong.
   - `pass`: any score is 2 or lower, or the user cannot reach a first customer.
5. Write the cheapest test for each `blind` assumption. Each test needs a cost in money and hours, a pass condition with a number, and a deadline.

## Output

Save the result to `idea/board.md` in the user's project when file tools are available, otherwise reply in chat. Use exactly this shape:

```
# <idea name>

Verdict: build | build if | test first | pass
One-line reason: ...

| Lens | Score | Biggest risk | Evidence |
|---|---|---|---|
| Offer | n/5 | ... | ... |
| Monopoly | n/5 | ... | ... |
| Focus | n/5 | ... | ... |

## Assumptions
| Assumption | Status | If wrong |
|---|---|---|

## Tests (cheapest first)
| Test | Cost | Pass condition | Deadline |
|---|---|---|---|

## What would change this verdict
- ...
```

## Rules

- Never invent market sizes, competitor names or prices. If you did not look it up, say it is an estimate and label it `blind`.
- Scores come from the idea as stated, not from the idea the user could have had.
- If the user disagrees, ask what evidence they have. Change a score only for new evidence, not for pressure.
- Keep the whole output under one page.
