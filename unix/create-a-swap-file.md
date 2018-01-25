# Create a swap file


Common problem on small DO or similar instances is that one runs out of memory pretty quick, to negate this it's possible to add a swap file. Although it's not recommended on machines that use ssd.

To create a swap file of 1Gb run:

```sh
sudo fallocate -l 1G /swapfile
```

Make it readable only to root:

```sh
sudo chmod 600 /swapfile
```

Make it swap file:

```sh
sudo mkswap /swapfile
```

And enable it running:

```sh
sudo swapon /swapfile
```

Check that it worked:

```sh
sudo swapon -s
```

Voila!

---

More info in this article: https://www.digitalocean.com/community/tutorials/how-to-add-swap-on-ubuntu-14-04
