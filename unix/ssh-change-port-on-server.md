# SSH change port on server


To avoid exposing ssh on default port it's possible to change it through `/etc/ssh/sshd_config` file:

```sh
sudo vi /etc/ssh/sshd_config
```

By default it has the following lines:

```
# What ports, IPs and protocols we listen for
Port 22
```

this can be changed to something like:

```
# What ports, IPs and protocols we listen for
Port 2222
```

Also it's possible to add multiple ports.

To finalize the changes ssh should be restarted:

```
sudo /etc/init.d/ssh restart
```

Now to connect to the server we can run:

```sh
ssh -p 2222 admin@192.168.0.1
```

Or this can be simplified by creating [an ssh config](./ssh-config-file.md)
