# ShivC (deprecated - see [ShivyC](https://github.com/ShivamSarodia/ShivyC) instead)

 Hey, beacause the ShivC hasn't got new updates, I've forked it, and I will provide updates later. `BUT:`It's not a C compiler. It is a compiler for a ShivC programming language, the ShivC11 dialect (the name is coming from this is the 11th fork of ShivC)
There are a few changes that will appear later:
 - `///` comment form: single line comment
 - Linux and Windows support
 - Porting to glibc

## ShivC

A small C compiler witten in Python in a couple weeks over my winter break. Generates x64 Intel-format assembly, which is then assembled and linked by `nasm` and `ld`.

Tested on OS X El Capitan 10.11.1 64-bit, Python 3.4.3, and NASM 2.11.08. The assembly uses OS X system calls, so it certainly won't run on Linux or Windows, and it may not run on other versions of OS X.

Note: ShivC is not meant to generate binaries that run quickly. The output code is at times extremely inoptimal.

### Features

See the `tests` folder for examples that compile. The `function_test.c` test is representative of the range of ShivC.

- Math
  - Operations: `+`, `-`, `*`, `/`, `%`, `++`, `--`, `&&`, `||`, `!`
  - Assignment: `=`, `+=`, `-=`, `*=`, `/=`, `%=`
  - Comparison: `==`, `!=`, `<`, `<=`, `>`, `>=`
- `int` type variables
- Control structures:
  - `if`
  - `while`
  - `for`
  - `break`
  - `continue`
- Pointers (referencing and dereferencing)
- Arrays
- Function definition and calling
- `\* ... */`-form comments
- `print` statement: `print n` outputs the integer `n` to stdout.
  - This isn't in the C spec, but I included it to facilitate outputting values from the program; ShivC is nowhere near being able to compile the stdio C libraries.

## Bugs
Oh, I use Windows (this only runs on OS X), but the project's target is to port this language to other systems.
