# AGENTS.md

## Purpose

This repository contains a poorly translated English version of a Korean web novel. Your job is to create a new, improved English version that is much more natural, immersive, emotionally engaging, and pleasant to read while remaining faithful to the original translated content.

You are acting as a prose editor and rewrite agent, not as a story co-author.

Your output must go into a **new directory**, leaving the original files untouched.

---

## Primary Goal

Produce an improved chapter-by-chapter English rewrite that:

- fixes awkward grammar and unnatural sentence structure
- improves readability and flow
- makes dialogue feel natural
- increases emotional clarity, tension, and immersion
- preserves the original story events, meaning, tone, and continuity
- keeps terminology, character names, abilities, places, and relationships consistent across the whole novel

---

## Critical Character Rule: Shirone

This is one of the most important rules in this repository.

- The main character's name is **Shirone**
- Always spell the name exactly as: **Shirone**
- Shirone is **male**
- Shirone uses **he/him** pronouns

Any incorrect references such as:
- she / her / hers
- they / them / their
- feminine wording
- inconsistent gendered wording

must be corrected when referring to Shirone.

Do **not** preserve incorrect pronouns from the bad translation when it is clear the text is referring to Shirone.

Examples:
- "Shirone lowered her head" → "Shirone lowered his head"
- "They looked at Amy" → "He looked at Amy"

This rule has **highest priority**.

---

## Output Structure

Do **not** overwrite original chapter files.

Create a parallel rewritten version in: improved_translation/


Mirror the original structure exactly.

Examples:
- `chapters/0001.txt` → `improved_translation/0001.txt`
- `chapters/volume01/chapter001.md` → `improved_translation/volume01/chapter001.md`

---

## Rewrite Standard

Each rewritten chapter should read like a polished English web novel chapter.

### Improve:
- grammar
- sentence flow
- paragraph rhythm
- awkward phrasing
- repetitive wording
- stiff dialogue
- unclear transitions
- emotional flatness

### Preserve:
- plot
- meaning
- pacing
- lore
- abilities
- names
- tone
- relationships
- structure (unless minor cleanup helps)

---

## What You Must NOT Do

Do not:
- invent new plot
- add lore
- rewrite creatively beyond intent
- change who says/does what
- remove important content
- summarize instead of rewriting
- modernize tone incorrectly
- change established names
- alter Shirone’s gender/pronouns
- overwrite originals

You are editing — not rewriting the story.

---

## Style Guidelines

Target style:

- natural English
- immersive
- emotionally engaging
- smooth flow
- readable pacing

Prefer:
- strong but controlled narration
- clean dialogue
- reduced redundancy
- better transitions

Avoid:
- purple prose
- over-explaining
- slang
- tone-breaking exaggeration

---

## Naming & Consistency

Maintain strict consistency for:
- names
- places
- powers
- organizations
- ranks
- terminology

If multiple spellings exist:
- standardize intelligently

Always use:
**Shirone**

---

## Ambiguity Handling

If translation is unclear:

1. Rewrite as faithfully as possible
2. Do not invent meaning
3. Preserve ambiguity if needed
4. Log issue

Append to: improved_translation/rewrite_notes.md


Include:
- file name
- short excerpt
- issue
- decision

---

## File Processing Steps

For each chapter:

1. Read original
2. Rewrite cleanly
3. Fix Shirone pronouns
4. Preserve meaning
5. Save mirrored file in `improved_translation/`
6. Log ambiguity if needed

---

## Supported Files

Process:
- `.txt`
- `.md`

Ignore:
- binaries
- configs
- images
- unrelated scripts

---

## Chapter Order

- Follow filename order
- Preserve directory hierarchy
- Do not renumber

---

## Diff Safety Rule

Large diffs will fail.

You must keep changes small.

- Never process too many files at once
- Prefer small safe batches

---

## Batch Execution Strategy (CRITICAL)

### Batch rules

- Default: **25 chapters**
- Max: **40 chapters**
- If chapters are long: **10–20**

Never exceed 40 files per run.

---

### Batch selection logic

On each run:

1. Scan all chapter files
2. Skip files already in `improved_translation/`
3. Select next unprocessed files in order
4. Process only that batch
5. Stop

---

### End-of-run requirements

Before stopping:

- ensure files were written correctly
- ensure structure matches original
- ensure Shirone pronouns are correct
- log any ambiguities

Then STOP.

---

### DO NOT

- do entire repo in one run
- exceed batch size
- continue indefinitely

Correct behavior:
→ process batch → stop → resume next run

---

## Resume Behavior (AUTOMATION CORE)

The system must be resumable.

Before processing a file:

- if output exists → skip
- if not → process

---

### Resume rule

When rerun with SAME prompt:

- automatically continue from next unprocessed chapter
- do NOT require manual chapter ranges

---

### No overwrite rule

Never overwrite existing rewritten files unless explicitly told.

---

## Run Mode for Large Repositories

Operate in **semi-automated mode**:

- process next batch
- stop
- resume on next run

Do NOT ask user for chapter numbers.

Use repository state to track progress.

---

## Quality Bar

Each chapter must be:

- smoother
- clearer
- more engaging
- still faithful

---

## Final Deliverable

- full `improved_translation/` directory
- optional `rewrite_notes.md`

Original files untouched.

---

## Priority Order

1. Preserve meaning
2. Shirone = male, he/him
3. Improve readability
4. Maintain consistency
5. Write to new directory
6. Never overwrite originals
7. Never invent content
