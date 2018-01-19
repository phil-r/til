# SSH config file


To avoid typing complex commands to ssh to your servers you can utilize `~/.ssh/config`

Imagine you connect to your server using following command:

```sh
ssh -p 2222 admin@192.168.0.1
```

This command can be simplified using `~/.ssh/config`. To do so, we need to create config file and put our data into it:

```sh
vi ~/.ssh/config
```

Now we can use following template:

```
# This is an example of `~/.ssh/config` file
Host example
  HostName 192.168.0.1
  Port 2222
  User admin
```

and save the file(`:wq`)

Now to connect to the server we can simply run:

```sh
ssh example
```

---

More info can be found here: https://linux.die.net/man/5/ssh_config
