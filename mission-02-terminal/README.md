# Mission 2 — Become Comfortable with the Terminal

## 1. Task / objective

Explore the command-line interface and become comfortable with basic Terminal operations. Practise navigating directories, creating and managing files, understanding command flags and pipes, and learning how package managers work.

## 2. Work completed

### Task 2.1 — Explore basic Terminal operations

Practised the required directory and file-management operations inside the assignment repository.

| Operation / command name | Command | What it does | What I observed |
|---|---|---|---|
| Current-directory display | `pwd` | Displays the absolute path of the current working directory. | Displayed the full path ending in `digital-detective-8001`. |
| Directory listing | `ls` | Lists files and directories in the current location. | Displayed the root README, evidence directory and all mission directories. |
| Detailed listing | `ls -l` | Displays file permissions, ownership, sizes and modification timestamps. | Displayed additional information about each file and directory, including permissions and ownership. |
| Change directory | `cd ..`, `cd -` | Changes the current working directory. | `cd ..` moved to the parent directory, while `cd -` returned to the previous directory. |
| Create directory | `mkdir practice-2-1` | Creates a new directory. | Created the `practice-2-1` directory inside the repository. |
| Create empty file | `touch practice-2-1/sample.txt` | Creates an empty file if it does not already exist. | Created an empty `sample.txt` file. |
| Copy file | `cp practice-2-1/sample.txt practice-2-1/sample-copy.txt` | Creates a copy of an existing file. | Created `sample-copy.txt` while retaining the original file. |
| Move / rename file | `mv practice-2-1/sample-copy.txt practice-2-1/renamed-copy.txt` | Moves or renames a file. | Renamed the copied file to `renamed-copy.txt`. |
| Display file contents | `cat practice-2-1/sample.txt` | Displays the contents of a file in the Terminal. | Displayed the text `Digital Detective Mission 2`. |

### Task 2.2 — Practise file changes safely

Created a directory named `terminal-practice` and performed file-management operations inside it.

Created `notes.txt` and added two lines of text:

```text
This is the first line.
This is the second line.
```

Used the following commands:

```bash
printf 'This is the first line.\n' > notes.txt
printf 'This is the second line.\n' >> notes.txt
cat notes.txt
```

Created a backup using `cp` and renamed it using `mv`.

The final directory contained:

- `notes.txt`
- `notes-backup.txt`

Both files had a size of 49 bytes.

**Answers to the questions:**

1. **Difference between replacing contents and appending text:** The `>` operator replaces the existing contents of a file, whereas `>>` appends new content without removing what is already present.

2. **Difference between copying and moving:** Copying creates another instance of a file while retaining the original. Moving transfers a file to another location or renames it without keeping the original at its previous path.

3. **Information provided by the current-directory display:** The `pwd` command displays the absolute path of the directory in which the Terminal is currently operating.

4. **Purpose of directory listing:** It helps identify the files and directories present in a location, making navigation and file management easier.

### Task 2.3 — Understand flags and pipes

Compared the outputs of the following commands:

```bash
ls
ls -l
ls -lah
```

The normal listing displayed file and directory names. The detailed listing provided additional information such as permissions, ownership, file sizes and modification times.

Using `-a` included hidden files and directories such as `.git` and `.gitignore`, while `-h` displayed file sizes in human-readable units.

Also practised piping the output of one command into another:

```bash
ls -lah | head -n 5
```

The command displayed only the first five lines of the detailed listing, including its initial total line.

The pipe symbol (`|`) transfers the standard output of the command on its left to the standard input of the command on its right. In this example, `ls -lah` generates the listing and `head -n 5` displays its first five lines.

### Task 2.4 — Understand package managers

Checked the installed Homebrew version and inspected its package list.

**Homebrew version:** 7.0.6

Commands used:

```bash
brew --version
brew list
```

The package listing was divided into two categories:

- **Formulae:** Included command-line tools, libraries and other packages, such as GitHub CLI, pnpm, Python and SQLite.
- **Casks:** Included graphical applications such as Visual Studio Code, Docker Desktop and WhatsApp.

A package manager simplifies software management by automating installation, updates and removal of packages. It also handles dependencies, making it easier to install and maintain software without manually configuring everything.

No packages were installed or uninstalled during this activity.

## 3. Commands / tools used

| Command / Tool | Purpose |
|---|---|
| `pwd` | Displays the current working directory. |
| `ls` | Lists files and directories. |
| `ls -l` | Displays a detailed directory listing. |
| `ls -lah` | Includes hidden entries and human-readable file sizes. |
| `cd ..` | Moves to the parent directory. |
| `cd -` | Returns to the previous working directory. |
| `mkdir` | Creates directories. |
| `touch` | Creates empty files. |
| `printf` | Writes formatted text to files. |
| `>` | Redirects output and replaces existing file contents. |
| `>>` | Redirects output by appending to a file. |
| `cp` | Copies files. |
| `mv` | Moves or renames files. |
| `cat` | Displays file contents. |
| `head -n 5` | Displays the first five lines of input. |
| `\|` | Connects commands through a pipe. |
| `brew --version` | Displays the Homebrew version. |
| `brew list` | Lists installed Homebrew packages. |

## 4. My understanding

The Terminal provides a command-line interface through which users can interact with the operating system using commands.

Directory-navigation commands such as `pwd` and `cd` help identify and change the current working location. Commands such as `ls` provide information about files and directories.

File-management operations such as `touch`, `cp`, `mv` and `cat` make it possible to create, copy, rename and inspect files directly from the Terminal.

I also learned the difference between output redirection using `>` and `>>`. The former replaces existing file contents, while the latter appends new text.

Command flags modify how commands behave. For example, `ls -lah` combines detailed listing, hidden-file visibility and human-readable file sizes.

Pipes allow multiple commands to work together by passing the output of one command to another.

Finally, package managers such as Homebrew simplify software installation and maintenance by managing packages and their dependencies.

## 5. Difficulties faced

No major difficulties.

## 6. How I resolved them

Not applicable.

## 7. Evidence / files

- `README.md` — Contains the command reference, observations, explanations and answers.
- `practice-2-1/sample.txt` — Original practice text file.
- `practice-2-1/renamed-copy.txt` — Renamed copy of the original file.
- `terminal-practice/notes.txt` — Text file containing two appended lines.
- `terminal-practice/notes-backup.txt` — Backup copy of the text file.

## 8. Commit details

**Commit message:** `Complete Terminal and file management mission`

**Push status:** Successfully committed and pushed to GitHub.
