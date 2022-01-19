# SCP copy a file from a server


Lets assume you have [configured ssh config file](./ssh-config-file.md) and you want to copy a database backup or some other important file from a server.

It's easy to do with a following command:

```sh
scp server://home/user/backups/latest.dump ./
```

where `server` is a hostname from `~/.ssh/config`, `home/user/backups/latest.dump` is a file you want to copy and `./` is a destination(in this example it's a current folder)