portable environment
====================

Description: A wrapper for ssh that scp straps your custom (bash) rcfile and any other dot files or scripts you want sent ahead of you.  

```
Setup: "./portable_env" -s
Usage: "/usr/bin/ss" user@some.remote.machine.net
```

Why I made this
==============
So that I can take my bash and vim rc's with me wherever I go.

* Can't live without set -o vi
* I like my PS1
* set scrolloff=999
* ts=2 !!!!
* relative number
* I can have the usefull scripts where I want them (everywhere)

Notes
=====
* Half of the logic is at the top of dotfile/bashrc look there. 
* If no user is given this script assumes root@some.remote.machine.net
* scp's everything in dotfiles/* to the remote machine ~/.$RANDOM.nameofdotfile
* call additional scripts from dotfiles/bashrc
* This script traps all files than it copies and removes them on exit
* running setup creates ~/.portable_env, symlinks dotfiles/* into ~/.portable_env and symlinks the script portable_env to /usr/bin/ss
* Tested on mavericks. but I'm almost certain it will run on debian/centos and their ilk

License
=======
BSD 
