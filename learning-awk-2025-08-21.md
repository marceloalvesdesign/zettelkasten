---
title: Learning Awk
date: Thu Aug 21 07:57:45 JST 2025
---

Started learning `awk` with this [Online Manual](https://www.gnu.org/software/gawk/manual/gawk.html).

Learned that there exists a command called `expand` that converts tabs to spaces and that there is also a dual of it called `unexpand`.

```sh
man expand
man unexpand

expand some-file
```

## Awk

`awk` takes a *pattern* and an *action*. For example:

```sh
awk '/foo/' { print $0 }' some-file # Prints all lines of the file, where the string "foo" occurs.
awk '/foo/' { print }' some-file # The default argument for print is $0.
awk '/foo/' some-file # The default action is { print }, so all of the above are equivalent.
```

