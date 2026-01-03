---
title: Git Commit Message
date: Fri Aug 15 12:44:26 JST 2025
---

You can use a `HEREDOC` to add better commit messages directly from the terminal:

```sh
git commit -F- <<HEREDOC
feat: do something

We did the thing. And we wrote this with a blank line after the first one.
We added more text here too.
HEREDOC
```

