# Mission 0 — Create your GitHub workspace

## 1. Task / objective

Create a correctly named GitHub repository and prepare an organised folder structure for all the missions in the Digital Detective assignment.

The objective was to set up a local development workspace, verify the required tools, and publish the project as a public GitHub repository.

**Repository name:** `digital-detective-8001`

## 2. Work completed

- Created the local project directory named `digital-detective-8001`.
- Created the required folder structure for all nine missions (Mission 0–8).
- Created a separate `README.md` inside every mission directory.
- Created the root `README.md` to introduce the project and provide a mission index.
- Created the `evidence/` directory for storing screenshots and supporting outputs.
- Created the initial `number_converter.py` file inside `mission-05-numbers-data/`.
- Verified the availability of Python 3, Git and GitHub CLI.
- Initialised the local Git repository with `main` as its initial branch.
- Configured the Git author profile for the assignment.
- Created the public GitHub repository and configured its local remote using GitHub CLI instead of the GitHub Web GUI.

## 3. Commands / tools used

| Command / Tool | Purpose |
|---|---|
| `python3 --version` | Checked the installed Python version (3.14.7). |
| `git --version` | Checked the installed Git version (2.54.0, Apple Git-157). |
| `gh auth status` | Verified GitHub CLI authentication and the active account. |
| `gits Shubham` | Used my custom shell function to select the Git author profile for the assignment. |
| `git config --global init.defaultBranch main` | Configured `main` as the default initial branch for newly initialised repositories. |
| `git init` | Initialised the local Git repository. |
| `git status` | Checked the repository state and identified untracked files. |
| `rm -r .git` | Removed the initial Git metadata before reinitialising the repository with the configured default branch. |
| `gh repo create --public --source=. --remote=origin` | Created the public GitHub repository directly from the current local directory and configured the remote as `origin`. |

**Repository creation approach:**

Instead of navigating to GitHub and manually creating a repository through the Web GUI, I used GitHub CLI:

```bash
gh repo create --public --source=. --remote=origin
```

This allowed me to create the remote repository directly from my local project directory and configure the `origin` remote as part of the same operation.

## 4. My understanding

A Git repository is a project directory whose changes are tracked using Git. It contains the project's files along with the `.git` directory, which stores the repository's history and other version-control information.

GitHub provides online hosting for Git repositories, allowing projects to be published, accessed and collaborated on.

The assignment is organised into separate mission directories to keep related tasks, documentation and evidence together. This makes the repository easier to navigate and maintain.

I also learned that GitHub CLI can perform repository-management operations directly from the Terminal, avoiding the need to perform every operation through the website.

## 5. Difficulties faced

- Initially, `git status` and my custom `gits` function returned errors because the project directory was not yet a Git repository.
- The initial repository was created before configuring `main` as the default branch.

## 6. How I resolved them

- Used `git init` to initialise the local repository, after which Git commands worked correctly.
- Configured `main` as the default initial branch using `git config --global init.defaultBranch main`.
- Removed the initial `.git` directory before any commits were made and reinitialised the repository. The new repository was successfully initialised on the `main` branch.
- Ran my custom `gits Shubham` function again after initialisation to configure the assignment's Git author profile.

## 7. Evidence / files

The repository currently contains the following structure:

```text
digital-detective-8001/
├── evidence/
├── mission-00-setup/
│   └── README.md
├── mission-01-computer-basics/
│   └── README.md
├── mission-02-terminal/
│   └── README.md
├── mission-03-operating-system/
│   └── README.md
├── mission-04-programs/
│   └── README.md
├── mission-05-numbers-data/
│   ├── number_converter.py
│   └── README.md
├── mission-06-git-github/
│   └── README.md
├── mission-07-networking/
│   └── README.md
├── mission-08-final-report/
│   └── README.md
└── README.md
```

**Tools verified:**

- Python 3.14.7
- Git 2.54.0 (Apple Git-157)
- GitHub CLI (authenticated successfully)

## 8. Commit details

**Commit message:** "Set up Digital Detective mission structure".

**GitHub push status:** Successfully committed and pushed to GitHub.

