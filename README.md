# Humanize

Rewrite or audit prose that sounds machine-written. The skill keeps the useful parts of `de-slopify`, adds a stronger audit pass, and makes `humanize` the public name.

## Use It For

- Editing README, docs, blog, or product copy
- Making AI-assisted writing sound like a person wrote it
- Cutting boilerplate without losing the point
- Auditing prose for robotic structure before rewriting it

## Install

Clone the repo and run the installer:

```bash
git clone https://github.com/cbzehner/skill-humanize.git
cd skill-humanize
./install.sh all
```

Install targets:

- `./install.sh claude` installs to `~/.claude/skills/humanize`
- `./install.sh codex` installs to `~/.codex/skills/humanize`
- `./install.sh agents` installs to `~/.agents/skills/humanize`
- `./install.sh opencode` installs to `~/.config/opencode/skills/humanize`
- `./install.sh all --copy` copies files instead of symlinking

Manual install works too: symlink or copy `skills/humanize` into your agent's skills directory.

## Agent Support

This repo uses the plain `skills/humanize/SKILL.md` layout. Claude Code and Codex also get small plugin manifests at `.claude-plugin/plugin.json` and `.codex-plugin/plugin.json`.

Other agents can read the same `SKILL.md` file. If a host does not support a frontmatter field or tool name, ignore that field and follow the workflow text.

## Credit

Harshaneel's [`humanize`](https://github.com/harshaneel/humanize) repo sharpened this skill's audit model, especially around burstiness, hedges, specificity, punctuation, and rhetorical scaffolding. This repo keeps a smaller workflow tuned for everyday docs, READMEs, messages, and public project writing.

## Layout

```text
.claude-plugin/plugin.json
.codex-plugin/plugin.json
install.sh
skills/humanize/SKILL.md
skills/humanize/references/pattern-checklist.md
tests/SCENARIOS.md
README.md
LICENSE
```

## Public Notes

These repos are public. Keep private repo names, secrets, customer data, raw logs, cookies, and absolute filesystem paths out of examples.

## License

MIT
