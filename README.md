# ABC Compiler Project

## Overview

This repository contains my **implementation of a compiler** for the **ABC (A-Better-C)** programming language. ABC is a small C-based language designed for learning how computers work at a low level. The project is part of the **Introduction (and Additions) to High-Performance Computing** course at Ulm University.  

The goal of the project is to **build your own compiler** from scratch, including components such as *lexers*, *parsers*, and simple *code generators*. Through this process, students learn how computers actually execute programs and how to code efficiently, **without unnecessary complexity**, focusing on the essential principles of computing.

This project builds on the foundations of [Michael Lehn's ABC LLVM repository](https://github.com/michael-lehn/abc-llvm) and uses the **ULM (Ulm-Lecture-Machine)**, a virtual teaching machine running on the [ice40 architecture](https://github.com/michael-lehn/ulm-on-ice). ULM allows you to see how instructions are executed and how memory and the stack are used.

---

## Learning Goals

By working on this project, you will:

- Build a compiler for a simple C-based language.  
- Implement lexers, parsers, and basic code generation.  
- Observe instruction-level execution on a virtual machine (ULM).  
- Work with memory management, including stack and heap.  
- Learn to program efficiently without unnecessary extras.  
- Gain a deeper understanding of how computers actually compute.

---

## Features

- Compile ABC source files (`*.abc`) into executables.  
- Run compiled programs in Bash.  
- Use ULM to debug and inspect execution.  
- Exercises include arithmetic, pointers, dynamic memory, linked lists, recursion, and lexical analysis.

---

## Getting Started

### Installing the ABC Compiler

To use ABC, you need to install it as described in Michael Lehn’s repository:
```bash
git clone https://github.com/michael-lehn/abc-llvm.git
cd abc-llvm
make
make install
```
This will provide the `abc` compiler on your system.  

### Compiling and Running Programs

Compile your ABC program:

    abc <file.abc>

This generates an executable, usually named `a.out`. Run it with:

    ./a.out

You can observe the execution on the ULM virtual machine to see instruction-level details.

---

## How it Works: Flow Diagram

```
  +-------------------+
  |  ABC Source File  |
  |      *.abc        |
  +-------------------+
            |
            v
  +-------------------+
  |   Student Compiler|
  | (Lexer, Parser,   |
  |  Code Generator)  |
  +-------------------+
            |
            v
  +-------------------+
  |  Executable Code  |
  |      a.out        |
  +-------------------+
            |
            v
  +-------------------+
  |      ULM VM       |
  |  (ice40 arch.)    |
  +-------------------+
            |
            v
  +-------------------+
  | Instruction-level |
  | Execution & Output|
  +-------------------+
```

This shows how ABC code is transformed into executable instructions and executed on the ULM virtual machine.

---

## References

- ABC Compiler: [https://github.com/michael-lehn/abc-llvm](https://github.com/michael-lehn/abc-llvm)  
- ULM Generator: [https://github.com/michael-lehn/ulm-generator](https://github.com/michael-lehn/ulm-generator)  
- ULM on ice40 architecture: [https://github.com/michael-lehn/ulm-on-ice](https://github.com/michael-lehn/ulm-on-ice)  

---

## License

This project is for educational purposes as part of above mentioned course. It follows the licensing terms of the original ABC and ULM repositories.

