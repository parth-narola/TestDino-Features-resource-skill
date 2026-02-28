# How to Use the TestDino Feature Resource Skill

This guide explains how anyone on your team can use the `testdino-features.md` skill file with Claude to instantly find TestDino feature resources — docs, changelog, and YouTube videos.

---

## Setup (One-Time)

### Option A: Claude Code (CLI)

1. Copy `testdino-features.md` into your project's `.claude/` directory or reference it in your `CLAUDE.md`:

```
# In your CLAUDE.md, add:
See .claude/testdino-features.md for TestDino feature resource lookup.
```

2. Claude Code will automatically pick it up in every conversation within that project.

### Option B: Claude Desktop / claude.ai

1. Start a new conversation.
2. Attach `testdino-features.md` as a file, **or** paste its full contents at the start of the conversation.
3. Then ask your questions.

### Option C: Cursor / Any MCP-Compatible IDE

1. Add `testdino-features.md` to your project root or `.cursor/` rules.
2. Reference it in your rules file so the AI always has context.

---

## How to Ask Questions

Once the skill file is loaded, just ask naturally. Here are example queries and what you'll get back:

### Find a feature by name

```
User: Tell me about flaky tests
```

Returns: Feature name, description, docs link, changelog link, YouTube video (if any), and all sub-features.

### Find a feature by keyword

```
User: How do I set up Slack notifications?
```

Returns: Both Slack App (14i) and Slack Webhook (14j) features with their respective docs and the Slack YouTube video.

### Get docs for a specific integration

```
User: Jira integration
```

Returns: Jira integration description, docs link, changelog link, and YouTube video link.

### Find YouTube videos for a feature

```
User: Are there any videos for environment mapping?
```

Returns: The Environment Mapping YouTube video link + docs link.

### Ask about multiple features at once

```
User: What resources are available for CI optimization and GitHub status checks?
```

Returns: Both features with all their resources listed separately.

### Get sub-feature details

```
User: What tabs are available in test runs?
```

Returns: All 6 test run tabs (Summary, Specs & Tags, Errors, History, Configuration, Coverage) with individual docs links.

### Ask about setup or CLI

```
User: How do I upload test results using the Node.js CLI?
```

Returns: Node.js CLI feature with commands, flags, and docs link.

### Ask about pricing

```
User: What are the TestDino plans?
```

Returns: All 4 plans with pricing, limits, and docs link.

---

## Quick Reference: Keywords That Work

These keywords map directly to features. Use any of them:

| What You Want | Keywords to Use |
|---|---|
| Initial setup | `setup`, `install`, `getting started`, `onboarding` |
| Dashboard views | `dashboard`, `qa view`, `developer view` |
| Test execution results | `test runs`, `runs`, `executions` |
| Failure analysis | `errors`, `error grouping`, `stack trace` |
| AI-powered insights | `ai insights`, `why failing`, `ai categorization` |
| Test case details | `test case`, `evidence`, `screenshots`, `trace` |
| Pull request view | `pull request`, `pr`, `merge request` |
| Analytics & trends | `analytics`, `metrics`, `trends`, `flakiness` |
| Live results | `real-time`, `streaming`, `live`, `websocket` |
| Flaky test detection | `flaky`, `intermittent`, `flaky test` |
| Scheduled reports | `reports`, `pdf`, `email`, `automated reports` |
| Branch mapping | `environment mapping`, `branch mapping` |
| CI optimization | `rerun`, `rerun failed`, `cache`, `ci optimization` |
| Quality gates | `quality gate`, `status check`, `ci check`, `block merge` |
| GitHub integration | `github`, `github app`, `github actions` |
| GitLab integration | `gitlab`, `merge request` |
| Azure DevOps | `azure devops` |
| TeamCity | `teamcity` |
| Jira tickets | `jira`, `bug ticket` |
| Linear issues | `linear` |
| Slack alerts | `slack`, `slack app`, `notifications` |
| AI agent access | `mcp`, `cursor`, `claude desktop`, `ai agent` |
| Manual test management | `test management`, `manual testing`, `suites` |
| Test annotations | `annotations`, `priority`, `owner`, `notify` |
| Visual debugging | `screenshots`, `video`, `visual evidence` |
| Trace debugging | `trace`, `trace viewer`, `dom snapshot` |
| Visual regression | `visual testing`, `snapshot`, `screenshot diff` |
| Code coverage | `code coverage`, `istanbul`, `coverage` |
| CLI tools | `cli`, `nodejs`, `tdpw`, `python`, `pytest` |
| Settings | `settings`, `project settings` |
| User management | `users`, `roles`, `permissions`, `invite` |
| Plans & billing | `billing`, `pricing`, `plans` |
| Data privacy | `privacy`, `data`, `redaction`, `retention` |
| API authentication | `api key`, `token`, `pat` |
| Help | `faq`, `help`, `troubleshooting` |

---

## Available YouTube Videos

When a feature has a video, the skill returns it automatically. Here's the full list:

| Video Topic | URL |
|---|---|
| TestDino Overview Demo (2 min) | https://www.youtube.com/embed/bBwu88xWpdI |
| Environment Mapping | https://www.youtube.com/embed/oVaYPIsYrJA |
| CLI Environment Override | https://www.youtube.com/embed/2jUSi6EZEqw |
| GitHub Integration | https://www.youtube.com/embed/7DIwD68lqB4 |
| Jira / Linear Issues | https://www.youtube.com/embed/M7Hg4TpjOM8 |
| Slack Integration | https://www.youtube.com/embed/1OGY1AuIAPs |

---

## Tips

- **Be specific:** "Slack App integration" gives a more precise result than just "Slack".
- **Use feature names from the docs:** The skill file mirrors TestDino's official documentation structure.
- **Ask follow-ups:** After getting a feature, you can ask "What are the sub-features?" or "Show me the CLI commands for this."
- **Combine queries:** You can ask about multiple features in one message.
- **The skill never guesses:** If a link doesn't exist for a feature, it says so instead of making one up.

---

## Sharing With Your Team

1. Share both files:
   - `testdino-features.md` — the skill (feature-to-resource mapping)
   - `how-to-use.md` — this guide
2. Each team member loads the skill file in their Claude session (see Setup above).
3. Done — everyone can look up any TestDino feature instantly.
