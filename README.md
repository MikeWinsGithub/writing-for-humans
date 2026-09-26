# writing-for-humans

A Claude Code skill: a style guide for writing up technical work (research summaries, proofs, derivations, algorithm descriptions, reports) so that a human reader can actually follow it.

The guide itself is in [`SKILL.md`](SKILL.md).

## Install

Copy the skill into your user-level Claude Code skills directory:

```sh
git clone https://github.com/MikeWinsGithub/writing-for-humans.git
mkdir -p ~/.claude/skills/writing-for-humans
cp writing-for-humans/SKILL.md ~/.claude/skills/writing-for-humans/SKILL.md
```

Or, to make it available only inside one project, put it at `.claude/skills/writing-for-humans/SKILL.md` in that project.

Claude Code picks it up automatically when it writes technical material for a person, and you can invoke it directly with `/writing-for-humans`.

## Adapting it

The default audience line near the top of `SKILL.md` describes ARC researchers. Edit that line to describe your own readers.
