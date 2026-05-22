# ProgrammingLanguage
# [LangName]

A programming language and bytecode virtual machine, implemented from scratch in Rust. Note: [LangName] is a temporary placeholder.

> **Status:** Early development. Currently building out the lexer and parser.
> This README describes the project's intended direction; see the milestones
> below for current progress.

## Overview

[LangName] is a dynamically-typed scripting language with a C-style syntax.
This project implements the full language pipeline from source text to
execution, built in two stages:

1. **Tree-walking interpreter** — a straightforward evaluator that walks the
   abstract syntax tree directly. Prioritizes correctness and clarity.
2. **Bytecode virtual machine** — a faster execution model that compiles the
   AST to bytecode and runs it on a stack-based VM, with its own memory
   management and garbage collection.

The goal is both to build a working language and to understand every layer of
how a language is implemented — lexing, parsing, evaluation, compilation, and
runtime — without leaning on parser generators or external language tooling.

## Why

This project is a deep dive into language implementation and systems
programming in Rust. The aim is depth over breadth: rather than a wide but
shallow feature set, the focus is on implementing the core machinery correctly
and efficiently, then extending the language with features of my own design.

## Planned Features

- Lexer and recursive-descent / Pratt parser
- Tree-walking interpreter (variables, control flow, functions, closures)
- Bytecode compiler and stack-based VM
- Hash tables, string interning, and first-class functions
- Mark-sweep garbage collector
- Custom language extensions beyond the base design *(TBD)*
- Benchmarks comparing VM execution against reference implementations

## Roadmap

- [x] Project setup (Rust toolchain, repo, CI)
- [x] Lexer — tokenize all language constructs
- [ ] Parser — expressions and statements
- [ ] Tree-walking interpreter — full base language
- [ ] Bytecode VM — compile and execute
- [ ] Garbage collection
- [ ] Custom extensions
- [ ] Benchmarks and write-up

## Building

```bash
cargo build
cargo run
cargo test
```

## Acknowledgements

The architecture follows the two-part structure described in Robert Nystrom's
*Crafting Interpreters*, reimplemented in Rust with design changes to suit the
language and Rust's ownership model.