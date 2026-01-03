---
title: Bash Pathname Expansion
date: Tue Aug 19 08:21:00 JST 2025
---

Bash Pathname Expansion refers to the Bash feature of *expanding* the `*` to a
list of files.

Example:

```sh
ls *.c
# After hitting the Tab key:
ls main.c lib.c
```

An unwanted example in a script:

```sh
# @see https://mywiki.wooledge.org/Arguments
names=Tom,Jack,*.c
IFS=,; namesArray=( $names ); unset IFS # "Works" but is BAD code. Pathname expansion will still occur.
```

The `*.c` will be expanded with the `.c` files found in the directory where the
script is being run, which is probably not what we want.
