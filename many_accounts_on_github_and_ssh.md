# Many accounts on Github and SSH

With a single Github account your `.ssh/config` might look like:

```
Match user git host github.com
    IdentityFile ~/.ssh/id_ed25519-github
```

With multiple Github accounts you will have to become a bit creative.

```
Match user git host github-other-account
    IdentityFile ~/.ssh/id_ed25519-github-other-account
```

Then (for example):

```
git clone git@github.com-other-account:user/repo
```
