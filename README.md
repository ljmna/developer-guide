![alt text](https://mapaction.org/wp-content/themes/mapaction/images/logo.svg)

[Documentation Site](https://stellular-basbousa-d782de.netlify.app/)

# Contribute

## Set this up locally

It is recommended to install `docsify-cli` globally, which helps initializing and previewing the website locally.

```bash
# Install nvm appropriately for your os

# Install a newish npm version (at time of writing 18)
nvm install --latest-npm
nvm use 18.9.0

# Install docsify
npm i docsify-cli -g

# Run this local dev site
npx netlify-cli dev
```

### Preview your site

Run the local server with `docsify serve`. You can preview your site in your browser on `http://localhost:3000`.

```bash
docsify serve docs
```

?> For more use cases of `docsify-cli`, head over to the [docsify-cli documentation](https://github.com/docsifyjs/docsify-cli).


### Writing content

- `README.md` acts as the home page

You can easily update the documentation in `README.md`, of course you can add [more pages](more-pages.md).

# Guide

> Software development guide for MapAction

## Documentation

![alt text](https://libapps.s3.amazonaws.com/accounts/125446/images/55c8bcff18b94.png)

Image Source: https://github.com/ybouz2/project-tech/wiki/Coding-standarts

### Why to Write Documentation

(Library guides. Library Guides. (n.d.). Retrieved September 22, 2022, from https://guides.lib.berkeley.edu/ )

Documentation effectively connects humans and machines.

Why writing documentation is important:

- For you:
    - You will be using your code in 6 months
    - You want people to use your code and give you credit
    - You want to learn self-determination
    - Others would be encouraged to contribute to your code

- For others: 
    - Others can easily use your code and build upon it

- For science:
    - Advance the science
    - Encourage open science 
    - Allow reproducibility and transparency

What should you document about your research? Everything! All the data, notes, code, and materials someone else would need to reproduce your work.

Consider the following questions:

- How is your data gathered?
- What variables did you use?
- Did you use any code to clean/analyze your data?

### Best practices for Documenting your project

- Include a README file that contains
    - A brief description of the project
    - Installation instructions
    - A short example/tutorial
- Allow issue tracker for others
- Write an API documentation
    - What a function does
    - What are the function's parameters or arguments are
    - What a function returns
 
 
- Document your code
- Apply coding conventions, such as file organization, comments, naming conventions, programming practices, etc.
- Include information for contributors
- Include citation information
- Include licensing information
- Link to your e-mail address at the end
- List all the versions of the files along with the major edits you did in each version


### Sphinx

![alt text](https://www.sphinx-doc.org/en/master/_static/sphinxheader.png)

Sphinx makes it easy to create intelligent and beautiful documentation.

TLDR: See the [quickstart](https://shunsvineyard.info/2019/09/19/use-sphinx-for-python-documentation/)

Here are some of Sphinx’s major features:

- Output formats: HTML (including Windows HTML Help), LaTeX (for printable PDF versions), ePub, Texinfo, manual pages, plain text

- Extensive cross-references: semantic markup and automatic links for functions, classes, citations, glossary terms and similar pieces of information

- Hierarchical structure: easy definition of a document tree, with automatic links to siblings, parents and children

- Automatic indices: general index as well as a language-specific module indices

- Code handling: automatic highlighting using the Pygments highlighter

- Extensions: automatic testing of code snippets, inclusion of docstrings from Python modules (API docs) via built-in extensions, and much more functionality via third-party extensions.

- Themes: modify the look and feel of outputs via creating themes, and re-use many third-party themes.

- Contributed extensions: dozens of extensions contributed by users; most of them installable from PyPI.

Sphinx uses the reStructuredText markup language by default, and can read MyST markdown via third-party extensions. Both of these are powerful and straightforward to use, and have functionality for complex documentation and publishing workflows. They both build upon Docutils to parse and write documents.

### .md

Please have a quick look at [Markdown syntax](https://www.markdownguide.org/cheat-sheet/) to see how easy it is to write in your next project!


### Docstrings

### Tone

#### Use sentence case for section titles, unless rules require differently, such as the use of special names.
#### Write documentation inside the code – which Docstrings allows developers to do.
#### Use an affirmative tone that clearly states what the code does and how to use it.
#### Keep documentation simple. If something does not need to be explained, don’t explain it. Don’t over-complicate simple concepts.


## Standards

### PEP8

[PEP8](https://peps.python.org/pep-0008/) coding conventions for the Python code comprising the standard library in the main Python distribution. Please see the companion informational PEP describing style guidelines for the C code in the C implementation of Python.

This document and PEP 257 (Docstring Conventions) were adapted from Guido’s original Python Style Guide essay, with some additions from Barry’s style guide [2].

This style guide evolves over time as additional conventions are identified and past conventions are rendered obsolete by changes in the language itself.

Many projects have their own coding style guidelines. In the event of any conflicts, such project-specific guides take precedence for that project.

### Black

[Black](https://github.com/psf/black) is the uncompromising Python code formatter. By using it, you agree to cede control over minutiae of hand-formatting. In return, Black gives you speed, determinism, and freedom from pycodestyle nagging about formatting. You will save time and mental energy for more important matters.

Blackened code looks the same regardless of the project you're reading. Formatting becomes transparent after a while and you can focus on the content instead.

Black makes code review faster by producing the smallest diffs possible.

Try it out now using the Black Playground. Watch the PyCon 2019 talk to learn more.

### Flake8

[Flake8](https://flake8.pycqa.org/en/latest/) is a wrapper around these tools:

- PyFlakes

- pycodestyle

- Ned Batchelder’s McCabe script

Flake8 runs all the tools by launching the single flake8 command. It displays the warnings in a per-file, merged output.

It also adds a few features:

files that contain this line are skipped:

# flake8: noqa
lines that contain a # noqa comment at the end will not issue warnings.

you can ignore specific errors on a line with # noqa: <error>, e.g., # noqa: E234. Multiple codes can be given, separated by comma. The noqa token is case insensitive, the colon before the list of codes is required otherwise the part after noqa is ignored

Git and Mercurial hooks

extendable through flake8.extension and flake8.formatting entry points

Quickstart
See our quickstart documentation for how to install and get started with Flake8.

## Project management

### Trunk based changes

Learn why [this](https://www.atlassian.com/continuous-delivery/continuous-integration/trunk-based-development) version control management practice is common practice among DevOps teams.

### CI-friendly repositories

#### Store large files outside the repository
#### Use shallow clones for CI
#### Cache the repository on build agents
#### Choose triggers carefully
#### Favour hooking over polling
#### Be observant / sensitive to the build process


## Versions
### LST
### Bleeding
### Stable
### Pulse

## Versioning
### Versioning
### How versioning relates to releases and timelines
### A version number is essential for releasing your package. Semantic versioning is a useful method for informative versioning.
### It can be useful to store this in a separate file, so that it can be referenced from multiple places (e.g. setup.py and the main documentation).
### Git tagging can be used to mark significant points in your projects development. These tags can also be used to trigger version releases, for example using GitHub Actions.

## Files
### Example data
### To include data in your source and binary distributions
    - In the setup.py file setup(...) function call, include include_package_data = True.
    - Alongside your setup.py file, provide a MANIFEST.in file.
    - The MANIFEST.in file should list any non-python files that you wish to include distributions.
    - A MANIFEST.in file includes single files, or all files of a type, as below:
        include README.rst
        recursive-include examplepackage/examples *.csv


## Environments
### Environment images
### Gitpod

## Approach to development

### Fix code issues immediately
### Readability
### Reusability
### Single statements per line
### Keep within 80 char line
### Naming conventions
### Good imports
### Favour simplicity
### Favour data classes
### Exception handling
### Simple style example
[Style example](https://gist.github.com/sloria/7001839)


## Repositories
### Structural pattern for project / data seeding

## Testing
### Pre-commit
### Linting
### Unit-tests
[PyTest best practices](https://www.nerdwallet.com/blog/engineering/5-pytest-best-practices/)
[Python testing](https://realpython.com/pytest-python-testing/)

### Files
    License
    Readme
    Modules
    setup.py*
    Requirements.txt
    /docs
    /tests

## Types
### Typing package
### Mypy package


## Typing

## Logging
### Standardised approach

## Patterns
### Loose coupling

## Anti-patterns



## Legacy
