---
layout: archive
title: "Guides for Students"
permalink: /guides/
author_profile: true
---

{% include base_path %}

Here are various guides to help with technical tasks.

Guides I wrote:
{% for post in site.guides reversed %}  {% include archive-single-guide.html %}{% endfor %}

-----

External guides:

[Installing Anaconda Python](https://docs.anaconda.com/anaconda/install/)

[Using Google Colab with Github](https://colab.research.google.com/github/googlecolab/colabtools/blob/master/notebooks/colab-github-demo.ipynb)

[Using Google Colab with Google Sheets](https://colab.research.google.com/notebooks/io.ipynb#scrollTo=sOm9PFrT8mGG)

[Using Github via the Github Desktop app](https://help.github.com/en/desktop)
