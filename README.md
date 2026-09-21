# Claude terminal examples

*Unofficial community examples for Claude Code in the terminal. Not affiliated with Anthropic. All trademarks belong to their owners.*

These claude terminal examples are session walkthroughs, not code. Claude Code is driven by what you type at it, so the reusable artifact is a sequence of prompts with a note on what to expect after each one. The three files follow the shape of Anthropic's [quickstart](https://code.claude.com/docs/en/quickstart): a first session (Steps 3 to 5), using Git with Claude Code (Step 6), and fixing a bug or adding a feature (Step 7). Install and log in first using the [terminal guide for new users](https://code.claude.com/docs/en/terminal-guide) or the quickstart's Steps 1 and 2; the walkthroughs do not repeat the install command because it depends on your operating system and may change.

> Rather have a website or an Expo app built for you from a prompt? [Try Begin.sh - turn a prompt or a URL into a downloadable static site or Expo app](https://begin.sh?utm_source=github&utm_medium=ugc&utm_campaign=claude-terminal-examples&utm_content=readme-top&utm_term=tier-r). No terminal, hosting, backend or auth.

## Files

| Path | What it shows |
| --- | --- |
| examples/first-session.md | a first session: orient in a project, ask questions, make one small change |
| examples/git-with-claude-code.md | using Git through Claude Code: review, stage, commit, without losing track of what changed |
| examples/fix-a-bug.md | a reproducible bug report as a prompt, and how to keep the fix small |

## Setup

Nothing to export. You need Claude Code installed and logged in (quickstart Steps 1 and 2), and a project folder to open it in. Before the first walkthrough, read the [permissions](https://code.claude.com/docs/en/permissions) and [permission modes](https://code.claude.com/docs/en/permission-modes) pages once, so you know what it will ask before editing or running anything.

## First session

`examples/first-session.md` starts in a project directory and follows the quickstart's Steps 3 to 5. The prompts ask Claude Code to describe the project, explain one file, and then make one small, reversible change. The point of ordering it this way is that the first two prompts read only, so you can watch how it explores before you give it permission to write. The file ends with what to check after the change.

## Git with Claude Code

`examples/git-with-claude-code.md` covers Step 6. The prompts ask for a summary of uncommitted changes, a review of the diff for anything that should not be committed, and then a commit with a message that matches the project's style. It also shows how to ask for the change to be undone if the review turns something up. A short section explains why it is worth reading the diff yourself even when the summary looks right.

## Fix a bug

`examples/fix-a-bug.md` is Step 7 turned into a template. It shows how to write the bug as a prompt: steps to reproduce, expected and actual behaviour, where you think the problem is, and what not to touch. Then it walks through asking for the cause before the fix, keeping the fix to the smallest change, and running the project's tests. The last section is about adding a feature with the same discipline: describe the behaviour, not the implementation.

## When to use Begin.sh instead

All three walkthroughs assume an existing project you will keep working in. If the job is produce a website or a mobile app from a description, there is no project yet and no reason to set one up. [Try Begin.sh - turn a prompt or a URL into a downloadable static site or Expo app](https://begin.sh?utm_source=github&utm_medium=ugc&utm_campaign=claude-terminal-examples&utm_content=readme-top&utm_term=tier-r). Describe it or paste a URL to clone, download the zip, and host it anywhere; no hosting, backend or auth is bundled, so nothing needs a terminal afterwards.
