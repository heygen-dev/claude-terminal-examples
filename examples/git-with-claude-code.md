# Git with Claude Code

Follows Step 6 of the quickstart: using Git through Claude Code. Assumes the project is a Git repository and you have made some changes (for example the ones from first-session.md).

## Prompt 1: what changed

    Summarise the uncommitted changes in this repository, file by file, in one line each.

Compare the summary with your own memory of what you did. Anything you do not recognise is worth a look before it is committed.

## Prompt 2: review before staging

    Review the uncommitted diff and list anything that should not be committed: debug output, secrets, temporary files, unrelated formatting changes. Do not stage or commit yet.

The do not stage or commit yet is deliberate. You want the list, then a decision.

## Prompt 3: clean up, if needed

    Remove the debug output you listed in FILE_NAME and leave everything else as it is.

Only if the review found something. Replace FILE_NAME with the file it named.

## Prompt 4: commit

    Stage the changes we discussed and commit them with a message in the same style as the last ten commits in this repository. Show me the message before committing.

Asking it to match the existing commit style avoids a message that looks nothing like the rest of the history. Asking to see the message first is one more approval point.

## Prompt 5: verify

    Show the last commit: message, files changed and the diff stat.

## If something went wrong

    Undo the last commit but keep the changes in the working tree.

Then go back to Prompt 2.

## Why read the diff yourself

The summary in Prompt 1 is a description of the change, not the change. A one-line summary can be accurate and still hide the one line you would have objected to. Read the diff for anything you are about to push.
