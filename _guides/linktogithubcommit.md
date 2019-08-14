---
layout: archive
collection: guides
title: "Linking to a particular version (commit) of a Github file"
permalink: /guides/linktogithubcommit/
author_profile: true
---


For various reasons, you may wish to link to a particular version, known as a commit, of a file in a repository on Github. For example, if you are linking to a file on Github as a way of turning in code for homework credit in one of my classes, it is necessary that you link to a commit that occurred before the due date, so that I can tell what work you had completed by that time. It can also be useful if you are trying to share information with a collaborator when debugging code.

If you visit your Github repositories via a web browser and then go to one of your files, you are presented with a screen similar to the one shown in the screenshot below:

![Github file view](/images/githublink1.png "Github file view")

Notice that this is a screenshot of this very webpage, but before I had added all of this content. Additionally, notice the portion of the URL that I have indicated with an arrow. It includes the word "master" in the URL. This portion of the URL instructs Github to retreive the latest version of this file from the "master" branch of the repository.

Try [visiting that URL right now](https://github.com/emtilt/emtilt.github.io/edit/master/_guides/linktogithubcommit.md), and you will see the code that generated the text that you are currently reading; you will not see the (older) version of the file shown in the screenshot. You would need a different URL to link to the version of the file that existed at that particular historical moment.

Github has a convenient shortcut command to help with this problem. If you press the <kbd>y</kbd> button on your keyboard while on the Github page for a file, the URL will change to a permanent URL for that version of the file. For example, while I was on the page shown in the screenshot above, I pressed <kbd>y</kbd> and the URL change to what is seen in the screenshot below:

![Github file view](/images/githublink2.png "Github file view")

If you [visit the URL shown in that screenshot](https://github.com/emtilt/emtilt.github.io/blob/756481c3dc86734c70b34abfcc159cdeaeee800c/_guides/linktogithubcommit.md), you will see that it shows the historical commit. If you want to share one particular file version with someone, then you should share the URL that you generate in this fashion. If you want to simply share the latest version of a file in the master branch with someone, you should simply use the "master" version of the URL.
