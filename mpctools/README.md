# mpctools
A set of python tools for extending standard (and non-standard) libraries. These originated from my own needs and those
of my students, and I decided to put them here in case they may be useful to other people.

## Features

The library currently contains the following two packages:
 1. `extensions`: A number of extensions to numpy, sklearn, pandas and matplotlib, as well as general-purpose utilities.
 2. `parallel`: A set of tools for wrapping pathos multiprocessing in a simple easy to use interface with multiple
     parallel workers. 
 
Eventually, I plan to add a neural toolbox.

More details for each library are provided as doxygen-style comments in the modules.

## Setting up

### Requirements

This Library has the following dependencies:
  * scikit-multilearn
  * scikit-learn
  * matplotlib
  * seaborn
  * pandas
  * pathos
  * scipy
  * numpy
  
In most cases, the above can be automatically installed through the library itself (i.e. pip will attempt to download 
them). If this causes issues, just install them manually.

There is an additional requirement for opencv: however, this is not included in the list of requirements for the reason that
some people may wish to build it from source. This is required for example if one wishes to use non open-source encoders: in this
case, I have provided a blog-post about how to do this on my 
[webpage](https://michaelpjcamilleri.wordpress.com/2019/03/21/installing-opencv-with-all-the-bells-and-whistles/).
Otherwise, you can either chose to ignore it if you are not going to use the CV extensions module (cvext),
or install the stock open-cv wrapper for python:
```bash
pip install opencv-python
```

### Installing

Installation is as easy as running the setup script and then installing using pip:
  ```bash
  python setup.py sdist --format=tar
  pip install dist/mpctools-0.3.10.tar --user
  ```
 The `--user` flag is optional and only necessary when one does not have full system permissions. Note that depending on
 which version the library is at, you may need to change the version number of the install command.
