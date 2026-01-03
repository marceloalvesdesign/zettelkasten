---
title: MacOS Set Fullscreen from Terminal
date: Sat Aug 30 19:16:06 JST 2025
---

Setting *Ghostty* to fullscreen from the terminal:

```sh
osascript -e 'tell application "System Events" to tell process "Ghostty" to set value of attribute "AXFullScreen" of window 1 to true'
```

