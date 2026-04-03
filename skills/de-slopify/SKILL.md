---
name: de-slopify
description: Remove AI writing patterns from prose to make it sound authentically human.
  Use when cleaning up AI-generated text, documentation, blog posts, READMEs, or any
  writing that should not read like LLM output. Trigger on "de-slop", "clean up this
  writing", "make this sound human", "remove AI patterns", or "this reads like AI wrote it".
allowed-tools: Read, Edit, Write, Grep
---

# /de-slopify

Systematically remove telltale AI writing patterns from prose. Works line-by-line through the text, not via regex or batch replacement.

## Why This Exists

LLMs produce text with statistically detectable patterns: overused vocabulary, predictable structure, filler phrases, and rhetorical tics. These patterns erode credibility and are increasingly recognizable. This skill fights against default generation tendencies.

## Process

1. **Read the full text** before making any changes
2. **Scan for patterns** from the reference checklist (see below)
3. **Consider each substitution in context** — don't apply replacements mechanically. A word that's fine once may be a tell when used four times. Prefer minimal write operations (read, process mentally, write back in one pass) over dozens of sequential edits
4. **Vary your fixes** — don't replace every em dash with a semicolon. Mix: comma, period, parenthetical, restructured sentence
5. **Read the result aloud** (mentally). Does it sound like a specific human wrote it, or like a helpful assistant?

## Pattern Checklist

See [references/pattern-checklist.md](references/pattern-checklist.md) for the full list of kill-on-sight words, filler phrases, structural patterns, and punctuation tells.

## What NOT to Do

- Don't make the text bland. De-slopifying means making it sound like a *specific human*, not stripping all personality.
- Don't replace every instance mechanically. "Leverage" is fine once if used correctly; it's a tell when used four times in two paragraphs.
- Don't add your own AI patterns while fixing others. Watch for self-slopification.
- Don't change technical terms, code, or quoted material.

## Output

After de-slopifying, briefly note what you changed (e.g., "Replaced 8 kill-on-sight words, removed 3 filler openers, broke up 2 em-dash clusters, varied paragraph lengths").
