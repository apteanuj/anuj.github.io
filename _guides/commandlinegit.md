---
layout: archive
collection: guides
title: "Using Github via git from the command line"
permalink: /guides/commandlinegit/
author_profile: true
---

[Github](http://www.github.com) is really just an online storage space designed to host `git` repositories ("repos"). These repositories are a standard method of version control for programming projects. The most obvious way to update your files in a Github repository is by editing them on the website or uploading them from your computer using the web interface. However, these methods are very cumbersome, and they are not how `git` repositiories are intended to be used. The basic idea of `git` is to allow you to work on the files on your computer in their folders using whatever methods you wish, while `git` itself tracks the changes you make and syncs them with the main repository.

The easiest way to use this approach with Github is via the [Github Desktop app](https://help.github.com/en/desktop). This app is what I use on both MacOS and Windows. It's pretty self explanatory, but that link contains tutorials for using it, and I won't further address it here.

Originally, however, `git` was used only from the command line of your operating system (and this what I always use on Linux, and sometimes on other operating systems).  I wish to give the basics of `git` (as used from the command line) here. If you have a modern version of MacOS or Linux, you should already have `git` installed. If you are using Anaconda in Windows, you can obtain `git` within Anaconda environments by running `conda install git` from the Anconda prompt. If you are using Windows but not Anaconda, you'll need to [obtain `git` on your own](https://git-scm.com/).

Once you have `git` running on your computer, you'll need to give it some information about yourself before it can function properly. From the command line, you'll need to set your name and email address as follows:
```
git config --global user.name 'My_Name'
git config --global user.email 'myEmail@wherever.com'
```
Now you're ready to use git. The commands are fairly simple, and I won't enumerate them all here because there are many guides on the internet. In particular, [this tutorial reference](https://www.atlassian.com/git/tutorials/setting-up-a-repository) is fairly comprehensive, and **I recommend reading through it**.

Suppose you've created a repository on the Github website. When you create a repository on GitHub, it exists as a *remote* repository. You can clone your repository to create a *local* copy on your computer and sync between the two locations. This process is described on this webpage: [https://help.github.com/en/articles/cloning-a-repository](https://help.github.com/en/articles/cloning-a-repository). The basic gist of it is that you need to run a `git clone` command like follows (updated with the correct URL, of course):
```
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY
```
(If you've already cloned your repo and just want to update the local copy, you'll want to use `git pull` instead) Now you can work on your files, and `git` will monitor those files for changes. When you want to add your changes back into the main branch of the repository, you first probably want to tell `git` to add any new files that you've created to its list of tracked files:
```
git add -A
```
Next, you'll want to "commit" all your changes to the local copy of the repository, so that they become fully recorded to it:
```
git commit -m "some message"
```
The message is mandatory, and should succintly describe the changes you made. Finally, you'll probably want to "push" your local copy (with its new changes) to the main remote copy of the repository:
```
git push
```
With that, you've successfully use `git` to implement version control while working on a project.
