# Function Extraction

[![skills.sh](https://skills.sh/b/addxing/function-extraction)](https://skills.sh/addxing/function-extraction)

A Codex-compatible skill for extracting a complete feature implementation chain from a codebase and generating a technical development document with business logic, data flow, exception handling, and Mermaid diagrams.

## Install

```bash
npx skills add addxing/function-extraction
```

## Usage

After installing the skill, ask Codex to use it when you need a feature-level implementation document:

```text
Use $function-extraction to document the login flow implementation.
```

For best results, provide:

- the feature name
- the entry file, class, method, route, page, button text, or other clues
- the expected output language or documentation scope, if different from the default

If the entry point is missing, the skill guides Codex to search the codebase and ask you to confirm the correct entry before continuing.

## What It Does

This skill guides an agent to:

- confirm the target feature and entry point
- trace the implementation from entry to completion
- identify key business logic, data flow, state changes, and exception handling
- generate a technical development document using `template.md`
- include Mermaid flowcharts, sequence diagrams, and dependency graphs when useful

## Files

- `SKILL.md` - the skill instructions
- `template.md` - the output document template
- `agents/openai.yaml` - Codex UI metadata
- `LICENSE.txt` - Apache 2.0 license

## Chinese Documentation

See [README.zh.md](README.zh.md).
