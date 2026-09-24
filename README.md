# ner-jarvis-context

The **NER software onboarding workspace** — your home base while you get set up on
the software team. `ner-jarvis` clones this repo, opens Claude Code here, and
installs the NER skills and data sources.

It stays minimal on purpose: the skills resolve people, repos, and docs live, so
nothing here can go stale. Claude's instructions are in [`CLAUDE.md`](CLAUDE.md).

## Try it

> "Help me get started on the NER software team."
> "Walk me through setting up my dev environment."
> "What does <repo> do, and who owns it?"

`ner-jarvis doctor` checks that your skills and data sources are healthy.

## When a doc is wrong

NER's Confluence is mid-restructure, so you'll hit pages that read as current and
aren't. Tell Claude and it records the page with the **ner-flag-stale** skill, or run
`ner-jarvis stale add` yourself. Reports stay on your machine
(`~/.claude/ner-jarvis/stale.jsonl`) — nothing is sent anywhere.

```bash
ner-jarvis stale list       # what you've recorded
ner-jarvis stale export     # paste-ready markdown for the team channel
```

A page counts as stale when someone could mistake it for current *and* acting on it
would be wrong.
