---
name: example-skill
description: >
  Use this skill when a user asks for a structured expert workflow that needs
  planning, review, build guidance, evidence handling, and final quality checks
  while staying generic enough to become a domain-specific skill template.
---

# Example Skill

## Purpose

Provide a disciplined, reusable workflow for a focused domain skill. Keep the
main behavior in this file. Use references only for supporting method, terms,
and boundaries.

## When to Use

Use this skill when the user asks for:

- a structured plan
- a review against explicit criteria
- a build or implementation guide
- a final quality check
- a reusable domain workflow

## Do Not Use When

Do not use this skill when:

- the task is a simple one-line answer
- another specialized skill exactly matches the request
- the user asks for unstructured brainstorming only
- evidence cannot be assessed and the user needs high-stakes advice

## Handoffs

- Hand off explicitly when another skill owns the main decision.
- State why the handoff is needed and which part of the request this skill can
  still handle.
- Do not silently answer outside the skill boundary.

## Mandatory Rules

- Read relevant reference files before applying their method.
- Preserve user-provided facts, names, paths, commands, and error strings.
- Separate evidence from inference.
- State assumptions when they affect the result.
- Prefer concise structured outputs over long prose.
- Do not invent standards, citations, or source claims.
- Ask a question only when missing input blocks meaningful progress.
- If required input is missing and the result would be misleading, mark the
  blocker instead of inventing the answer.

## Inputs Expected

Useful inputs include:

- goal or decision to support
- audience
- constraints
- source material
- review criteria
- target output format

Proceed with reasonable assumptions when missing details are low risk.

## Modes

### /example plan

Create a short execution plan with goal, constraints, steps, risks, and outputs.
Use `assets/checklist-template.md` when a checklist helps.

### /example review

Review supplied material against explicit criteria. Use
`assets/review-matrix-template.md` for structured review results.

### /example build

Produce an implementation-ready artifact or guide. Include only necessary
context and keep decisions traceable.

### /example final-check

Run a final quality pass against the quality gates. Highlight blockers first.

## Evidence Handling

Use `references/evidence-discipline.md`.

Required distinction:

- Evidence: directly present in supplied material or cited source.
- Inference: reasoned conclusion from evidence.
- Assumption: useful but not verified.
- Gap: missing information that may change the answer.

## Output Contracts

Use assets when the user asks for structured output:

- `assets/output-template.md`
- `assets/review-matrix-template.md`
- `assets/checklist-template.md`

## Quality Gates

Before final answer, check:

- output matches requested mode
- assumptions are visible
- evidence and inference are separated
- no placeholder markers remain
- boundaries are respected
- next step is clear

## Boundaries

Use `references/boundaries.md`.

Do not provide legal, medical, financial, or security-critical conclusions as
certainty without appropriate source verification and caveats.

## Output Style

- Direct.
- Structured when useful.
- Short paragraphs.
- No decorative filler.
- Use tables only when comparison is clearer than prose.
