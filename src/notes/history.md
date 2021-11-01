---
layout: page
order: 4
title: Using the history
---

{% panopto "5db30e72-a435-4e86-b5d5-add300e72cca" %}

One of the other useful things about tracking your changes using Git is being able to go back to any point in your project and see what the code looked like, or even to reset or revert the commits that happened after that point.

There are three main commands for examining or undoing our changes.

-   `git checkout`
-   `git reset --hard`
-   `git revert`

All three are discussed below, but probably you want `git revert`. 

## `git checkout`

The `checkout` command is actually more commonly used to create new branches[^1] but it can also be used to have a look at the state of our project at any point in time. The command:

```bash
git checkout <COMMIT_ID>
```

Will allow us to see the state of our whole project at the time of that commit. To get back to the current state, we can do

```bash
git checkout master
```

## `git reset --hard`

`git reset` can be used to remove any trace of a particular commit. This undoes any changes made in that commit and resets the files to their previous state. However, this can only be used to remove local changes - if those changes have already been pushed to a remote repository they will still exist, and the next time you try to synchronise git will try to force you to re-include those changes in your project. To remove changes that have already been pushed you should use ...

## `git revert`

This command lets you undo changes made in a commit - it essentially creates a new commit with the inverse of the original changes applied. This makes the changes more public and transparent, and makes it easier to keep remote repositories in sync.



[^1]: We'll worry about these later
