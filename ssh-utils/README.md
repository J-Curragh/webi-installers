---
title: SSH Utils
homepage: https://webinstall.dev/ssh-utils
tagline: |
  SSH Utils: Because --help takes to long.
---

## Cheat Sheet

> SSH Utils includes shortcut commands for some common tasks, including
> `ssh-pubkey`, `ssh-setpass`, and `ssh-adduser`

**ssh-pubkey**:

`ssh-pubkey` will make sure you have an SSH key, and then print it to the screen
and place it in `~/Downloads`.

```sh
ssh-pubkey
```

```txt
~/Downloads/id_rsa.johndoe.pub:

ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDTOhRnzDJNBNBXVCgkxkEaDM4IAp81MtE8fuqeQuFvq5gYLWoZND39N++bUvjMRCveWzZlQNxcLjXHlZA3mGj1b9aMImrvyoq8FJepe+RLEuptJe3md4EtTXo8VJuMXV0lJCcd9ct+eqJ0jH0ww4FDJXWMaFbiVwJBO0IaYevlwcf0QwH12FCARZUSwXfsIeCZNGxOPamIUCXumpQiAjTLGHFIDyWwLDCNPi8GyB3VmqsTNEvO/H8yY4VI7l9hpztE5W6LmGUfTMZrnsELryP5oRlo8W5oVFFS85Lb8bVfn43deGdlLGkwmcJuXzZfostSTHI5Mj7MWezPZyoSqFLl johndoe@MacBook-Air
```

**ssh-adduser**:

Many modern web programs (`npm` and `postgres`, for example) will not function
correctly if run as root. `ssh-adduser` adds user `app` with the same
**`~/.ssh/authorized_keys`** as the `root` user, with a long random password,
and gives `app` `sudo` privileges.

**ssh-setpass**:

`ssh-setpass` will ask you for your old passphrase (if any) and then for the new
one to reset it with.
