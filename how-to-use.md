# How to Use the TestDino Resource Finder Skill

This skill dynamically searches for TestDino documentation and YouTube videos based on any feature name or keyword you provide.

---

## Setup (One-Time)

### Option A: Claude Code (CLI)

1. Copy `testdino-resource-finder-skill.md` into your project's `.claude/` directory or reference it in your `CLAUDE.md`:

```
# In your CLAUDE.md, add:
See .claude/testdino-resource-finder-skill.md for TestDino resource lookup.
```

2. Claude Code will automatically pick it up in every conversation within that project.

### Option B: Claude Desktop / claude.ai

1. Start a new conversation.
2. Attach `testdino-resource-finder-skill.md` as a file, **or** paste its full contents at the start of the conversation.
3. Then ask your questions.

### Option C: Cursor / Any MCP-Compatible IDE

1. Add `testdino-resource-finder-skill.md` to your project root or `.cursor/` rules.
2. Reference it in your rules file so the AI always has context.

---

## How It Works

Unlike a static mapping, this skill **actively searches** every time you ask:

1. **Docs Index Lookup** — Fetches `https://docs.testdino.com/llms.txt` to find matching pages.
2. **Web Search for Docs** — Searches `site:docs.testdino.com` for your query.
3. **YouTube Search** — Searches YouTube for `@testdinohq` videos matching your query.
4. **Changelog Search** — Searches `site:changelog.testdino.com` for release mentions.
5. **Verification** — Every link is verified before being returned. No guessed URLs.

This means you always get **up-to-date** results, including new pages or videos added after the skill was created.

---

## How to Ask Questions

Just ask naturally. The skill will search and return structured results.

### Find docs for a feature
```
User: Find resources for flaky tests
```
Returns: Docs links, YouTube videos, changelog entries, and related resources — all from live search.

### Search by keyword
```
User: Find resources for Slack notifications
```
Returns: Slack App and Slack Webhook docs, setup guides, and the Slack integration YouTube video.

### Search for integrations
```
User: Find resources for Jira integration
```
Returns: Jira docs page, integrations overview, Jira/Linear YouTube walkthrough.

### Search for CLI tools
```
User: Find resources for CLI upload
```
Returns: Node.js CLI docs, Python CLI docs, upload command reference.

### Search for any topic
```
User: Find resources for code coverage
```
Returns: Code coverage guide, analytics coverage, test run coverage tab, instrumentation docs.

---

## What You Get Back

Every response includes these sections:

| Section | Count | Description |
|---------|-------|-------------|
| **Documentation** | 1-5 links | Primary docs, setup guides, related pages |
| **YouTube Videos** | 0-3 links | Walkthroughs from @testdinohq channel only |
| **Changelog** | 0-3 links | Feature release mentions |
| **Related Resources** | 0-3 links | Contextual pages based on feature area |

Each link includes: Title, URL, and a one-sentence relevance explanation.

---

## Tips

- **Be specific:** "Slack App integration" gives more precise results than just "Slack".
- **Use feature names:** "GitHub status checks", "trace viewer", "environment mapping".
- **Ask for multiple features:** You can ask about several features in one message.
- **Results are live:** The skill searches the web each time, so new docs and videos are always included.
- **No fake links:** If nothing is found, the skill tells you honestly instead of guessing URLs.

---

## Optional: Combine with Static Feature Mapping

For the fastest results, you can use both files together:

1. `testdino-features.md` — Static feature-to-resource mapping (instant, offline, comprehensive)
2. `testdino-resource-finder-skill.md` — Dynamic search skill (live, always up-to-date)

Load both in your Claude session for the best of both worlds. The static mapping gives instant answers for known features, while the dynamic skill catches anything new.

---

## Sharing With Your Team

1. Share these files:
   - `testdino-resource-finder-skill.md` — the dynamic search skill
   - `testdino-features.md` — the static feature mapping (optional, for offline/fast lookup)
   - `how-to-use.md` — this guide
2. Each team member loads the skill file in their Claude session (see Setup above).
3. Done — everyone can search for any TestDino feature resource instantly.
