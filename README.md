```
git switch --orphan new-main
```

```
git config core.sshCommand "ssh -o IdentitiesOnly=yes -i ~/.ssh/HMRWork42_rsa -F none"
```

`~/.ssh/config`

```
Host HMRWork42-github
  HostName github.com
  AddKeysToAgent yes
  IdentityFile ~/.ssh/HMRWork42-rsa
```

`Settings` -> `Emails` -> `Keep my email addresses private` and `Block command line pushes that expose my email`
