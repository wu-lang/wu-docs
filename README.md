---
description: A guide on the Wu language.
---

# Getting Started

## Installing the Language

In order to get the Wu compiler you'll need to first make sure you've installed Rust. This can be done using the following, or by following the instructions on [their official website](https://rust-lang.org).

```
$ curl https://sh.rustup.rs -sSf | sh
```

You can then proceed to installing the Wu Compiler through the Github repository.

```
$ git clone https://github.com/wu-lang/wu
$ cd wu/
$ cargo install
```

Now, you should see something along the lines of the following, when running the compiler.

```text
$ wu
The Wu Compiler
- made by Niels

Usage:
  wu                # Show this message
  wu <file>         # Compile .wu file to corresponding .lua file
  wu <folder>       # Compile all .wu files in given folder
  wu clean <folder> # Removes all compiled .lua files in given folder
```

