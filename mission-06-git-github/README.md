# Mission 6 — Git and GitHub

## 1. Task / objective

Understand how Git tracks changes in a project and how GitHub supports collaboration through remote repositories, branches and Pull Requests.

The objective was to explore the basic Git workflow, create and publish a separate branch, update the root README, open a Pull Request, and understand how changes are reviewed and merged into the main branch.

## 2. Work completed

### Task 6.1 — Understand the basic Git workflow

Inspected the repository status, current branch and recent commit history using Git commands.

**Repository status:**

Command:

```bash
git status
```

Observed output:

```text
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

The working tree was clean, meaning there were no pending changes to commit. The local `main` branch was also synchronised with its remote counterpart, `origin/main`.

**Current branch:**

Command:

```bash
git branch --show-current
```

Observed output:

```text
main
```

This confirmed that the repository was initially on the `main` branch.

**Recent commit history:**

Command:

```bash
git log --oneline
```

The six most recent commits were displayed:

| Commit | Message |
|---|---|
| `9a2650d` | Build number converter and practise data representation |
| `38b6e88` | Compare compilers and interpreters |
| `4d665e5` | Document operating system and file management |
| `49d707d` | Complete Terminal and file management mission |
| `2e153b0` | Complete computer basics and IPOS mission |
| `fe3d912` | Set up Digital Detective mission structure |

**Basic Git operations:**

| Git operation | What it does in my own words |
|---|---|
| Check repository status | Shows the current branch and whether files have been modified, staged or left untracked. |
| Stage selected changes | Selects specific changes and places them in the staging area so they can be included in the next commit. |
| Create a commit | Saves the staged changes as a new snapshot in the repository's local history. |
| View commit history | Displays previous commits, their messages and other information about the project's history. |

**Difference between staging and committing:**

Staging and committing are two separate operations in Git. `git add` selects the changes that should be included in the next commit, whereas `git commit` records those staged changes in the repository's history.

A staged change is not yet a commit. It must be committed before it becomes part of the local commit history.

### Task 6.2 — Create and use a branch

Created a new branch named `update-about` using:

```bash
git switch -c update-about
```

Verified the active branch using:

```bash
git branch --show-current
```

The output confirmed that the current branch was `update-about`.

Updated the root `README.md` by replacing the previous placeholder section with a new section titled **My Learning**.

The section summarises three areas covered during the completed missions:

- **Computer fundamentals and operating systems:** Learning how hardware and software work together through the IPOS model, along with how an operating system manages processes, memory, storage and file permissions.
- **Working with the Terminal:** Becoming more comfortable with directory navigation, file management, command-line tools and absolute and relative paths.
- **Programming and data representation:** Exploring program execution, compilers and interpreters, number-system conversions and building a Python number converter.

**Inspecting and staging the change:**

Initially, `git status` showed the root `README.md` as modified but not staged.

Staged the selected file using:

```bash
git add README.md
```

Inspected the staged changes using:

```bash
git diff --cached
```

The diff confirmed that the previous placeholder section had been replaced with the new learning summary.

**Creating the commit:**

```bash
git commit -m "Add learning summary to root README"
```

Observed output:

```text
[update-about a2118cf] Add learning summary to root README
1 file changed, 6 insertions(+), 2 deletions(-)
```

**Publishing the branch:**

```bash
git push -u origin update-about
```

The push completed successfully, and the remote branch `origin/update-about` was created. The local branch was also configured to track its remote counterpart.

### Task 6.3 — Create a Pull Request

After publishing the branch, opened the GitHub repository and created a Pull Request from `update-about` into `main`.

**Pull Request details:**

| Information | Value |
|---|---|
| Pull Request number | #1 |
| Title | Add learning summary to root README |
| Source branch | `update-about` |
| Target branch | `main` |
| Changed file | `README.md` |
| Changes | 6 additions, 2 deletions |
| Final status | Merged |

The Pull Request description explained that the update adds a learning summary covering computer fundamentals, operating systems, Terminal usage, program execution and number representation.

**Merging the Pull Request:**

Used GitHub CLI to merge the Pull Request:

```bash
gh pr merge 1 --merge
```

The command completed successfully:

```text
Merged pull request light-at-nst/digital-detective-8001#1
(Add learning summary to root README)
```

The `--merge` option created a merge commit on the target branch.

Verified the Pull Request using:

```bash
gh pr view 1
```

The output confirmed that Pull Request #1 was merged and closed.

Updated its description using:

```bash
gh pr edit 1 --body "This PR adds a My Learning section to the root README, summarising what I learned about computer fundamentals, operating systems, Terminal usage, program execution and number representation during the completed missions."
```

Verified that the updated description was visible using `gh pr view 1`.

**Synchronising the local main branch:**

Switched back to the main branch:

```bash
git switch main
```

Retrieved the merged changes from GitHub:

```bash
git pull --ff-only origin main
```

Git successfully fast-forwarded the local `main` branch to the latest remote commit.

**Final repository verification:**

Used the following commands:

```bash
git status
git branch --show-current
git log --oneline --graph
```

The final status confirmed:

```text
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

