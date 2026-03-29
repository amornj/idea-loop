# CLAUDE.md

## Project
`idea-loop` is a CLI for structured critical thinking.

The core loop is:
1. clarify
2. Feynman model
3. Socratic / grill-me pressure test
4. subtraction pass
5. rebuild
6. optionally repeat

## Main goals
- turn ambiguity into action
- separate signal from noise
- remove fake complexity
- produce useful output, not just clever output

## Current modes
- `paper`
- `framework`
- `build`
- `teach`
- `strategy`

## Important behavior
- YouTube URLs should be treated as rich sources, not raw URL strings
- strategy mode for YouTube should challenge claims, not summarize transcripts
- paper mode should focus on practice change
- output should prefer clarity, compression, and usefulness

## Current structure
- main CLI entry: `src/cli.js`
- project is intentionally still small, but will likely benefit from splitting later into:
  - arg parsing
  - source loading
  - model routing
  - templates
  - output formatting

## Style
- keep language direct
- avoid unnecessary abstraction
- avoid decorative engineering
- optimize for practical use by Amornj

## Near-term priorities
1. make non-paper modes as strong as paper mode
2. improve claim-checking / fact-vs-interpretation behavior for YouTube
3. reduce brittleness in model fallback chain
4. refactor `src/cli.js` into smaller modules when stable enough
