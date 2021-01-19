---
layout: archive
collection: guides
title: "Setting up an Anaconda environment for a class"
permalink: /guides/anacondaenv/
author_profile: true
---
## Setting up Python

In many of my classes, we use Python Jupyter notebooks for calculations, and one of the easiest ways to get the software for these notebooks is to use Anaconda.

You should have [downloaded and installed the Anaconda Python distribution](https://docs.anaconda.com/anaconda/install/) already (you may use a different means of installing Python if you prefer, but I will not be able to provide support). We need to get Anaconda ready to do science.

![An animation of creating a conda environment](/images/createcondaenv.gif)

1. Start Anaconda Navigator.
2. Go to the "Environments" tab in Navigator, and click the "Create" button to create a Python 3.7 (or greater) environment in which you'll do this course's work. Name it something clear (I chose "ph447-2020" in my video). Wait until the environment is fully created, which may take several minutes.
3. Click on the small arrow next the the new environment's name. Click "Open Terminal." Type ``conda install git numpy scipy astropy`` (just the most common packages -- you can add others if you want). Follow the prompts, typing a ``y`` to confirm that you want to proceed when prompted. This will install several common packages of Python code, and you can use this approach to install others in the future.
4. Again on the "Home" tab of the navigator, there should be a button to "Install" Jupyter Notebook. Do so. It may take several minutes.

**Whenever you work on Python code for this class, you should do so with this environment selected.** That is, everytime that you open the Anaconda Navigator to work on this class, you should use the pulldown menu to select this environment. This will ensure that you continue to have access to the packages you need.

To edit a Jupyter notebook, select the environment, then click the Jupyter notebook button. That will open your web browser to a page that lets you navigate to and open python files.
