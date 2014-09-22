portable environment
====================

Description: A wrapper for ssh that can push and use a bashrc and any other dot files or scripts you want sent ahead of you.  

```
Setup: "./portable_env" -s
Usage: "/usr/bin/cs" user@some.remote.machine.net
```

Why I made this
==============
So that I can take my bash and vim rc's with me wherever I go.

Notes
=====
* Half of the logic is at the top of dotfile/bashrc it gets copied to the remote host and used as the rcfile. 
* If no user is given this script assumes root@some.remote.machine.net
* Uses a clever trick I saw on Russell91/sshrc using xxd tar and pipes to copy files to the remote host inside the ssh command
* call additional scripts from dotfiles/bashrc
* This script traps all files than it copies and removes them on exit
* running setup creates ~/.portable_env, symlinks dotfiles/* into ~/.portable_env and symlinks the script portable_env to /usr/bin/cs
* Tested on mavericks and Fedora 
License
=======
BSD 
