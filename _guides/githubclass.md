---
layout: archive
collection: guides
title: "Using Github Classroom as a Student"
permalink: /guides/githubclass/
author_profile: true
---
This describes how to edit the contents of a GitHub Classroom repository.

1. Start by visiting the GiHub Classroom link that your instructor provided. You should accept the assignment at that link.
2. A template **repository** (usually just called a **repo**) containing the files you need for the lab was automatically created in your Github account. Confirm that you can see it on the website; it should be named something like ``homework01-YOURNAME`` (depending on what your teacher named it).
3. If you want to work on the files on your own computer, then now you need to **clone** the remote GitHub repo to your local computer. For this set of instructions, I will assume that you installed and logged into the Github Desktop App. In the GitHub Desktop app, click on the "Current Repository" pull down menu, where you will find an "Add" button. From there, choose "Clone Repository" and find the repo that you just accepted. Clone it to a location on your computer of your choice. Pick somehwere sensible. To give an example, on my Windows machine, I keep all my repos in a ``GitHub`` folder inside my ``Documents`` directory, so if i were to clone the repo I meantioned in step 2, the local path might end up looking like ``D:\Documents\GitHub\homework01-YOURNAME`` (but that's just my personal preference). 
4. Once the repo has been cloned, make sure that the "Current Repository" is set to be the one you just cloned. Now your ready to work. Whenever you start working on one of your repos, you should have GitHub Desktop open and set to that repository.
    - Normally, before you'd start working, you'd want to click "Fetch Origin" to make sure that no one has made any updates since you last looked. If they did, you'd want to **pull** them from the remote server to your copy, so that you could see the updates. However, we just made this repo, so there's nothing to pull in yet.
5. Click the button that shows the repo's files in your file manager. The exact wording varies by operating system, but it's probably something like "Show in Explorer" or "Show in File Manager." You should see the actual files in this repo. Any changes you make to these files will be tracked by ``git``. 
6. Now you can make some changes and do some work. For example, if the repo came with a Python Jupyter notebook (an ipynb file), then you might open that notebook, do some coding, and save your work.
7. Now that you've made a change, you need to **commit** it to the repo, creating a permanent record of your work. To do so, you must give a description of your commit, which should be clear, descriptive, and concise; for example, "wrote some code to make a plot of the E-field" would be reasonable.
    - Take a minute to reflect on this step, because it is the crux of the whole ``git`` concept. You can always undo ("revert") commits, and you can always easily find the one you need if your descriptions are clear. That means that you should commit often throughout a complicated project, not wait until the whole thing is done. *This is central to the whole concept of ``git``.*
8. The commit still only exists on your computer; to sync it with the remote server you must **push** it to GitHub. 
9. Now, if you go look at the repository on the GitHub website, you should see that it includes your changes.
    
## GitHub Classroom Grading
All that work you just did will be graded. However, you don't need to do anything else to submit it. Just as you used git to create your project, your instructor will simply pull all of your repos to their computer to grade them. Grading will be done as direct changes to the repo. 
