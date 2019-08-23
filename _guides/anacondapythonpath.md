---
layout: archive
collection: guides
title: "Making Anaconda Python Find Your Python Scripts - Modifying the PYTHONPATH"
permalink: /guides/anacondapythonpath/
author_profile: true
---

Suppose you write a Python script file called, say, `coolscript.py` which has all kinds of cool functions that you wrote. Maybe you saved it on your computer's desktop. Maybe then you go to Anaconda Navigator, fire up Spyder or another program within Anconda, and try to import those functions with a line of code like, 
```python
from coolscript import *
```
But, alas, you receive an error:
```python
ModuleNotFoundError: No module named 'coolscript'
```
Lots of things might cause this, but perhaps it is because the directory in which `coolscipt.py` resides is not part of the `PYTHONPATH`, i.e., the set of file directories in which Python searches for files it needs. Let's find out what our `PYTHONPATH` is and see if it contains our script. Start an Anaconda Prompt. You may be able to do this directly from the Start menu in Windows or the Launcher app in MacOS, but another way you can start it is by launching the Anaconda Navigator and launching a terminal as in the screenshot below:

![open terminal](/images/anacondapythonpath-openterminal.png "open terminal")

Now, run this command to see your `PYTHONPATH`:
```
python -c "import sys; print('\n'.join(sys.path))"
```
In my case, I get the following result on a personal Windows-based machine with a fresh Anaconda3 installation:
![pyhtonpath](/images/anacondapythonpath-findpath.png "pythonpath")
