# NER onboarding workspace

This folder is your **Northeastern Electric Racing (NER) software onboarding
workspace** — a home base for your Claude Code session while you get set up. It is
intentionally almost empty: the real knowledge lives in the **NER skills** that
`ner-jarvis` installed into your Claude Code, and those resolve people, repos, and
docs **live**, so nothing checked in here can go stale.

## For Claude

When working on NER software — onboarding, dev-environment setup, understanding a
repo or its code, NER conventions/docs, or figuring out who owns what and how to
escalate — reach for the installed NER skills rather than answering from memory, and
resolve people/ownership **live** rather than assuming. Use the `gh` CLI for GitHub.

## For you

Open Claude Code here and try things like:

> "Help me get started on the NER software team."
> "Walk me through setting up my dev environment."
> "What does <repo> do, and who owns it?"

`ner-jarvis doctor` checks that your skills and data sources are healthy.

## When a doc is wrong

NER's Confluence is mid-restructure, so you will hit pages that read as current and
aren't. That is worth capturing, not working around — say so, and Claude will record
it with the **ner-flag-stale** skill.

Reports stay **on your machine** (`~/.claude/ner-jarvis/stale.jsonl`). Nothing is
sent anywhere. When you're ready to share:

```bash
ner-jarvis stale list       # what you've recorded
ner-jarvis stale export     # paste-ready markdown for the team channel
```

A page counts as stale when someone could mistake it for current *and* acting on it
would be wrong. A doc describing how something was built before is history, not a
problem — leave it be.
