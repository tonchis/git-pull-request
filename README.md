git-pull-request
================

Git extension to create GitHub Pull Requests using the GitHub API.

Usage
-----

From your checked-out topic branch:

    $ git pull-request

This will create a Pull Request in the repository you're contributing to.

`git-pull-request(1)` assumes there are two ways to work against a repository.

Pushing to the repository itself, where you clone using SSH or pushing to a fork of your own.

The latter requires you to have the original owners' repository as a remote.

More options:

    usage: git pull-request [options]
       or: git pull-request -t <title> [options]
       or: git pull-request -i <issue> [options]

    Create a Pull Request (PR) in GitHub.

    OPTIONS:
       -h <branch>         Branch you want to PR. It has to exist in the remote. (Default: current branch)
       -r <repo>           Repo where to PR. (Default: current repo name)
       -o <owner>          Owner of the repo. (Default: parsed from your remote's URL)
       -b <base>           Branch where you want your PR merged into. (Default: master)
       -t <title>          Title of the PR. (Default: the last commit's title, as long as there is only one commit in the PR.)
       -d <description>    Description of the PR. "-" means read from standard input.
       -i <issue>          Number of the issue related.
                           WARNING: This will convert the issue into a PR and override <title> and <description>
       -e                  Opens your EDITOR in a temporary file to write the description.
       -c                  Copy the PR URL to the clipboard.
       -f                  Fake run, doesn't make the request but prints the URL and body.
       -w                  Add "wip" label on the issue. The -i <issue> option is required.

The `-c` option requires `xclip` or `pbcopy`.

Installation
------------

With Homebrew

```shel
brew tap tonchis/goodies && brew install git-pull-request
```

For the standalone version, just lay `git-pull-request` on your `PATH`.

You'll need to create a Personal Access Token at https://github.com/settings/applications and put it in the `~/.git-pull-request` file.

