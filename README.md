# Cross-squad Documentation

- [Cross-squad Documentation](#cross-squad-documentation)
  - [Deployed site URLs](#deployed-site-urls)
  - [Git Best Practices](#git-best-practices)
    - [Branch management](#branch-management)
    - [Pull request](#pull-request)
  - [Prettier](#prettier)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>

## Deployed site URLs

- Marketing squad: https://not-a-potluck.gebel.tech
- Front-end squad: https://app.not-a-potluck.gebel.tech
- Back-end squad:

## Git Best Practices

### Branch management

Branches should be made on a per-feature basis. That can be one file, or one
function on a file, what constitutes a feature is the kind of thing that is hard
to define, but you know it when you see it. If working on the same file as
someone else at the same time as they are working on it, everyone may not see a
feature the same, so make sure you both agree on what constitutes the features
you are both working on, try not to be working on the same part of the same file
with another person. As long as you work on different parts of the file, you
should be able to work on a file with another person without merge conflicts.

When pulling a branch from the remote repo (`origin`) that has never been pulled on your local repo, for example when pulling another person's branch to edit their pull request, do not use `git checkout -b branch_name` `git checkout branch_name`. This will create a new branch that does not have any of the changes from the remote repo. Instead, checkout the branch with

```sh
git checkout origin/branch_name
```

The reference to `origin` assures you pull the branch from the remote.

### Pull request

When reviewing a pull request, be sure to check all the changes made and any
tests that are failing. After reviewing a pull request, if you approve it you
should also merge it unless you have made changes to the pull request, in which
case you should have your changes reviewed like any other PR. Github has an
option to merge the pull request you are reviewing near the bottom of the first
page of the PR. After merging the pull request, there will be a button in the
same place the merge button was to delete the branch. Unless the original
requester requested otherwise in their description you should always delete the
branch. This helps to prevent people from accidentally working on or branching
from a stale branch. It also prevents the repo from ending up with massive
numbers of branches.

Before starting a new branch, review the open pull requests and approve and
merge any that you feel are ready. This assures you are making the new branch
from the latest possible version of master. Also, to make sure your local repo
is as up-to-date as possible, run these commands before making the new branch:

```sh
git checkout master
git fetch --prune origin
git pull
```

The `--prune` option deletes any branches on your local repo that have been
delete on the remote repo. This is usually best practice to keep you from
eventually having dozens of stale branches on your computer, however if you feel
you need one of the old branches for now you can omit this option.

`git fetch` updates the git index on your local repo, but it does not pull in
the latest version of the files. This is what the `git pull` command does. If
you think of the git index as being similar to the index in the back of a book,
you can think of `git fetch` as updating the back of the book, and `git pull` as
updating the front.

## Prettier
