This main file mostly covers using 2nd identity on an existing machine. The new machine directory covers new machine setups.

To remove old mis-committed branch:

```
git switch --orphan new-main
```

Alternative ssh key from main:

```
git config core.sshCommand "ssh -o IdentitiesOnly=yes -i ~/.ssh/HMRWork42_rsa -F none"
```

Set up redirection temporarily for initial clones:

`~/.ssh/config`

```
Host HMRWork42-github
  HostName github.com
  AddKeysToAgent yes
  IdentityFile ~/.ssh/HMRWork42-rsa
```

This allow clones with `git clone git@HMRWork42-github:HMRWork42/HelloWorld`, but not pushes. Pushes requires the `git config` line about, and also editing the `url` line in `.git/config`
to revert back to standard non-redirected URL.

Found later, it is much easier to just set `GIT_SSH_COMMAND` to the same value as `core.sshCommand` during the initial clone!

`Settings` -> `Emails` -> `Keep my email addresses private` and `Block command line pushes that expose my email`
