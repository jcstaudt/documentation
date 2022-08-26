# Olimex Documentation #

## Overview ##

Documentation is written in markdown and stored in the `docs/` subfolder.  Images go in `docs/images`

This repo is meant for storing and quick glances.  Official output is [http://docs.olimex.com](http://docs.olimex.com).

Olimex Documentation is available in the following formats:

* mkdocs site [http://docs.olimex.com](http://docs.olimex.com).
* PDF user guides \(in progress\)

Olimex Documentation relies on a file naming convention:

`Parent-Topic-Name_Child-Topic-Name.md`

Parent-Topic-Name and Child-Topic-Name are separated by an underscore `_`.  Hyphens `-` are automatically converted to spaces.

Please try to avoid creating new parent topics unless absolutely necessary.

Current Parent Topics:

* Hardware
* Process
* Release
* Developer Guide
* User Guide
* Howto

### .gitignore ###
For easier testing and commits `.gitignore` is configured to ignore `site/`

`mkdocs.yml` should probably be added, but we can commit for now

## Required Packages ##

The documentation build process will require the following packages:

* git
* python-jinja2
* mkdocs

Install these on the development host using:

`sudo apt-get install -y -qq git python-jinja2 mkdocs`


## Tools ##

### mkOlimexDocs.py ###
generates mkdocs.yml file based on contents of `docs/`

* command-line options for input and output directories
* requires the python-jinja2 module which may not be installed by default
* not needed unless making changes to the structure of the documentation
* see `mkOlimexDocs.py -h` for help

### missing tools ###
The following capabilities are not yet available.

* html2doc output to PDF user manual
* automated mkdocs deployment to [http://docs.olimex.com](http://docs.olimex.com)

## generating ##
From the parent folder of the repo, run:

`tools/mkOlimexDocs.py && mkdocs build`

This will generate the mkdocs.yml configuration file and then generate the mkdocs site to the `site/` folder.

## testing ##
To preview locally, execute the preview server `mkdocs serve`. You will be able to make edits to existing files and observe the results in real time.

After changing text in an existing file, use this command to rebuild and view the documentation:

`mkdocs build --clean && mkdocs serve`

After adding a new file, either hand-edit `mkdocs.yml`, or rerun `tools/mkOlimexDocs.py`.

## Quick Start ##

```
pip install mkdocs
git clone https://github.com/OLIMEX/documentation
#vim docs/[Parent Topic Example]-child-topic-example.md
#generate config, build, launch local preview server
tools/mkOlimexDocs.py && mkdocs build --clean && mkdocs serve
git add docs/*.md
git commit -m "added new howto on exampling"
git push
```
