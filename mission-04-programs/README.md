# Mission 4 — How Programs Run

## 1. Task / objective

Understand how programs are executed by computers by running a simple Python program and comparing the working principles of compilers and interpreters.

The objective was to create and execute a Python program, observe its output, and understand the differences between the two approaches to program execution.

## 2. Work completed

### Task 4.1 — Create and run a Python program

Created a Python file named `hello.py` inside the Mission 4 directory.

**Program:**

```python
print("Hello from Python")
```

Executed the program using Python 3 from the Terminal:

```bash
python3 hello.py
```

**Output:**

```text
Hello from Python
```

The program executed successfully and displayed the expected message.

### Task 4.2 — Compare compiler and interpreter

| Point | Compiler | Interpreter |
|---|---|---|
| When translation / execution happens | Translates the program before execution. | Processes and executes instructions during runtime. |
| Typical output | Often produces machine code or an executable file. | Generally executes through an interpreter without producing a separate native executable. |
| One example | C (GCC / Clang) | Python (CPython) |
| One advantage | Compiled programs can execute faster after compilation. | Supports interactive execution and convenient testing. |

**Explanation:**

A compiler translates source code into another form, often machine code, before the program is executed. An interpreter processes and executes instructions at runtime rather than requiring a separately compiled executable in the traditional model. Compiled programs can offer faster execution, while interpreted environments make interactive development and testing convenient. Some programming language implementations combine both approaches.

## 3. Commands / tools used

| Command / Tool | Purpose |
|---|---|
| `cd mission-04-programs` | Navigates into the Mission 4 directory. |
| `printf` | Writes the Python source code into `hello.py`. |
| `python3 hello.py` | Executes the Python program using Python 3. |
| Python 3 | Used to interpret and execute the program. |
| Terminal | Used to create and execute the program through the command line. |

## 4. My understanding

A program consists of instructions that a computer executes to perform a particular task. These instructions are written in programming languages and need to be translated or processed into a form that the computer can execute.

A compiler translates source code into another form before execution, often producing machine code or an executable file. An interpreter processes instructions during runtime and carries out their execution.

I also learned that these approaches are not always completely separate. Some programming language implementations combine compilation and interpretation. For example, CPython compiles Python source code into bytecode before executing it using its virtual machine.

Running the `hello.py` program helped me understand how Python code is executed through the Python runtime and how its output is displayed in the Terminal.

## 5. Difficulties faced

No major difficulties.

## 6. How I resolved them

Not applicable.

## 7. Evidence / files

- `hello.py` — Contains the Python program that displays the message "Hello from Python".
- `README.md` — Contains the compiler/interpreter comparison, execution details and explanations.

## 8. Commit details

**Commit message:** `Compare compilers and interpreters`

**Push status:** Successfully committed and pushed to GitHub.
