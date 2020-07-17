# Julia Notebooks

Some Julia Jupyter/Colab Notebooks to learn and play around with the [Julia language](https://julialang.org/).

Right now, there are two notebooks:

* [Julia_for_Pythonistas.ipynb](https://colab.research.google.com/github/ageron/julia_notebooks/blob/master/Julia_for_Pythonistas.ipynb)
  * This is an introduction to the Julia language for Python programmers.
  * It covers the main Python constructs and shows how to code them in Julia.
  * Also covers powerful Julia features such as parallel computing and metaprogramming.
* [Julia_Colab_Notebook_Template.ipynb](https://colab.research.google.com/github/ageron/julia_notebooks/blob/master/Julia_Colab_Notebook_Template.ipynb)
  * This is a template to create Colab notebooks for Julia. It was inspired by the notebooks proposed in [this discussion](https://discourse.julialang.org/t/julia-on-google-colab-free-gpu-accelerated-shareable-notebooks/15319/24), with additional features.
  * It supports setting the version of Julia easily (from 0.7.0 to the latest version).
  * Easy to change the list Julia packages to install.
  * Support setting the number of threads.

_Enjoy!_

## About this fork
I found the original Julia_for_pythonistas.ipynb quite lazy on loading and working through, so I've splitted the nb into several --logical-- parts:
* Intro: running locally, getting help, first look at Julia, Unicode, python code in Julia, Loop fusion & performance
* Numbers and control flow: numbers, strings ``if`` and ``for`` statements
* Data Structures: Tuples, structs, arrays, dicts, sets, other collections and generators
* Functions: *still working through*
* Misc:
* Large projects and performance:

Also, I've added a tables summary md to have a quick reference
