# Git hooks

## Config your git

### Global
You can make git use your centralized hooks, like this:

    git config --global core.hooksPath /path/to/my/centralized/hooks
or,
edit `~/.gitconfig`, by adding a line in `[core]` like this:

    [core]
          hooksPath = /path/to/hooks


### Per repo
You can set per repo config, like this:

    git config core.hooksPath /path/to/my/centralized/hooks
or,

    git config core.hooksPath hooks/in/repo

or, edit config file in repo `repopath/.git/config`, like this:

    [core]
        hooksPath = /my/centralized/hooks/path
or,

    [core]
        hooksPath = path/to/hooks/in/the/repo

*NOTE* If the repo has config for hooksPath, it will override the global configuration.

## Troubleshooting

### Execution rights
Make sure the script has execution rights

### Naming
Make sure the scripts have the correct hook name. Eg. a pre-commit-hook should be named `pre-commit`

## Furhter information
Please check the git-scm official information.
