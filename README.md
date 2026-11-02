# Simple Talk — a skimmable output style for Claude Code

Replies you can understand by skimming the colored words only.

- Plain, coworker-style language: what Claude is doing and why.
- Work reports have a **bold** headline, then a `diff` block where
  green `+` lines are done and red `-` lines are problems. The terminal
  colors these, so you see good and bad news at a glance.
- An optional *italic* side note in a quote for skippable detail.
- The question for you always comes last.
- No emojis, short lines, and an empty line between points.

## Example reply

**The login error message is done.**

```diff
+ Login page now shows an error on a wrong password
+ Added a test for the wrong-password case
+ Committed and pushed
- One old test broke after the change, fixed it
```

> *The old test expected an empty page on a wrong password.*

Should I **also lock the account** after 5 wrong tries?

## Install

```bash
mkdir -p ~/.claude/output-styles
curl -o ~/.claude/output-styles/simple-talk.md \
  https://raw.githubusercontent.com/Sanjarbek17/simple-talk-output-style/main/simple-talk.md
```

Restart Claude Code, then pick **Simple Talk** in `/output-style`.
For one project only, put the file in `<repo>/.claude/output-styles/` instead.

Edit the file freely, since it is just instructions added to Claude's system prompt.
