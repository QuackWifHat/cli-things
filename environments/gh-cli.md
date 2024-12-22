# GH CLI commands that make my life easier

## Remote name
### Problem:
```
fatal: 'origin' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
```

### Solution:
Check if origin is setup.
```
$ git remote -v
someName ssh://git@example.com:1234/myRepo.git (fetch)
someName ssh://git@example.com:1234/myRepo.git (push)
```
If the following is outputted, then just do:
```
$ git push someName master
```
To actually use origin do:
```
$ git remote remove someName
$ git remote add origin ssh://git@example.com:1234/myRepo.git
```

## Creating repo on cwd
```
git init

gh repo create repo-name --public --source=. --remote=upstream
```

## Deleting some repo
```
gh repo delete repo-name
```
