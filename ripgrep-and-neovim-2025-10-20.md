---
title: Ripgrep and Neovim
date: Mon Oct 20 08:50:52 JST 2025
---

Do a search with *ripgrep* and then pipe the results to *Neovim*'s quickfix list.

```sh
rg --vimgrep "foo" | nvim -q -
```

