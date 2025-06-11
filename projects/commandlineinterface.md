---
layout: project
type: project
image: img/CL.png
title: "Command Line Interpreter"
date: 2025-02-09
published: true
labels:
  - Ubuntu
  - C++
  - Unix/Linux
summary: "Built a Unix-style shell in C++ with support for interactive and batch modes, concurrent command execution, signal handling, command history, and I/O redirection. Gained hands-on experience with process control, memory management, and terminal interaction."
---
LopeShell is a Unix/Linux command line interpreter my partner Hunter and I developed in C++ as part of a systems programming course at Grand Canyon University. The shell supports both interactive and batch modes. In interactive mode, it presents a prompt (lopeShell>) where users can input and execute commands. Multiple commands can be separated by semicolons and executed concurrently using POSIX system calls like fork() and execvp(). Batch mode reads commands from a file and executes them line-by-line. The shell includes built-in commands such as exit and handles termination signals like CTRL+C (SIGINT) for graceful shutdown. LopeShell was designed to simulate the behavior of real-world shells while maintaining a clean and modular architecture.

My responsibilities included developing the input parsing logic, implementing process control through child forking, and handling concurrent execution of multiple commands. I wrote functions to tokenize user input, manage dynamic memory allocation, and execute commands using system-level calls. In the second phase of development, I enhanced the shell by adding features like command history navigation with arrow keys, I/O redirection (<, >, >>), background task execution using &, and improved terminal interactions. I also added support for parsing special symbols and implemented signal handling for a smoother user experience. This second iteration brought the shell closer to the behavior of modern command line interfaces.

From this project, I gained significant experience with low-level systems programming in C++, deepened my understanding of how Unix shells function, and developed a strong grasp of process management, memory handling, and file descriptor manipulation. I also became more comfortable debugging concurrency issues and structuring complex programs in modular functions. Working on this shell taught me the importance of graceful termination, resource management, and how thoughtful user interface design (even in a terminal) can enhance usability. Overall, LopeShell was a valuable deep-dive into the operating system's interface layer and gave me hands-on experience building from scratch what most users take for granted.

You can view the [source code here](https://github.com/HunterCay/CST-315/blob/main/ImprovedCLI.cpp).
