# Git-TODO
Maintains a TODO list for each `git branch`.

## Usage
Save `git-todo` somewhere under PATH and invoke by `git todo`:
```
$ git todo [-e|--edit] [-c|--clear] [-v|--verify]
```

## Examples
Create a new todolist for current branch (uses `git config core.editor`):
```
$ git todo -e
```

Clear todolist for current branch:
```
$ git todo -c
```

Verify and remove invalid todolists:
```
$ git todo -v
```

## Internals
All todolists will be stored under `$HOME/.git-todo`. The directories under `$HOME/.git-todo` represents base64 encoded repo path which contains todolists.
