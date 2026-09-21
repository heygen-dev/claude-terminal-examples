# First session

Follows Steps 3 to 5 of the Claude Code quickstart: start a session, ask a question, make a change.

## Before you start

- Open a terminal in the root folder of a project you know a little about.
- Start Claude Code the way the quickstart's Step 3 shows.
- Notice which permission mode you are in; the first two prompts only read.

## Prompt 1: orient

    Describe this project in five lines: what it does, the main language, how it is run, where the entry point is, and where the tests are.

Expect it to look at the top-level files and read a few of them. If the description is wrong, say so now; correcting early is cheaper than correcting after a change.

## Prompt 2: go one level deeper

    Explain what ENTRY_POINT_FILE does, function by function, in plain language. Do not change anything.

Replace ENTRY_POINT_FILE with the file it named in Prompt 1. The explicit do not change anything keeps this a read-only step regardless of mode.

## Prompt 3: one small, reversible change

    Add a one-line comment at the top of ENTRY_POINT_FILE that states what the file does, matching the comment style already used in this project. Show me the diff before writing it.

This is the quickstart's Step 5 in miniature. Asking for the diff first shows you how it proposes edits and how approval works in your permission mode.

## After the change

- Open the file and confirm the comment matches the surrounding style.
- If the project has tests, run them; a comment should not change anything, which makes this a safe first check of the test command.
- If you want it gone, ask: Remove the comment you just added to ENTRY_POINT_FILE.
