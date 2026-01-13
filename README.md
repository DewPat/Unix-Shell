# Unix Shell in C

## Overview
This project is a **Simple Unix-like Shell** implemented in C using low-level Unix system calls.  
The shell reads user commands from standard input, parses them, and executes them in child processes, similar to how a basic Linux shell works.

The goal of this project is to understand **process creation, command execution, and inter-process communication** at the operating system level.

---

## Features
- Custom command prompt for user interaction
- Execution of Unix commands using `fork()` and `exec()` family
- Support for command-line arguments
- Pipe (`|`) support for chaining multiple commands
- Command history tracking (only for commands executed in this shell)
- Displays execution details on shell termination:
  - Process ID (PID)
  - Execution start time
  - Total execution duration

---

## Supported Commands
The shell supports most basic Unix commands available in `/usr/bin`, such as:
- `ls`, `ls -l`, `ls -R`
- `echo <message>`
- `wc -l file`, `wc -c file`
- `grep <pattern> <file>`
- `sort`, `uniq`, `cat`
- Executing local binaries like `./a.out`, `./fib`

### Example:
```bash
cat file.txt | grep hello | wc -l
