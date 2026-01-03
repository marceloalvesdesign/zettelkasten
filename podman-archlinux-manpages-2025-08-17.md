---
title: Podman ArchLinux ManPages
date: Sun Aug 17 09:29:52 JST 2025
---

When installing archlinux with podman, and then trying to install man-pages,
and running `man ls` for example, nothing happens. This is because pacman is
not extracting the actual manpages because of a configuration option in
`/etc/pacman.conf`. We can remove all the `NoExtract` entries and run the
install command again:

Edit the pacman configuration file:

```sh
vi /etc/pacman.conf
```

Reinstall `man`:

```sh
pacman -Syu && pacman -S man-db man-pages

man ls
```

## References

- [Solved](https://bbs.archlinux.org/viewtopic.php?id=285790)


