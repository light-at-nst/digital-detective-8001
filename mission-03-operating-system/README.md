# Mission 3 — Understand the Operating System

## 1. Task / objective

Explore the operating system, running processes, storage, directory paths and file permissions. Understand the different responsibilities of an operating system and how it manages computer resources.

## 2. Work completed

### Task 3.1 — Explore your operating system

Used Terminal commands to inspect the operating system, current account, available storage and running system activity.

**Operating system information:**

| Information | Observation |
|---|---|
| Operating System | macOS |
| Version | 27.2.1 |
| Build | 26B131 |
| Current Account | [redacted] |

**Storage information:**

Used `df -h /` to inspect the storage available on the root filesystem.

| Information | Observation |
|---|---|
| Total filesystem size | 926 GiB |
| Used space | 13 GiB |
| Available space | 516 GiB |
| Capacity used | 3% |

**System activity snapshot:**

Used `top -l 1 -n 10` to observe running processes and resource usage.

| Information | Observation |
|---|---|
| Total processes | 811 |
| Running processes | 3 |
| Sleeping processes | 808 |
| Total threads | 3,860 |
| CPU user usage | 3.84% |
| CPU system usage | 9.93% |
| CPU idle | 86.21% |
| Physical memory used | 15 GB |
| Physical memory unused | 251 MB |

The output provided a snapshot of system activity, including process states, CPU usage, memory usage and other resource statistics.

### Task 3.2 — Understand processes

A process is a program that is currently executing.

Used the following command to inspect running processes:

```bash
ps -Ao pid,comm | head -n 15
```

Some of the processes observed were:

| PID | Process | Description |
|---|---|---|
| 1 | `launchd` | Manages the startup and execution of system services. |
| 104 | `logd` | Handles system logging activities. |

**Answers:**

1. **What is a process?**

   A process is a program currently being executed, with its own execution state and allocated system resources.

2. **What does the PID column represent?**

   PID stands for Process Identifier. It is a numerical identifier assigned to a running process, allowing the operating system to distinguish between different processes.

3. **Give two examples of processes that may be running on your computer.**

   `launchd` and `logd` are two examples of processes observed on the system.

### Task 3.3 — Understand paths and permissions

Navigated between the assignment repository and its Mission 3 directory to observe how the current working directory changes.

**Absolute path:**

An absolute path specifies the complete location of a file or directory starting from the filesystem root.

Example:

```text
/Users/[hidden]/Files/Coding/NST/SnAI/SnAI-Diwali-Assignment/digital-detective-8001/mission-03-operating-system/README.md
```

**Relative path:**

A relative path specifies a location with respect to the current working directory.

Assuming the current directory is the assignment repository root:

```text
mission-03-operating-system/README.md
```

**File permissions:**

Inspected the permissions of the `notes.txt` file created during Mission 2.

Command used:

```bash
ls -l mission-02-terminal/terminal-practice/notes.txt
```

Observed permission string:

```text
-rw-r--r--
```

| Permission | Meaning | Observation |
|---|---|---|
| r — Read | Allows file contents to be read. | Owner, group and others have read permission. |
| w — Write | Allows a file to be modified. | Only the owner has write permission. |
| x — Execute | Allows a file to be executed. | No execute permission is present. |

The first character (`-`) indicates that the entry is a regular file. The remaining nine characters represent permissions for the owner, group and others.

### Task 3.4 — Explain operating-system responsibilities

| OS responsibility | My explanation | Example |
|---|---|---|
| Process management | Manages running processes, allocates CPU time and controls their execution. | Running a browser and Terminal simultaneously. |
| Memory management | Allocates and manages RAM for running applications and processes. | Assigning memory to an application and reclaiming it when no longer needed. |
| Device management | Controls and coordinates hardware devices through drivers and system services. | Managing keyboard input and display output. |
| File management | Organises, stores, retrieves and manages files and directories. | Creating folders and saving documents. |
| User interface / shell | Provides an interface through which users interact with the computer. | Finder provides a graphical interface, while Terminal provides a command-line interface. |
| Security and permissions | Controls access to system resources and protects information. | User accounts and file permissions restrict access to files. |

## 3. Commands / tools used

| Command / Tool | Purpose |
|---|---|
| `sw_vers` | Displays macOS product name, version and build information. |
| `whoami` | Displays the username of the currently active account. |
| `df -h /` | Displays filesystem storage information in human-readable units. |
| `top -l 1 -n 10` | Takes a snapshot of running processes and system resource usage. |
| `ps -Ao pid,comm` | Lists running processes along with their PIDs and command names. |
| `head -n 15` | Displays the first 15 lines of the input. |
| `pwd` | Displays the current working directory. |
| `cd mission-03-operating-system` | Navigates into the Mission 3 directory. |
| `cd ..` | Moves to the parent directory. |
| `ls -l` | Displays detailed file information, including permissions. |

## 4. My understanding

An operating system acts as an intermediary between computer hardware and software. It manages system resources and provides the necessary environment for applications to run.

I learned that process management involves controlling running programs and allocating CPU time, while memory management deals with allocating and managing RAM.

Device management allows the operating system to communicate with hardware, and file management handles the organisation and storage of files and directories.

The operating system also provides interfaces such as graphical user interfaces and command-line shells. Security mechanisms and file permissions help protect resources by controlling who can access or modify them.

I also understood the difference between absolute and relative paths. Absolute paths specify the complete location of a resource, whereas relative paths describe its location in relation to the current working directory.

File permissions determine whether an owner, group or other users can read, write or execute a file.

## 5. Difficulties faced

No major difficulties.

## 6. How I resolved them

Not applicable.

## 7. Evidence / files

- `README.md` — Contains operating system information, process observations, storage details, path examples, permission analysis and explanations of OS responsibilities.
- `mission-02-terminal/terminal-practice/notes.txt` — File used for observing file permissions.

All identifying information from the system output has been excluded or redacted.

## 8. Commit details

**Commit message:** `Document operating system and file management`

**Push status:** Successfully committed and pushed to GitHub.

