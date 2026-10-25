# Contributing to policy-checker

Thanks for wanting to improve this skill! It's plain Markdown, so
contributions are simple. This document explains what helps most.

## How to contribute

1. **Fork** the repo and create a branch from `main`
   (e.g., `feat/coppa-clause-refinement`).
2. Make your changes.
3. Open a **Pull Request** describing: what changed, why, and which skill
   behavior it affects.

## What we're looking for

### High-value contributions

- **New jurisdiction references** — add a section to
  `policy-checker/references/jurisdictions.md` following the existing format
  (legal basis names, user rights, special clauses, supervisory authority,
  cookie/email rules). Cite the law by name so reviewers can verify.
- **New document templates** — add skeletons to
  `policy-checker/references/document-templates.md` in the same numbered
  style. Every new document type must also get a row in the decision matrix
  (`document-selection.md`) with clear "applies when / does not apply when"
  criteria.
- **Dark-pattern detection rules** — extend the refusal and gap-detection
  guidance (writing-rules.md, document-selection.md) with concrete patterns
  (e.g., new consent-wall variants, confirmshaming copy, retention tricks).
- **Example sessions** — realistic example interactions in `examples/`
  (interview → selection → excerpt of drafting). Use fictional companies and
  clearly marked placeholders. Anonymize everything.
- **Interview improvements** — questions that catch real-world gaps earlier.

### Ground rules

- **English for all skill/repo content** (generated *documents* are drafted
  in the user's language — that's runtime behavior, not repo content).
- **Never invent legal facts** in examples: placeholders only.
- **Always keep the attorney-review disclaimer** intact in templates.
- **Keep SKILL.md concise.** Push detailed material into `references/` files;
  SKILL.md should stay under ~150 lines.
- No proprietary or copied legal text — write original plain-language
  sections. Quoting short statutory concepts in your own words is fine.

## Reporting issues

Open an issue with:

- What the skill did (quote the relevant output if possible).
- What you expected.
- Phase of the workflow where it happened (interview / analysis / selection /
  drafting / checklist).

**Do not paste real personal data, real company contracts, or real client
documents in issues.**

## Review process

- PRs are reviewed for accuracy of regulatory references and consistency with
  the non-negotiable rules in `SKILL.md`.
- Changes that weaken disclaimers, allow placeholder-free invented facts, or
  tolerate dark patterns will be rejected.
