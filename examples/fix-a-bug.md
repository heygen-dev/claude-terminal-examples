# Fix a bug or add a feature

Follows Step 7 of the quickstart. The quality of the fix depends mostly on the quality of the bug report you type, so most of this file is about the prompt.

## The bug report as a prompt

    There is a bug. Steps to reproduce: STEPS. Expected: EXPECTED. Actual: ACTUAL.
    I think the problem is somewhere in SUSPECTED_AREA but I am not sure.
    First, find the cause and explain it to me. Do not change any files yet.

Replace the ALL_CAPS placeholders. The last line matters: you want the diagnosis before the edit, so you can tell whether the fix addresses the cause or the symptom.

## Confirm the diagnosis

If the explanation makes sense, ask it to prove it:

    Write a test that reproduces the bug and fails right now. Run it and show me the failure.

If the test passes, the diagnosis was wrong; go back a step.

## Ask for the smallest fix

    Fix the cause with the smallest change that makes the new test pass. Do not touch files outside SUSPECTED_AREA unless you tell me why first. Then run the whole test suite.

## Review

    Show me the full diff and a two-line summary of what changed and why.

Read the diff. Then use the prompts in git-with-claude-code.md to commit.

## Adding a feature with the same discipline

Describe the behaviour, not the implementation:

    Add FEATURE. From the user's point of view: BEHAVIOUR. It should not change EXISTING_BEHAVIOUR.
    Before writing code, list the files you expect to change and why, and wait for me to confirm.

The list of files is your chance to catch scope creep before it happens. Confirm, or narrow it, and then let it proceed with the same test-first sequence as the bug fix.
