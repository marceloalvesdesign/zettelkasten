---
title: Kubectl Cheatsheet
date: Sun Jan  4 13:03:11 JST 2026
---

Port forwarding:

```sh
kubectl -n namespace port-forward podname 3001:3001
```

Secrets:

```sh
kubectl get secrets secretname -o jsonpath='{.data.SECRET}' | base64 -d
```

Scaling deployments:

```sh
kubectl -n namespace scale deployment deploymentname --replicas=0
kubectl -n namespace scale deployment deploymentname --replicas=1
```

Copying files:

```sh
kubectl -n namespace cp hello.txt podname:/tmp/hello.txt
```
