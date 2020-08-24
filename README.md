# Cross-squad Documentation

## Deployed site URLs

- Marketing squad: https://not-a-potluck.gebel.tech
- Front-end squad: https://app.not-a-potluck.gebel.tech
- Back-end squad:

## Git Best Practices

Branches should be made on a per-feature basis. That can be one file, or one
function on a file, what constitutes a feature is the kind of thing that is hard
to define, but you know it when you see it. If working on the same file as
someone else at the same time as they are working on it, everyone may not see a
feature the same, so make sure you both agree on what constitutes the features
you are both working on, try not to be working on the same part of the same file
with another person. As long as you work on different parts of the file, you
should be able to work on a file with another person without merge conflicts.

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

## Prettier
