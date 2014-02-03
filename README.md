portable_env
============

Description: A wrapper for ssh that scp straps your custom (bash) rcfile


Description: A wrapper for ssh that uses dotfiles/bashrc as your rcfile
Setup: "/usr/bin/ss" -s
Usage: "/usr/bin/ss" user@some.remote.machine.net

If no user is give this script assumes root@some.remote.machine.net
scp's everything in dotfiles/* to the remote machine
call additional scripts from dotfiles/bashrc
This script traps the files it copies and rm's them on exit

