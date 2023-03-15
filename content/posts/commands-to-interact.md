---
title: "Some Commands to Interact with a GNU/Linux Server"
date: 2023-03-06T23:00:59+03:00
draft: false
tags: ["GNU/Linux", "system administration", "terminal commands"]
showToc: true
# description: "Here you can find some fundamental commands to use your GNU/Linux server."
---

## Connecting to the server

To connect to the server:

```bash
ssh my_user@my_server
```

If you have a desktop environment installed on your server, you can use `-X` flag. This enables launching GUI apps from the server on your local PC. Here is an example:

```bash
ssh -X my_user@my_server
# ...auth...
nautilus
```

## Finding your way in terminal

`pwd` command shows where you are.

```bash
pwd

# /home/my_user/my_awesome_dir
```

To change directory use `cd`:

```bash
cd path-to-go
```

To list contents of a directiory:

```bash
# Basic command
ls

# Show also hidden files
ls -a

# Show detailed info
ls -l

# Show size of contents in a human-readable way
ls -lh

# The ultimate form
ls -lah
```

## Copy files

To copy files, use `cp`:

```bash
cp what-to-copy where-to-copy
```

To copy directories use `-r` parameter:

```bash
cp -r dir-to-copy where-to-copy
```

## Move and rename files

To move files use `mv`

```bash
mv what-to-move where-to-move
```

You can also use `mv` to rename files:

```bash
mv old-file-name new-name
```

## File transfer

You can use `scp` (secure copy) to transfer files between your server and your local PC.

To upload a file to the server:

```bash
scp path-of-what-to-upload my_user@my_server:where-to-upload
```

To download a file from the server:

```bash
scp my_user@my_server:what-to-download where-to-download
```


