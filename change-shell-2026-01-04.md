---
title: Change Shell
date: Sun Jan  4 13:00:56 JST 2026
---

Changing shell after installing `bash` through `homebrew`.

```sh
chsh /opt/homebrew/bin/bash # Error.
sudo echo "/opt/homebrew/bin/bash" >> /etc/shells
chsh /opt/homebrew/bin/bash # Ok.
```

