# Mission 8 — Final Report and Submission

## 1. Task / objective

Review the complete Digital Detective repository, verify that all mission folders and required files are present, improve the root README and confirm that the completed work is available on GitHub.

The objective was to perform a final review of the assignment, document the status of every mission and prepare the public repository for submission.

## 2. Work completed

### Step 1 — Verify the repository structure

Reviewed the repository structure on GitHub and checked that all nine mission folders were present.

| Required path | Contents / observations |
|---|---|
| `README.md` | Project introduction, mission index, topics, converter instructions and learning summary. |
| `mission-00-setup/README.md` | Repository setup and workspace structure. |
| `mission-01-computer-basics/README.md` | IPOS, hardware, software and computer-system examples. |
| `mission-02-terminal/README.md` | Terminal practice, file management, flags, pipes and package managers. |
| `mission-03-operating-system/README.md` | Operating-system information, processes, paths, storage and permissions. |
| `mission-04-programs/README.md` | Program execution and compiler/interpreter comparison. |
| `mission-04-programs/hello.py` | Python program used to practise execution. |
| `mission-05-numbers-data/README.md` | Number conversions, Python verification and text encoding. |
| `mission-05-numbers-data/number_converter.py` | Working decimal-to-binary and hexadecimal converter. |
| `mission-06-git-github/README.md` | Git workflow, command glossary, branch and Pull Request details. |
| `mission-07-networking/README.md` | Networking concepts, connectivity and DNS observations. |
| `mission-08-final-report/README.md` | Final repository review and submission details. |
| `evidence/.gitkeep` | Preserves the optional evidence directory in the repository structure. |

The Mission 2 directory also contains the files created during Terminal practice, including the sample, renamed and notes files.

The `evidence/` directory has been retained with a `.gitkeep` placeholder. Practical observations and selected outputs are documented in the relevant mission READMEs and folders. The placeholder itself is not presented as practical evidence.

### Mission completion status

| Mission | Status |
|---|---|
| Mission 0 — Create your GitHub workspace | Completed |
| Mission 1 — Know your computer | Completed |
| Mission 2 — Become comfortable with the Terminal | Completed |
| Mission 3 — Understand the operating system | Completed |
| Mission 4 — How programs run | Completed |
| Mission 5 — Numbers and data | Completed |
| Mission 6 — Git and GitHub | Completed — Pull Request #1 merged |
| Mission 7 — How computers communicate | Completed |
| Mission 8 — Final report and submission | Completed after final report commit is pushed |

### Step 2 — Update the root README

Reviewed and improved the root `README.md` so that someone visiting the repository can understand its purpose and navigate through the assignment.

The updated root README includes:

- A short introduction to the assignment.
- Links to all nine mission folders.
- A summary of the topics explored.
- Instructions for running the Python number converter.
- A learning summary covering computer fundamentals, Terminal, programming, Git and networking.
- A note explaining that each mission was documented and committed separately.

The previous placeholder learning section was replaced with actual learning notes, and the project status was updated to reflect the completed work.

### Step 3 — Complete the final mission README

Updated this README to record the final repository review, the status of every mission, the corrections made, the commit history and the repository submission information.

The final review also confirmed that the repository is public and that the completed mission commits are available on GitHub.

### Step 4 — Final checklist

| Requirement | Status |
|---|---|
| All mission folders are present, each with its own README. | Completed |
| Mission READMEs document tasks, tools, understanding and difficulties. | Completed |
| Every mission has a dedicated commit pushed to GitHub. | Completed after final push |
| IPOS, hardware, software and computer-system examples are included. | Completed |
| Terminal operations, file management, flags and pipes are covered. | Completed |
| Operating systems, processes, paths, storage and permissions are covered. | Completed |
| Compiler and interpreter are compared. | Completed |
| Number conversions include manual working and Python verification. | Completed |
| Number converter runs with at least three positive test values. | Completed |
| Git history, branch and Pull Request activity are visible. | Completed |
| LAN, MAN, WAN, DNS, router, protocols and client-server are explained. | Completed |
| Root README explains the project and how to run the converter. | Completed |
| Mission documentation and practical outputs have been reviewed for private information. | Reviewed |
| Historical Git commit metadata has been checked for personal email exposure. | Requires separate historical cleanup |
| Final changes are committed and pushed to GitHub. | Completed after final push |

