# Remove ssh passphrase prompt on macOS

Sometimes when you do some `git` commands, like `git push`, you can get `Enter passphrase for key '~/.ssh/id_rsa':`

To avoid this, run:

```
ssh-add ~/.ssh/id_rsa
```


## macOS 10.12 sierra fix
macOS 10.12 sierra update introduced changes to how ssh works, so after each reboot you need to run `ssh-add ~/.ssh/id_rsa` again. 
To avoid this add thsose lines to `~/.ssh/config`:

```
Host *
   AddKeysToAgent yes
   UseKeychain yes
   IdentityFile ~/.ssh/id_rsa
```
