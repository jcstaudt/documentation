# Olimex documentation

## Overview

Documentation is written in markdown and stored in the `docs/` subfolder.
Images should be placed in `docs/images`.

Official output is https://docs.olimex.com.

## Resolve dependencies

To build and view the mkdocs-generated documentation:
`$ sudo apt-get install mkdocs`

## Generating documentation

From the parent folder of the repo, run:

`$ mkdocs build`

This generates a `mkdocs.yml` configuration file and creates the mkdocs site in the `site/` folder.

## Testing documentation layout

To preview locally, start the server with `$ mkdocs serve`.
You will be able to edit existing files and observe the results in real time.

After changing text in an existing file, you may wish to build a clean instance using:

`$ mkdocs build --clean`
