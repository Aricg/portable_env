portable_env
============

Description: A wrapper for ssh that scp straps your custom (bash) rcfile

```
Setup: "./portable_env" -s
Usage: "/usr/bin/ss" user@some.remote.machine.net
```

Notes
=====
* If no user is give this script assumes root@some.remote.machine.net
* scp's everything in dotfiles/* to the remote machine
* call additional scripts from dotfiles/bashrc
* This script traps all files than it copies and removes them on exit
* running setup creates ~/.portable_env, symlinks dotfiles/* into ~/.portable_env and creates symlinks the script portable_env to /usr/bin/ss
* Tested on mavericks. but I'm almost certain it will run on debian/centos and their ilk


