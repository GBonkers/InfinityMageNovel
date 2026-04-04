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
- Any incorrect references such as:
  - she / her / hers
  - they / them / their
  - feminine wording
  - inconsistent gendered wording
  must be corrected when referring to Shirone

Do **not** preserve incorrect pronouns from the bad translation when it is clear the text is referring to Shirone.

If a sentence refers to Shirone, the rewrite must use male wording and male pronouns.

Examples:
- "Shirone lowered her head" → "Shirone lowered his head"
- "They looked at Amy" when referring to Shirone → "He looked at Amy"

This rule has very high priority.

---

## Output Structure

Do **not** overwrite original chapter files.

Create a parallel rewritten version in a new directory:

- `improved_translation/`

Preserve the original chapter organization and filenames whenever possible.

Example:

- `chapters/0001.txt` → `improved_translation/0001.txt`
- `chapters/volume01/chapter001.md` → `improved_translation/volume01/chapter001.md`

If the source files are nested, preserve that nesting inside `improved_translation/`.

---

## Rewrite Standard

Each rewritten chapter should read like a polished English web novel chapter, not like a literal machine translation.

### You must improve:

- grammar
- sentence flow
- paragraph rhythm
- awkward or repetitive phrasing
- stiff exposition
- unnatural dialogue
- unclear speaker/action transitions
- emotional flatness caused by poor wording

### You must preserve:

- plot events
- intended meaning
- scene order
- power system details
- lore
- named entities
- tone of the scene
- character relationships
- chapter structure unless minor paragraph cleanup helps readability

---

## What You Must NOT Do

Do not:

- invent new plot points
- add new lore
- add jokes or stylistic flourishes that change tone
- change who says or does what
- remove meaningful content just because it is repetitive
- summarize chapters instead of rewriting them
- modernize dialogue in a way that breaks the setting
- rewrite into a different story voice than the original seems to intend
- change established names or terms unless correcting an obvious translation inconsistency
- alter Shirone's gender or pronouns
- overwrite original files

You are editing and refining, not reauthoring.

---

## Style Guidelines

The rewritten prose should be:

- clear
- natural
- immersive
- emotionally engaging
- easy to read
- consistent in tone

Aim for prose that feels like a good English web novel translation.

### Preferred style traits

- natural English sentence flow
- stronger emotional delivery where the original clearly intends emotion
- cleaner dialogue tags and action beats
- reduced redundancy when the original wording is clumsy
- vivid but controlled narration
- better transitions between thoughts, actions, and speech

### Avoid

- purple prose
- excessive embellishment
- slang that feels out of place
- overexplaining obvious actions
- changing pacing too much
- dramatic exaggeration not supported by the scene

---

## Naming and Terminology Consistency

Maintain strict consistency for:

- character names
- locations
- spells
- abilities
- organizations
- titles
- ranks
- technical or magical terminology

If the original translation uses multiple spellings for the same name or term, standardize to the most likely correct form based on context and existing repository conventions.

Priority example:
- Use **Shirone**, not Sirone or Shiron or any other variation

If unsure, prefer the most frequently used correct canonical form already established in the rewritten files.

---

## Ambiguity Handling

Sometimes the original translation may be too broken or ambiguous to confidently rewrite.

When that happens:

1. Make the **best faithful rewrite possible**
2. Do **not** invent facts
3. If needed, preserve some ambiguity rather than making up a precise meaning
4. Add a note to a log file documenting the uncertain line

Create or append to:

- `improved_translation/rewrite_notes.md`

For each unclear issue, note:
- chapter filename
- short quoted excerpt
- why it was ambiguous
- what choice was made

Keep notes brief.

---

## File-by-File Process

For each chapter file:

1. Read the original chapter carefully
2. Rewrite it into polished English
3. Correct Shirone references to **Shirone / he / him / his**
4. Preserve story meaning and continuity
5. Save the rewritten result to the matching path under `improved_translation/`
6. If needed, append ambiguity notes to `improved_translation/rewrite_notes.md`

---

## Batch Execution Strategy

This repository contains many chapters. Process them incrementally and safely.

### Preferred approach

Work in batches, not in a single giant uncontrolled rewrite.

Suggested batch sizes:
- 10 chapters at a time
- 25 chapters at a time
- one volume at a time if files are already grouped cleanly

After each batch:
- verify output files were created correctly
- verify filenames and directories match source structure
- spot-check consistency of names and pronouns
- continue to next batch

### Important

Do not stop after one file unless explicitly told to do so.
Continue through the repository chapter by chapter until all supported files are processed.

If execution limits interrupt progress, continue from the last completed chapter in the next run.

---

## Idempotence / Resume Behavior

The agent should be resumable.

Before rewriting a chapter:
- check whether the corresponding output file already exists in `improved_translation/`

If it already exists:
- skip it unless explicitly instructed to overwrite or refresh existing rewritten chapters

This allows long-running work to resume safely.

---

## Supported File Types

Process chapter files with likely text content, such as:

- `.txt`
- `.md`

Ignore files that are clearly:
- config files
- binaries
- images
- scripts unrelated to chapter content
- metadata unless needed for chapter order

---

## Chapter Order

If filenames imply chapter order, preserve that order.

If chapters are stored in multiple directories, preserve their relative organization.

Do not renumber chapters unless explicitly instructed.

---

## Quality Bar

Every rewritten chapter should feel:

- smoother than the source
- more coherent than the source
- more engaging than the source
- still faithful to the source

The result should read like a corrected and polished translation, not like raw machine output.

---

## Final Deliverable

The final output of the rewrite process is:

- a complete `improved_translation/` directory containing rewritten chapters
- a `rewrite_notes.md` file for ambiguous cases, if needed

Original files must remain untouched.

---

## Agent Instruction Summary

When in doubt, follow this priority order:

1. Preserve story meaning
2. Keep Shirone male and use he/him pronouns
3. Improve readability and engagement
4. Keep names and terminology consistent
5. Write output into `improved_translation/`
6. Never overwrite originals
7. Do not invent story content