The commit graph showed the merge history:

```text
*   ff3062b Merge pull request #1 from light-at-nst/update-about
|\
| * a2118cf Add learning summary to root README
|/
* 9a2650d Build number converter and practise data representation
```

The merged README update was successfully integrated into `main`.

### Task 6.4 — Build your Git command glossary

| Git operation | Command | Explanation |
|---|---|---|
| Initialise a repository | `git init` | Creates a new Git repository in the current directory. |
| Check status | `git status` | Displays the current branch and the state of tracked and untracked files. |
| Stage changes | `git add <file>` | Selects changes to be included in the next commit. |
| Commit changes | `git commit -m "message"` | Records the staged changes as a new commit in local history. |
| View history | `git log --oneline` | Displays the repository's commit history in a compact format. |
| Create or list branches | `git branch` | Lists existing branches; `git branch <name>` creates a new branch. |
| Switch branches | `git switch <branch>` | Switches the currently checked-out branch. |
| Publish changes | `git push` | Publishes local commits to the corresponding remote branch. |
| Retrieve remote changes | `git pull` | Fetches remote changes and integrates them into the current local branch. |

The repository had already been initialised during Mission 0, so `git init` was included in the glossary for reference rather than executed again.

## 3. Commands / tools used

| Command / Tool | Purpose |
|---|---|
| `git status` | Checks the current branch and the state of the working tree. |
| `git branch --show-current` | Displays the currently checked-out branch. |
| `git log --oneline` | Displays recent commits in a compact format. |
| `git switch -c update-about` | Creates and switches to the `update-about` branch. |
| `git add README.md` | Stages the root README change. |
| `git diff --cached` | Displays the changes currently in the staging area. |
| `git commit -m "message"` | Records staged changes in the local repository. |
| `git push -u origin update-about` | Publishes the new branch and sets its upstream tracking branch. |
| `gh pr merge 1 --merge` | Merges Pull Request #1 using a merge commit. |
| `gh pr view 1` | Displays information and status about Pull Request #1. |
| `gh pr edit 1 --body` | Updates the Pull Request description. |
| `git switch main` | Switches back to the main branch. |
| `git pull --ff-only origin main` | Retrieves and fast-forwards the local main branch with remote changes. |
| `git log --oneline --graph` | Displays commit history with branch and merge relationships. |
| Git | Tracks project changes and maintains commit history. |
| GitHub | Hosts the remote repository and provides collaboration features. |
| GitHub CLI (`gh`) | Allows GitHub operations, including Pull Request management, through Terminal. |

## 4. My understanding

I learned how Git tracks changes in a project and how its staging area and commit history work together.

The working directory contains the actual project files. Changes can be selected using `git add`, which places them in the staging area. Once ready, `git commit` records those selected changes in the repository's local history. Finally, `git push` publishes local commits to a remote repository.

I also learned how branches provide separate lines of development. Instead of modifying the main branch directly, I created `update-about` and made the README changes there.

A Pull Request is a proposal to merge changes from one branch into another. It provides an opportunity to inspect and discuss changes before integrating them into the main project.

In this mission, I created Pull Request #1 from `update-about` into `main` and merged it using GitHub CLI. The resulting merge commit preserved the relationship between the two branches in the commit history.

I also understood the difference between Git and GitHub. Git handles version control locally, while GitHub hosts repositories online and provides collaboration features such as Pull Requests.

Using `gh` for Pull Request management and `git` for local repository operations helped me understand how both tools work together.

## 5. Difficulties faced

No major difficulties were encountered during this mission.

One important distinction I understood was that merging a Pull Request through GitHub and merging branches directly using local Git commands are different workflows.

## 6. How I resolved them

Used GitHub CLI to manage and merge the Pull Request, then switched back to the local `main` branch and retrieved the merged changes using `git pull --ff-only`.

Verified the final repository state through Git status and the commit graph.

## 7. Evidence / files

- `README.md` — Root repository README updated with the My Learning section.
- `mission-06-git-github/README.md` — Contains the Git workflow explanations, command glossary, branch details, Pull Request information and learning notes.
- Pull Request #1 — Documents the README update and its successful merge into `main`.

**Pull Request:** [Add learning summary to root README](https://github.com/light-at-nst/digital-detective-8001/pull/1)

**Merge commit:** `ff3062b`

## 8. Commit details

**Commit message:** `Complete Git and GitHub collaboration mission`

**Push status:** Successfully committed and pushed to GitHub.
