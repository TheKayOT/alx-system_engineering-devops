# Shell
## Manpage
Most of Unix systems are managed by using Shell. Just as you need to know a minimum number of words to have a discussion in a language, you need to know a minimum number of commands to be able to easily interact with a system. Unix systems all have, sometimes with slight differences, the same set of commands. While it is not too hard to remember commands, it might be hard to remember all of their options and how exactly to use them. The solution to this is the `man command`. Let’s go through a part of the `ssh` one, as there are few elements to know to be able to read a man page:
```
NAME
ssh — OpenSSH SSH client (remote login program)

SYNOPSIS
ssh [-1246AaCfgKkMNnqsTtVvXxYy] [-b bind_address] [-c cipher_spec] [-D [bind_address:]port] [-E log_file] [-e escape_char] [-F configfile] [-I pkcs11] [-i identity_file] [-L [bind_address:]port:host:hostport] [-l login_name] [-m mac_spec] [-O ctl_cmd] [-o option] [-p port]
[-Q cipher | cipher-auth | mac | kex | key] [-R [bind_address:]port:host:hostport] [-S ctl_path] [-W host:port] [-w local_tun[:remote_tun]] [user@]hostname [command]

DESCRIPTION
ssh (SSH client) is a program for logging into a remote machine and for executing commands on a remote machine. It is intended to replace rlogin and rsh, and provide secure encrypted communications between two untrusted hosts over an insecure network. X11 connections and arbitrary TCP ports can also be forwarded over the secure channel.
```
Some tips:
- The `NAME` will summarize what the command is doing. As it is usually super short, you might want to look at DESCRIPTION (below) if it does not give clear enough information
- The `SYNOPSIS` will help you to understand the structure of the command:
    - A shell command usually have this format: `command options parameters`
    - Options inside `[]` are optional
    - The string without `[]` are mandatory
- `ssh [-1246AaCfgKkMNnqsTtVvXxYy] [-D [bind_address:]port]`
    - `ssh` is mandatory
        - `-1246AaCfgKkMNnqsTtVvXxYy` is optional
        - `-D [bind_address:]port` is optional (with `bind_address:` being itself optional within `-D [bind_address:]port`

## Commands
