---
layout: default
title: Documentation Setup
---

# Princeton Geophysics Documentation and Tutorials

This is the homepage for github pages based documentation written
by members of the Princeton Geophysics group.

The setup is fairly simple since `Jekyll` will take care of creating a
website from provided `markdown` files given a `_config.yml` file. So,
every page in the directory `docs` automatically is included.
Subdirectories of `docs` will automatically create subpages.

The detailed description of the theme and how to organize content for
`jekyll` pages is shown in the docs for [Just the
docs](`https://just-the-docs.github.io/just-the-docs`).

At a bare minimum each page has the following header:

```markdown
---
layout: default
title: <title>
---
```

Followed by normal markdown syntax. As far as I know, cross referencing
is not really supported (feel free to add explanation if it is).

For simplicity do not use the `nav_order: <int>` directive. So, no

```markdown
---
layout: default
title: <title>
`nav_order: <int>`
---
```

That way, the docs except the `Homepage` are sorted in alphabetical order.

If you want to create a subdirectory structure, please visit
[`just-the-docs`
Documentation](https://just-the-docs.github.io/just-the-docs/docs/navigation-structure)
on navigation structure. Because the markdown headers need to know
what's a parent and what not. To sort your `subdirectory` docs in a
specific order, please refer to the navigation structure documenation
as well.

The documentation are automatically built once new adds are merged
with or pushed to the `main` branch.  Note that it takes a sec to
update.

Happy docs writing!

---

## Useful external quick links

***Command line***:
* Be a command line wizard: [Intro to the Command Line](https://github.com/gabeclass/introcmdline)

***Anaconda Installation***
* Install Anaconda: [Link](https://docs.anaconda.com/anaconda/install/index.html)

or less storage
* Install miniconda: [Link](https://docs.conda.io/en/latest/miniconda.html)

***Documentation for `conda-build` and creating `conda` packages***:
* [Link](https://docs.conda.io/projects/conda-build/en/latest/index.html)

***YAML Documentation***
* [Link](https://yaml.org)

***Cheatsheet for `conda`***
* [Link](https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf)

***Shameless plug***:
* How to make a python package: [Link](https://lsawade.github.io/how_to_make_a_python_package/index.html)
