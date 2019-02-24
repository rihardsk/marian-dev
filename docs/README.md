# Marian NMT code documentation and API

This directory contains code documentation and library API for developers of Marian NMT.

The documentation is generated using
[Sphinx](https://www.sphinx-doc.org/en/master/usage/quickstart.html) +
[Breathe](https://breathe.readthedocs.io/en/latest/directives.html) +
[Doxygen](http://www.doxygen.nl/manual/docblocks.html) +
[Exhale](https://exhale.readthedocs.io/en/latest/usage.html).
The documentation source code is written in `.rst` or `.md` files with special directives that allow
to reference to C++ source code and documentation. The source documents are then build into static
HTML pages.


## Installation

On Ubuntu, install the following packages:

    sudo apt-get install python3-sphinx python3-pip python3-setuptools doxygen
    pip3 install --upgrade sphinx breathe exhale recommonmark

Documentation building should also work on Windows, but has not been tested yet.


## Generation

The documentation can be generated by running:

    make html

The website will be generated into `_build/html` and accessible by opening _index.html_ in your
browser.

The generation of automatic library API can be skipped to speed-up the building process
significantly:

    make html-no-api

Directories:

- `_build` - output directory for HTML documentation
- `_doxygen` - automatically generated Doxygen XML files
- `_static` - custom CSS and JavaScript files
- `api` - automatic library API generated with Exhale
- All `.rst` files and some `.md` files in this directory and its subdirectories are documentation
  source files


## Writing documentation

See the 'Writing documentation' section in the generated HTML documentation or `writing_docs.rst`.
