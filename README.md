![alt text](https://mapaction.org/wp-content/themes/mapaction/images/logo.svg)

[Documentation Site](https://stellular-basbousa-d782de.netlify.app/)

# Contribute

It is recommended to install `docsify-cli` globally, which helps initializing and previewing the website locally.

```bash
npm i docsify-cli -g
```

### Writing content

- `README.md` acts as the home page

You can easily update the documentation in `README.md`, of course you can add [more pages](more-pages.md).

### Preview your site

Run the local server with `docsify serve`. You can preview your site in your browser on `http://localhost:3000`.

```bash
docsify serve docs
```

?> For more use cases of `docsify-cli`, head over to the [docsify-cli documentation](https://github.com/docsifyjs/docsify-cli).

# Guide

> Software development guide for MapAction

## Documentation
### Sphinx
### .md

### Docstrings

### Tone

#### Use sentence case for section titles, unless rules require differently, such as the use of special names.
#### Write documentation inside the code – which Docstrings allows developers to do.
#### Use an affirmative tone that clearly states what the code does and how to use it.
#### Keep documentation simple. If something does not need to be explained, don’t explain it. Don’t over-complicate simple concepts.


## Standards

### PEP8

### Black

### Flake8

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