### Step 5 — Submit your repository

**Repository details:**

| Information | Value |
|---|---|
| GitHub account | `light-at-nst` |
| Repository | `digital-detective-8001` |
| Visibility | Public |
| Default branch | `main` |
| Repository URL | https://github.com/light-at-nst/digital-detective-8001 |

The repository was checked on GitHub, and the latest changes from the previous missions were visible on the remote `main` branch.

**Submission status:** Repository prepared for submission through the Google Form provided by the instructor.

The repository URL must be submitted through that form. The final submission is not considered complete until the URL has been submitted.

## 3. Commands / tools used

| Command / Tool | Purpose |
|---|---|
| `git status` | Checks whether the working tree has any uncommitted changes. |
| `git branch --show-current` | Confirms the currently checked-out branch. |
| `git log --oneline --graph` | Reviews the commit history and branch/merge relationships. |
| `git reset --hard HEAD~1` | Removes the latest local commit while resetting the working tree to its parent. |
| `git reset --soft HEAD~1` | Moves the branch pointer back while keeping the previous commit's changes staged. |
| `git reset` | Unstages changes while preserving them in the working directory. |
| `git add` | Stages selected files for a commit. |
| `git commit` | Records staged changes in the repository history. |
| `git fetch origin` | Retrieves the latest remote references before updating the remote branch. |
| `git push --force-with-lease origin main` | Updates the remote `main` branch after the latest commits have been reconstructed, while checking that the remote has not unexpectedly changed. |
| `gh pr view 1` | Verifies the status and details of Pull Request #1. |
| Git | Used to track and verify changes throughout the assignment. |
| GitHub | Used to host the public repository and inspect mission files and commits. |
| GitHub CLI (`gh`) | Used to create, inspect, edit and merge the Pull Request. |
| Text editor | Used to update the root README and prepare the final mission documentation. |

## 4. My understanding

The final review helped me understand why organising and documenting a software project is important.

A repository is more useful when its files are arranged clearly and a visitor can understand the purpose of the project without having to inspect every file individually. A root README provides an introduction and navigation, while individual mission READMEs explain the work in more detail.

I also understood the importance of maintaining a meaningful Git history. Separate commits make it easier to identify the work completed in each mission, while branches and Pull Requests provide a structured way to develop and integrate changes.

Across the assignment, I explored computer fundamentals, operating systems, command-line tools, program execution, number representation and networking. The practical exercises helped me connect these concepts with the behaviour of my own computer.

Completing the final review also reinforced the importance of checking that files are actually present on the remote repository, rather than assuming that a successful local operation means the work has been published.

## 5. Difficulties faced

The final repository review identified two documentation corrections:

- The previous report stated that the `evidence/` directory had not been created. This became outdated after the directory was preserved using `.gitkeep`.
- The final report needed an explicit completion-status table for all nine missions.

The review also identified personal email exposure in historical Git commit metadata. Recreating the latest two commits does not remove email addresses from older commits.

## 6. How I resolved them

Updated the final report to reflect the actual repository structure and added a mission-by-mission completion table.

Reconstructed the latest evidence and final-report commits separately so that the evidence-directory change remains independent from the final Mission 8 report.

The historical commit-metadata privacy issue requires a separate history-wide cleanup. It is not resolved merely by recreating the latest commits.

## 7. Evidence / files

- `README.md` — Updated project overview, mission navigation, topic summary, converter instructions and learning notes.
- `mission-00-setup/README.md` through `mission-08-final-report/README.md` — Individual mission documentation.
- `mission-04-programs/hello.py` — Python execution exercise.
- `mission-05-numbers-data/number_converter.py` — Number conversion program.
- `evidence/.gitkeep` — Preserves the optional evidence directory.
- Pull Request #1 — Evidence of the `update-about` branch being merged into `main`.
- Git commit history — Records the work completed across the missions.

**GitHub repository:** https://github.com/light-at-nst/digital-detective-8001

**Pull Request:** https://github.com/light-at-nst/digital-detective-8001/pull/1

## 8. Commit details

**Evidence commit message:** `Preserve evidence directory in repository`

**Final Mission 8 commit message:** `Complete final report and verify assignment submission`

**Push status:** Successfully committed and pushed to GitHub after final verification.
