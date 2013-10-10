git-pull-request
================

Git extension to create GitHub Pull Requests

Installation
------------

Just lay `git-pull-request` on your `PATH`.

Usage
-----

Place a Personal Access Token in the `GIT_PULL_REQUEST_ACCESS_TOKEN` variable first. You can create one at https://github.com/settings/applications.

```bash
usage: git pull-request -h <branch> -t <title> [options]

Create a Pull Request (PR) in GitHub.

OPTIONS:
   -h <branch>         Branch you want to PR. It has to exist in the remote.
   -r <repo>           Repo where to PR. Default is picked up from "$ git remote -v" origin fetch url.
   -o <owner>          Owner of the repo. Default is picked up from "$ git remote -v" origin fetch url.
   -b <base>           Branch where you want your PR merged into. Default "master".
   -t <title>          Title of the PR.
   -d <description>    Description of the PR.
```

