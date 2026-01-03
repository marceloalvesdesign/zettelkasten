---
title: Bash Error Handling
date: Thu Aug 21 11:52:49 JST 2025
---

```sh
set -e

# This will exit when there is a diff,
# because the error code is 1.
git diff --quiet

# This code is never reached because we set the `-e` flag.
if [ $? -eq 1 ]; then
  echo "Reached."
fi
```

Alternatives involve temporarily unsetting the flag or piping to true.

```sh
set -e

# Some code goes here.

set +e # Unset.
git diff --quiet
ret=$?
set -e # Restore.

if [ $ret -eq 1 ]; then
  echo "Reached."
fi
```

## References

- [Bash FAQ 105](https://mywiki.wooledge.org/BashFAQ/105)
- [Unofficial Bash Strict Mode](http://redsymbol.net/articles/unofficial-bash-strict-mode/)

