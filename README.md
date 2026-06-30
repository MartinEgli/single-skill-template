# single-skill-template

Production-ready template for one focused agent skill per repository.

Use this repository when you want to create a reusable skill with clear behavior,
evidence discipline, install instructions, validation, and maintainer rules.

## What This Template Gives You

- One canonical skill under `skills/example-skill/SKILL.md`
- References for method, terminology, evidence, and boundaries
- Assets for reusable output contracts
- Examples that show expected behavior
- Validation for structure, frontmatter, placeholders, empty references, and links
- Scaffold script for new skills
- Package script for a distributable `.skill` archive
- GitHub Actions workflow for pull request validation

## Quick Start

```powershell
npm install
npm run validate
npm run test
```

Create a new skill from templates:

```powershell
npm run scaffold -- sabsa-thesis
```

Package the example skill:

```powershell
npm run package
```

## Layout

```text
skills/example-skill/
  SKILL.md
  README.md
  references/
  assets/
  examples/
scripts/
templates/
tests/
```

## Design Principles

- One skill per repo by default.
- `SKILL.md` is the behavioral source of truth.
- References explain method, not hidden behavior.
- Assets provide reusable output structures.
- Examples prove expected behavior.
- Validation prevents sloppy skill drift.
- No installer complexity before usage pattern is stable.
- No generated files edited by hand.
- No domain-specific content in the generic template.

## Install

See [INSTALL.md](INSTALL.md).

## Maintain

See [CLAUDE.md](CLAUDE.md) and [CONTRIBUTING.md](CONTRIBUTING.md).

## Continuous Improvement

This skill supports an explicit feedback loop. Use /example-skill feedback to
capture lessons and /example-skill improve to propose changes. Improvements must
remain traceable, validated, committed on a feature branch, and pushed before
they become part of the released skill behavior.