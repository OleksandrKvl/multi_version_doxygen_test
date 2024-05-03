Should we deploy not from a branch but from an action?
It's not clear.
The problem is that for
- `git-main` and maybe `PR<NUMBER>` we always want to override the whole
    directory.
- but for others we want `keep_files: true`.
