# De-Slopify

Systematically remove telltale AI writing patterns from prose. Works line-by-line through the text, not via regex or batch replacement.

## Why Use This?

LLMs produce text with statistically detectable patterns: overused vocabulary, predictable structure, filler phrases, and rhetorical tics. These patterns erode credibility and are increasingly recognizable. This skill fights against default generation tendencies.

## Installation

### Manual Installation

```bash
cd ~/.claude/skills/
ln -s ~/Developer/Personal/skill-de-slopify/skills/de-slopify de-slopify
```

## Usage

```
/de-slopify                # Clean up the most recently edited file
/de-slopify README.md      # Target a specific file
```

### When to Use

- Cleaning up AI-generated text, documentation, blog posts, READMEs
- Any writing that should not read like LLM output
- Trigger on "de-slop", "clean up this writing", "make this sound human", "remove AI patterns"

## What It Catches

- **Kill-on-sight words** — "delve", "utilize", "leverage", "facilitate", etc.
- **Filler phrases** — "It's worth noting that...", "Let's dive into...", etc.
- **Structural patterns** — "Not just X, it's Y", em dash overload, transition word chains
- **Punctuation tells** — semicolon avoidance, colon overuse, hedging chains

See `skills/de-slopify/references/pattern-checklist.md` for the full list.

## Files

```
skill-de-slopify/
├── .claude-plugin/
│   ├── plugin.json         # Plugin metadata
│   └── marketplace.json    # Marketplace listing
├── skills/
│   └── de-slopify/
│       ├── SKILL.md        # Skill definition
│       └── references/
│           └── pattern-checklist.md  # Kill-on-sight words, filler, patterns
├── README.md               # This file
└── LICENSE                 # MIT
```

## License

MIT
