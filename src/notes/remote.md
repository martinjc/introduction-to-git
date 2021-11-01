---
layout: page
order: 3
title: Using git + Gitlab
---

{% panopto "9ddd5877-020f-4bb8-8f59-add300e72c2d" %}

One of the really neat things about Git is that it works as a distributed service, in that it allows us to keep multiple copies of a repository in different places, and use Git to keep them all in sync with one another.

A really common use case is to keep a local copy of your repository on your local machine, and another copy of the repository in an online service like [Github](https://www.github.com) or [Gitlab](https://www.gitlab.com)[^1].

The University has a [Gitlab service](https://git.cardiff.ac.uk) to which you have access. You can find this at [`git.cardiff.ac.uk`](https://git.cardiff.ac.uk).

To keep a copy of our repository in one of these services, we must add the server as a new `remote` to our repository.

```bash
git remote add <REMOTE NAME> <BRANCH NAME> <REMOTE ADDRESS>
```

Then we use the `git push` command to send any local changes to our remote repository. If we ever have changes in our remote repository that we need to incorporate into our local repository we can use `git pull` to synchronise these changes from the server and merge them into our current code. We also have the `git fetch` and `git merge` commands to do this in two separate steps


[^1]: Other services also exist...