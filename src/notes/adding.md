---
layout: page
order: 2
title: Adding files and tracking changes
---

{% panopto "e44b063e-df33-4179-809b-add300e72b19" %}


To be able to track changes to our files, we need to create a Git `repository`. This repository is the sum of our current files that we are tracking, plus all the changes and history that go along with them. Creating a git repository is straightforward; to create an empty repository in the current directory we use the following command:

```bash
git init .
```

Once we have a repository and some files to track, there are a few commands we'll need to use to control how Git tracks our files. Tracking files in a repository is a two stage process. First we `stage` the files, which means telling Git to prepare to add the current changes to the file to the repository. Then we `commit` the changes, which means a record of the changes we staged is added to the repository itself.

We add changes to a file to the commit `stage` using 

```bash
git add <FILENAME>
```

`git add` tells Git that it should prepare to add a record of the current changes to the specified file to the repository. Once we have all the changes we want to add to our repository staged, we commit them:

```bash
git commit -m "<my helpful commit message>"
```

This creates a new commit in the repository with the given `commit message`, logging all changes to files that were staged in the previous step.

By using `git add` and `git commit` whenever we have made substantial changes to our project that we feel are worthy of tracking, we can keep a record of all changes to our project over time.