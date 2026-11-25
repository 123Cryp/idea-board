# idea-board

A small Claude skill that stress-tests an idea before you build it.

It reviews the idea through three lenses (Offer, Monopoly, Focus), lists the assumptions that could kill it, and gives one verdict with the cheapest tests to run first.

## What you get

- A verdict: `build`, `build if`, `test first` or `pass`.
- A score from 1 to 5 per lens, with the biggest risk and the evidence.
- A table of assumptions marked `known`, `likely` or `blind`.
- Cheapest-first tests, each with a cost, a pass condition and a deadline.

## Install

Claude Code:

1. Copy `skills/idea-board/` into your project's `.claude/skills/` folder, or into `~/.claude/skills/` to use it everywhere.
2. Ask: "Run the idea board on this idea: ..."

Claude.ai:

1. Zip the `idea-board` folder from `skills/`.
2. In Settings, open Skills and upload the zip.

## Layout

```
skills/idea-board/SKILL.md    steps, rules and output shape
skills/idea-board/lenses.md   the three lenses and score guides
examples/                     a sample board
```

## Limits

The skill reasons from what you tell it. It does not look up markets or competitors unless you give it search tools, and it marks anything it did not check as `blind`. Treat the verdict as a way to decide what to test next, not as a forecast.

## License

MIT. See `LICENSE`.
