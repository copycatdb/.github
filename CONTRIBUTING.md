# 🐾 Contributing to CopyCat

First off: **thank you!** Whether you're fixing a typo, adding a feature, or just opening an issue to say "this is broken and it made me sad" — you're making CopyCat better. We appreciate every contribution.

This guide applies across all CopyCat repos. Individual repos may have additional notes in their own CONTRIBUTING.md.

## 🧶 The Short Version

1. Find something to work on (or bring your own idea)
2. Fork the repo, make a branch
3. Do the thing
4. Open a PR
5. Be nice about it

That's it. Everything below is just details.

---

## 🐛 Reporting Issues

- Check if someone already reported it (we know, everyone says this, but really)
- Use the issue template if one exists
- Include reproduction steps, error messages, and your environment
- Screenshots are worth a thousand words. Logs are worth ten thousand.

## 💡 Suggesting Features

- Open a Discussion (not an Issue) for feature ideas
- Explain the problem you're solving, not just the solution you want
- "It would be cool if..." is a perfectly valid start

## 🔧 Pull Requests

1. **Fork & branch** — branch from `main`, name it something descriptive
2. **Keep it focused** — one PR, one concern. Monster PRs make reviewers cry.
3. **Write tests** — if the repo has tests, your change should too
4. **Update docs** — if you changed behavior, update the relevant docs
5. **Describe your changes** — the PR description should explain *what* and *why*

### First-time contributors

Look for issues labeled `good first issue` or `help wanted`. These are deliberately scoped to be approachable. No contribution is too small — typo fixes, doc improvements, and test additions are all genuinely valued.

---

## 🎨 Code Style

We keep it simple. Let the tools do the arguing.

| Language | Formatter | Linter |
|----------|-----------|--------|
| **Rust** | `cargo fmt` | `cargo clippy` |
| **Python** | `ruff format` | `ruff check` |
| **JavaScript/TypeScript** | `prettier` | `prettier` |

Run these before committing. CI will catch it if you don't, but it's nicer for everyone if you do.

---

## 🔄 Ideas Flow Freely

This is important enough to get its own section.

CopyCat exists in the same ecosystem as Microsoft's official SQL Server drivers and tools. We think that's great, not adversarial. Here's how we see it:

- **If Microsoft wants to adopt patterns from CopyCat** — amazing. That's literally the dream. The RowWriter trait in tabby? If that concept shows up in an official driver someday, we'll throw a party.
- **If CopyCat adopts ideas from official drivers** — also great. Good ideas don't have owners. We'll credit where we can and keep building.
- **If you work at Microsoft** (or any company) and want to contribute — welcome! Your PRs are reviewed the same as anyone else's. Good code is good code.

We don't do "us vs. them." We do "let's make SQL Server tooling better for everyone."

---

## 🐱 Cat Puns

Cat puns in commit messages, comments, and docs are welcome but absolutely not required. We won't reject a PR for insufficient feline wordplay. But if you manage to sneak a good one in, we will appreciate it.

Some past favorites:
- "fix: stop connection pool from cat-astrophic failure"  
- "feat: add purr-formance metrics endpoint"
- "docs: clarify the tail end of the migration guide"

---

## 📜 Licensing

All CopyCat projects are MIT licensed. By contributing, you agree your contributions will be licensed under MIT as well. No CLAs, no paperwork, no friction.

---

## 🤝 Code of Conduct

We have a [Code of Conduct](CODE_OF_CONDUCT.md). The gist: be kind, be helpful, don't be a jerk. Read it — it's short and has cat references.

---

## ❓ Questions?

- Open a Discussion in the relevant repo
- Tag `@tinkeringforfun` if you're stuck

Don't be shy. The only silly question is the one you didn't ask (and then spent three hours debugging alone).

---

*Happy contributing! 🐈‍⬛*
