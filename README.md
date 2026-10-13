# The Algorithm — a Claude skill

A skill that teaches Claude to run any process through Jon McNeill's five-step Algorithm: question every requirement, delete every possible step, simplify and optimize, accelerate cycle time, automate last. It enforces the order, which is the whole point. If you ask it to automate something, it works through the first four steps before it gets to automation, because automating a step you should have deleted just makes the wrong thing faster.

It triggers whenever something is slow, bloated, manual, or drowning in approvals. You can also ask for it by name.

## Installing

The skill is the `the-algorithm` folder: a `SKILL.md` plus two reference files.

**Claude Code:** copy the folder into your skills directory, then start a new session.

```bash
cp -R the-algorithm ~/.claude/skills/
```

**Claude.ai or the Claude desktop app** (no GitHub account needed):

1. Download **[the-algorithm.zip](https://github.com/coltonllu/the-algorithm-skill/releases/latest/download/the-algorithm.zip)**. Don't unzip it.
2. In Claude, go to **Customize → Skills**, click **+**, choose **Create skill**, then **Upload a skill**, and pick the zip.
3. Make sure the skill's toggle is on.

This needs **Settings → Capabilities → Code execution and file creation** turned on.

## Notes

The skill is written to deliver its result as a Claude Doc. Without a document connector, Claude puts the result in the conversation instead, which works fine but is less handy for sharing with a team.

It cites *The Algorithm: The Hypergrowth Formula That Transformed Tesla, Lululemon, General Motors, and SpaceX* by Jon McNeill. The skill is my own writeup of the framework, not the book's text.

This repo is a fixed copy shared for reading and downloading. Make your own copy if you want to change it.
