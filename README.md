# Olimex documentation

**Build Version**: `mkdocs, version 0.15.3`

**Known bugs**: hidden pages (i.e. pages not included in nav/pages within mkdocs.yml) are not rendered, breaking hyperlinks

## Overview

Documentation is written in markdown and stored in the `docs/` subfolder.
Product-specific documentation should be placed in `docs/products` with associated images in `docs/products/<hardware|software>/images`.
Common images should reside in `docs/images`.

Official output is https://docs.olimex.com.

## Resolve dependencies

To build and view the mkdocs-generated documentation:
`$ sudo apt-get install mkdocs`

## Generating documentation

From the parent folder of the repo, run:

`$ mkdocs build`

This creates the mkdocs site in the `site/` folder.
After changing text in an existing file, you may wish to build a clean instance using:

`$ mkdocs build --clean`

## Testing documentation layout

To preview locally, start the server with `$ mkdocs serve`.
You will be able to edit existing files and observe the results in real time.
