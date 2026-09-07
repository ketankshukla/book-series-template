# SPEC - book-series-template

> What this repo is for, what it deliberately does not do, and what must stay
> true for a change to be correct.

## 1. Purpose

Turn a filled-in creative brief into a complete series project - website,
planning documents, publishing templates and production scaffolding - by cloning
one repository.

It exists because three series were built before it, and the fourth should not
have required rediscovering the structure.

## 2. Scope

**In scope** - a fillable client brief; a parameterised Next.js 16 site whose
components carry `{{PLACEHOLDER}}` tokens; series planning documents; Amazon KDP
metadata, pricing and launch templates; AI image prompt templates for ebook
covers, paperback wraps, branding, box sets, social media, character portraits
and thumbnails; front and back matter for fiction and non-fiction; PowerShell
DOCX assembly via Pandoc; video script templates; the full directory structure.

**Explicitly out of scope**

- **Writing the books.** That is `agentic-development-v3`. This template
  organises a series; it does not generate prose.
- **Publishing.** It produces KDP-ready assets; uploading is manual.
- **A theme system.** The site is one design, parameterised - not a framework.

## 3. Architecture

```
client-request-template.md   the brief - the only required human input
        |
        v
{{PLACEHOLDER}} substitution across:
   website/          Next.js 16, React 19, Tailwind 4, TypeScript
   planning/         series plan, book outlines, character documents
   amazon-production/ metadata, pricing, categories, keywords, launch
   image-prompts/    covers, wraps, branding, box sets, social, portraits
   front-back-matter/ fiction and non-fiction variants
   scripts/          PowerShell + Pandoc DOCX assembly
```

## 4. Invariants

1. **The brief is the only required input.** Anything the template needs that is
   not in the brief is a gap in the brief, not a question for the user.
2. **Every placeholder is substituted or the project is incomplete.** A residual
   `{{PLACEHOLDER}}` in shipped output is a defect, not a default.
3. **The website is functional before substitution.** It runs with placeholders
   visible, so the structure can be reviewed before content exists.
4. **Fiction and non-fiction have separate matter templates**, because their
   front and back matter genuinely differ and one merged template serves neither.
5. **The template captures patterns that were used**, not patterns that seemed
   sensible. Every section here came out of a completed series.

## 5. Verification

Clone, fill the brief, substitute, and confirm the site builds and no
placeholder tokens remain in generated output.

## 6. Known limitations

- **Substitution is manual or agent-driven**; there is no `init` script that
  performs it.
- **One website design.**
- **PowerShell scripts assume Windows and a local Pandoc.**
- **KDP templates track Amazon's requirements as of authoring** and will drift as
  the platform changes.

## 7. Related

Series built with these patterns: `aztec-samurai-adventures`,
`reality-without-belief`, `repetition-mother-of-mastery`, `quick-draw-series`.
