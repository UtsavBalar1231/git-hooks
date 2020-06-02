## Git change-id

This git hook adds a change-id to the commit message on commit. eg

```
commit 7be56dd17cbf45a4694a77065d20b5b62ff65aad (HEAD -> feature/third-change)
Author: Brock Noland <brock@phdata.io>
Date:   Fri Jan 18 22:01:34 2019 -0600

    Add b c back
    
    Change-Id: I6ff326dce82ba4f6c13846cd5fa1c13516a75054
````

This change id will persist across squash and unclean cherry-picks.

Install Globally

```
git config --global init.templatedir '~/.git-templates'
mkdir -p ~/.git-templates/hooks
curl -so - "https://raw.githubusercontent.com/phdata/git-hooks/master/commit-msg-add-change-id" > ~/.git-templates/hooks/commit-msg
chmod 755 ~/.git-templates/hooks/commit-msg
```
Install in a single repo
```
cd some-repo
curl -Lo .git/hooks/commit-msg "https://raw.githubusercontent.com/phdata/git-hooks/master/commit-msg-add-change-id" && chmod 755 .git/hooks/commit-msg
```

## Spotless Check Before Commit

Install in a single repo
```
cd some-repo
curl -Lo .git/hooks/pre-commit "https://raw.githubusercontent.com/phdata/git-hooks/master/pre-commit-spotless-check" && chmod 755 .git/hooks/pre-commit
```
