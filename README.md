portable_env
============

Description: A wrapper for ssh that scp straps your custom (bash) rcfile

```
Setup: "./portable_env" -s
Usage: "/usr/bin/ss" user@some.remote.machine.net
```

Why I made this
==============
So that I can take my bash and vim rc's with me wherever I Go.

* Can't live without set -o vi
* I like my PS1
* set scrolloff=999
* ts=2 !!!!
* relative number
* I can have the usefull scripts where I want them (everywhere)

Notes
=====
* If no user is give this script assumes root@some.remote.machine.net
* scp's everything in dotfiles/* to the remote machine ~/.$RANDOM.nameofdotfile
* call additional scripts from dotfiles/bashrc
* This script traps all files than it copies and removes them on exit
* running setup creates ~/.portable_env, symlinks dotfiles/* into ~/.portable_env and creates symlinks the script portable_env to /usr/bin/ss
* Tested on mavericks. but I'm almost certain it will run on debian/centos and their ilk

License
=======
BSD 
