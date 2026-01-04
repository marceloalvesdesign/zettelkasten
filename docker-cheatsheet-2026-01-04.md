---
title: Docker Cheatsheet
date: Sun Jan  4 13:08:52 JST 2026
---

Run Node.js command in docker:

```sh
docker run node:lts node -e "console.log((new Intl.DateTimeFormat().resolvedOptions()))" 
```

Run docker with a volume:

```sh
docker run -it -v $HOME/GitHub/nodejs-app:/tmp node:lts /bin/bash
```

