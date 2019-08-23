---
layout: archive
collection: guides
title: "Making Anaconda Python Find Your Python Scripts - Modifying the PYTHONPATH"
permalink: /guides/anacondapythonpath/
author_profile: true
---

(The following information applies only to Anaconda installations. The basic idea applies to any python installation, but the precise ways of addressing the issue are different.)

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

Unless my script is in one of those folders (or their subfolders), it will not be found by python unless you explicitly indicate the complete path when you call it from python (or if you start python in the directory in which the file resides). Ideally, we want to avoid this issue by properly installing modules. If it is someone else wrote the code module, the best way to do that is to install it using `conda` or, if that isn't possible, by using `pip` or a `setup.py` file. These are also the best practices for one's own code.

However, sometimes it is helpful to have a convenient "working directory" for temporary or unfinished code, and you may not want to navigate python to that directory every single time you call the code. One way to solve this problem is add your preferred directory to your `PYTHONPATH`. 

If we want to *temporarily* add a directory to our python, we could simply run the following commands in the python terminal that we are using to run the script:
```python
import sys
sys.path.append(r'/path/to/my/package')
```
where "/path/to/my/package" should be changed to the file path to the folder containing your python script file.

If we want to more permanently add a folder to our `PYTHONPATH`, we can do so by creating a `.pth` file in the `site-packages` directory. In the screenshot above, notice the `site-packages` folder. Each Anaconda installation should have a folder of that name. Create a new text file in that directory, naming it such that it has the file extension `.pth` (e.g., a file named `extrapythonfolders.pth` would be fine). Within that text file, you can list directories that you want to include in your `PYTHONPATH`, one per line. For example, on a Windows machine I might add a line that reads `C:\myscripts`. Save the file with these new locations, and then try again running the following command on the Anaconda Prompt:
```
python -c "import sys; print('\n'.join(sys.path))"
```
You should see that your new directories are now included (you may have the restart Anaconda to make it work in all of its software, though). You should now be able to import modules or run code from that directory, regardless of where you start python in your file structure.
