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

Install

```
cd some-repo
curl -so - "https://raw.githubusercontent.com/phdata/git-hooks/master/commit-msg-add-change-id" > .git/hooks/commit-msg && chmod 755 .git/hooks/commit-msg
```
