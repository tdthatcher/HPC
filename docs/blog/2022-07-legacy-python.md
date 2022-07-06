---
title: Options for Legacy Python 2 Code
postdate: July 15, 2022
layout: post
author: Timothy Thatcher
description: Options for handling legacy Python 2 code on Eagle
---

# Legacy Python Code on Eagle

### What is Legacy Code?
One definition of "legacy" code or software is code was written in the past using currently outdated, obsolete, or otherwise deprecated, compilers, functions, methods, or methodology.

Python 2.x was officially declared "end of life" on January 1st, 2020 in favor of Python 3. This means that ALL python 2 code is, by extension, considered "legacy code" at this point, and in an ideal world would never be used, as there will be no more official updates, bug fixes, or security patches to the Python 2.x interpreter by the Python Software Foundation or official maintainers. 

In practice, there are still software packages out there that have not been converted yet, or will never be converted, to Python 3.

### Software I need is written in Python 2. What do I do?
There are several options available for users who are considering software written in Python 2.x. You may:

* Look for an updated version of the software
* Search for an alternative package or module
* Convert your code to Python 3
* Use a conda virtual environment to run your own version of Python 2

Each method has advantages and disadvantages, discussed below, but searching for an updated version should always be your first move when considering code written in Python 2. If you are the author of the software, you should _strongly_ consider refactoring to use Python 3, for reasons discussed below in the section on code conversion.

#### Search for updates
If the software or module is still under active development, it's highly likely that the authors have transitioned the software to Python 3.x, so the first step is to search for an updated version. If an updated version is available, you should strongly consider it over an outdated Python 2 version. It will likely be more secure, have better performance, be more reliable, and have a longer shelf life for reproducibility in the future.

#### Search for alternatives
The original software you want may no longer be maintained, but there may be a newer replacement or an alternative available. Newer software may be written in Python 3 or another language entirely. Compared to out-of-date software, alternatives often have improved performance and reliability, though it may require adjusting your tool chain or workflow for the new software.

#### Converting Python 2 to Python 3
For small codebases, manually converting from Python 2 to 3.x may be possible with a minimum of effort. More complex software could require more effort, but the conversion will help extend the useful lifespan of your software. Python

Python's development tool suite (e.g. the `python3-devel` package in CentOS) also includes the `2to3` tool, which can perform some automated conversion.

Documentation on 2to3 is available on the [python.org documentation site](https://docs.python.org/3/library/2to3.html)

#### Using Conda for Python 2
Currently, [Conda](https://www.anaconda.org) is capable of managing virtual environments using either python 3 or python 2. You may load the conda module on Eagle with `module load conda` or install your own conda/miniconda in your /home or /projects directory.

Once you have conda, the following command:

`conda create --name my_environment python=2`

will create a new environment with the latest release of python 2 available. See the official Conda documentation for further options.

Since Python 2 has been officially deprecated, this feature may not last forever, and you are encouraged to explore the other options before you resort to a conda environment. As time passes, more and more code is either being updated or rewritten entirely in Python 3, and the community-maintained Python 2 packages in the default conda channels will likely disappear at some point in the future.

Over the past decade, Python has become a powerful tool for data science, and will likely continue to be so for the foreseeable future. Keeping your code modernized to the latest standards will help ensure both the longevity and reproducibility of your software and your results.






