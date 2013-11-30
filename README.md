git-pull-request
================

Git extension to create GitHub Pull Requests

Installation
------------

Just lay `git-pull-request` on your `PATH`.

Usage
-----

First you need to create a Personal Access Token at https://github.com/settings/applications. Then store it under

```bash
$ git config --global github.pull-request.token <access_token>
```

```bash
usage: git pull-request -h <branch> -t <title> [options]
   or: git pull-request -h <branch> -i <issue> [options]

Create a Pull Request (PR) in GitHub.

OPTIONS:
   -h <branch>         Branch you want to PR. It has to exist in the remote.
   -r <repo>           Repo where to PR. Default is picked up from "$ git remote -v" origin fetch url.
   -o <owner>          Owner of the repo. Default is picked up from "$ git remote -v" origin fetch url.
   -b <base>           Branch where you want your PR merged into. Default "master".
   -t <title>          Title of the PR.
   -d <description>    Description of the PR.
   -i <issue>          Number of the issue related.
                       WARNING: This will convert the issue into a PR and override <title> and <description>
   -e                  Will open your EDITOR in a temporary file to write the description.

```

