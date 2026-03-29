# idea-loop

A CLI for turning vague, overcomplicated, or overconfident ideas into clearer, simpler, and more actionable outputs through a structured **research → critique → subtraction → rebuild** loop.

## Modes
- `paper` — paper to practice
- `framework` — decisions to structure
- `build` — ideas to product
- `teach` — knowledge to explanation
- `strategy` — ambiguity to judgment

## Install

If developing locally:

```bash
cd /Users/home/projects/idea-loop
npm link
```

Then use globally as:

```bash
idea-loop --help
```

## Basic usage

### Paper mode
```bash
idea-loop paper --pdf ./paper.pdf --monday-morning
```

### YouTube / URL input
```bash
idea-loop strategy "https://youtu.be/t5oisJiorsU?si=K349GOZng3_6xx7G"
```

### Build mode
```bash
idea-loop build "AI workflow for digesting papers into slide decks"
```

### Save to Obsidian
```bash
idea-loop paper --pdf ./paper.pdf --obsidian
```

### Send PDF to Reader
```bash
idea-loop strategy "https://youtu.be/t5oisJiorsU?si=K349GOZng3_6xx7G" --reader
```

## Inputs
- `--file <path>`
- `--stdin`
- `--pdf <path>`
- `--url <url>` / `--URL <url>`
- bare quoted URL input is auto-detected

## Model selection
List aliases:

```bash
idea-loop --list-models
```

Examples:

```bash
idea-loop strategy "https://youtu.be/..." --model gemini-3.1-pro
idea-loop paper --pdf ./paper.pdf --model gpt-5.4
idea-loop build "..." --model minimax-m2.7
```

Default model is configured in:

```bash
~/.idea-loop/config.yaml
```

Current default:
- `gemini-3.1-pro-preview`

## Reader integration
The `--reader` flag converts the output to PDF and emails it to:

```text
your-email@library.readwise.io
```

## Config
Config file:

```bash
~/.idea-loop/config.yaml
```

Example:

```yaml
default_format: markdown
default_loops: 2
default_mode: strategy
obsidian_path: /Users/home/projects/obsidian/journal
strict_by_default: false
include_confidence: true
default_model: gemini-3.1-pro-preview
use_model_by_default: true
```

## Status
This is an evolving CLI scaffold. The core workflow exists, YouTube-aware URL loading exists, PDF input exists, model selection exists, and Reader / Obsidian integrations exist. More cleanup and refactoring are still planned.
