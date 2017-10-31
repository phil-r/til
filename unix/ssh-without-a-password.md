# SSH without a password


To avoid entering password on every login to remote server you can add your public ssh key to `~/.ssh/authorized_keys`

To do so, first get your public key(usually it's `~/.ssh/id_rsa.pub`):

```sh
cat ~/.ssh/id_rsa.pub
```

Now copy it contents and on remote server run:

```sh
vi ~/.ssh/authorized_keys
```

and save the file(`:wq`)


---

More info in this article: https://www.debian.org/devel/passwordlessssh
