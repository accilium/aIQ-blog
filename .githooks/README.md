# Hooks

Enable once per clone:

```
git config core.hooksPath .githooks
```

Two provenance guards for a public repository:

- `pre-commit` — the commit author is a person, not a bot or assistant account, and the author email is a real address rather than the local hostname git substitutes when `user.email` was never set. That default publishes the name of your machine.
- `commit-msg` — the message carries no tool or assistant attribution. It should describe the change, not how it was written.

Post bylines in `_posts/*.md` frontmatter are a separate thing and unaffected: those are deliberate, published author credits.
