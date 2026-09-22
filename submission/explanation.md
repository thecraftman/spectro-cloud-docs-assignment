## Contents

| Path                           | Description                                           |
| ------------------------------ | ----------------------------------------------------- |
| `submission/assignment.md`     | The reference page, "Debug Operations in Kubernetes". |
| `submission/images/`           | Three screenshots from the test cluster.              |
| `instructions/instructions.md` | A copy of the assignment instructions.                |

## Test Method

I tested the page on a local Kubernetes cluster on Docker Desktop. The cluster has three pods in three states: `Running`, `CrashLoopBackOff`, and `ImagePullBackOff`. I issued every command on the page against this cluster with `kubectl` v1.37 and captured the real output. Readers can compare their own output with the page. I checked every command and flag against the `kubectl` v1.37 help, and I checked every link for a deprecation notice. I removed the deprecated link and updated the Resources section.

## Pull Request

The `main` branch holds the original draft without changes. The `debug-operations-in-kubernetes` branch holds the rewrite. The pull request from the branch into `main` shows every change line by line. Its description explains the reason for each change.

## Changes

- **Structure.** Each command has its own section. Every section has the same parts: a description, the syntax, an example with its real output, and the common flags. A summary table at the top links to each section.
- **Language.** The page uses simple English, the present tense, and the active voice. It addresses the reader as "you" and uses "We recommend" for recommendations based on the style guide. The rewrite fixes the spelling and grammar errors of the draft.
- **Code snippets.** The page replaces the incomplete code block of the draft. Every command has a syntax line and an example in a code block with a language tag. Every example shows its real output.
- **New content.** The page adds `kubectl describe pod`, because a pod that never starts has no logs. It also adds a table of status values, a table of `kubectl exec` error messages, the common flags with their short forms, and two warnings.
- **Images.** Three screenshots show the pod list and the two interactive `kubectl debug` sessions. The text output next to each screenshot has the same values as the picture.
- **Resources.** The plain address of a deprecated page now points to the replacement that the deprecation notice names. The "What is Kubernetes" link uses the current title of that page. Three more pages give the reader more detail.

## Style Guide

The page follows all the rules of the Spectro Cloud style guide.