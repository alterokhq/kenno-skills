# Kenno agent skill

Optional guidance for working with your team's living plans in [Kenno](https://kenno.dev). The Kenno MCP connection provides the tools and complete workflow; the skill adds reminders about collaboration, reporting evidence and safe retries.

## Connect first

Sign in to Kenno with GitHub and open **Settings → Connect an agent**. Copy the commands for Claude Code or Codex, authorize access in your browser, then use the verification prompt shown in Kenno. Each connection belongs to one person and one workspace. You do not need to connect a GitHub repository to collaborate or report agent work.

## Install the optional skill

Run in your project:

```sh
npx skills add alterokhq/kenno-skills --skill kenno-plan --agent claude-code
```

For Codex:

```sh
npx skills add alterokhq/kenno-skills --skill kenno-plan --agent codex
```

The [skills installer](https://github.com/vercel-labs/skills) also supports `--global` for a personal installation across projects. Restart your coding session after installing. You can instead copy `skills/kenno-plan/SKILL.md` into `.claude/skills/kenno-plan/` or `.agents/skills/kenno-plan/` in your project.

Installing this skill does not authorize a connection, grant repository access or start any work.

## Use it

Ask your agent to read a Kenno plan URL, publish a plan you've discussed, build a plan, or fix its failing checks. You can explicitly invoke `/kenno-plan` in Claude Code or `$kenno-plan` in Codex.

Plans remain editable while agents work. Reports stay attached to the text assigned to each run. Agent reports describe what the agent did; GitHub checks, reviews and merges provide separate verification. Final merging happens on GitHub.
