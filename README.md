# Why this fork exists

It adds some modifications to accommodate the needs of the work at FhG IIS.

## Branch main

It remains the same with a correction in the original link repository path and the RV32I registers table alignment.

The full reference card v1.0 can be found [here][pdf_fhg]

## Branch RV32I-Edition

It reduces the card only to the RV32I instructions, pseudo instructions and registers. It also marks out the instructions not being implemented by [Lund University][lund_course] to be used as a reference for students attending the course.

The RV32I reference card v1.0 can be found [here][pdf_fhg_rv32i]

# RISC-V Reference Card (unchanged from the [original repository][original_repo] by jameslzhu)

An unofficial reference sheet for RISC-V, the free and libre instruction set from Berkeley. ([**PDF**][pdf]).

## Compiling

Compile the root document `riscv-card.tex` with [LaTeX][latex] from your system's
standard TeX distribution (TeX Live / MikTeX):

```sh
pdflatex riscv-card.tex
```

Or with [tectonic][tectonic]:

```sh
tectonic riscv-card.tex
```

## What's inside?

- The base 32-bit ISA (RV32I), with opcode values and C-like descriptions
- Standard ISA extensions (currently only targeting the RVI20 standard profile)
- Register aliases and calling conventions
- Pseudoinstructions

Other information from the more official reference cards not specific to the
ISA, like the stack/heap memory layout, IEEE 754 floating-point layout, and size
prefixes, have been omitted.

## Why?

In RISC tradition, the assembly reference for [MIPS][mips-green-sheet]
and [RISC-V][riscv-card] fits onto a single double-sided 'Green Sheet'.

When I took [CS 61C][cs61c] at UC Berkeley in 2017, we were the first semester taught
using RISC-V, and our reference card scans from our [RISC-V textbook][patterson-hennessy]
were low-quality. I wanted a card I didn't have to squint at, so I typeset it in LaTeX.

This little reference has grown well past a double-sided page, but if you still want
the original you can print the first and last pages for the asm opcodes and calling convention.

## Contributing

This repository is not actively developed, but pull requests are accepted for
fixes, new ISA standard extensions, style improvements, or other such changes.
Please include a rebuilt PDF binary in your pull request.

Print-friendly format is preferred, when possible: legible font sizes, clean
page breaks and full letter page width usage.
(A4 support may be a good thing to check.)

Some ideas if you are truly motivated:

- RISCV64 64-bit ISA support
- Directly parsing the spec, banishing typos forever
- Build system to select binary or hex instruction opcodes

## Licensing

This work is licensed under the Creative Commons [CC-BY-4.0][CC] license.
(See LICENSE for the full text.)

In brief, feel free to use this for your own purposes, as long as you credit
me, and don't restrict others. (Again, read the license for the specifics.)

This work is adapted from the RISC-V Instruction Set Manual, available at
[https://riscv.org/specifications/][RV] and licensed
under the Creative Commons [CC-BY-4.0][CC] license.

[pdf_fhg_rv32i]: https://github.com/HElzomor/riscv-card/releases/download/v1.0_RV32I/riscv-card-rv32i.pdf
[pdf_fhg]: https://github.com/HElzomor/riscv-card/releases/download/v1.0/riscv-card.pdf
[pdf]: https://github.com/jameslzhu/riscv-card/releases/download/v1.0/riscv-card.pdf
[RV]: https://riscv.org/specifications
[CC]: https://creativecommons.org/licenses/by/4.0/
[cs61c]: https://cs61c.org/
[patterson-hennessy]: https://www.elsevier.com/books/catalog/isbn/9780128203316
[riscv-card]: https://inst.eecs.berkeley.edu/~cs61c/resources/RISCV_Green_Sheet.pdf
[mips-green-sheet]: https://inst.eecs.berkeley.edu/~cs61c/resources/MIPS_Green_Sheet.pdf
[latex]: https://www.latex-project.org/get/
[tectonic]: https://tectonic-typesetting.github.io/en-US/
[original_repo]: https://github.com/jameslzhu/riscv-card
[lund_course]: https://github.com/PalePrime/single_cycle
