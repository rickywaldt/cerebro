When you ssh into a devpod workspace, you can run:
```
ssh -T git@github.com
``` 
to check if you’re also authenticated within the devpod.

If this is not the case, then run:
```
ssh-add —apple-load-keychain
```

To confirm, run:
```
ssh-add -l
```

You may need to run:
```
ssh-add --apple-use-keychain ~/.ssh/id_ed25519
```
