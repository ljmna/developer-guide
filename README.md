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

*(Library guides. Library Guides. (n.d.). Retrieved September 22, 2022, from https://guides.lib.berkeley.edu/ )*

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

        You can ignore specific errors on a line with # noqa: <error>, e.g., # noqa: E234. Multiple codes can be given, separated by comma.

        Git and Mercurial hooks

        Extendable through flake8.extension and flake8.formatting entry points

See the [quickstart](https://flake8.pycqa.org/en/latest/index.html#quickstart) documentation for how to install and get started with Flake8.

## Project management

### Trunk based changes

In trunk-based development, developers push code directly into trunk. Changes made in the release branches—snapshots of the code when it's ready to be released—are usually merged back to trunk (depicted by the downward arrows) as soon as possible. In this approach, there are cases where bug fixes must be cherry picked and merged into releases (depicted by the upward arrow), but these cases are not as frequent as the development of new features in trunk. In cases where releases happen multiple times a day, release branches are not required at all, because changes can be pushed directly into trunk and deployed from there. One key benefit of the trunk-based approach is that it reduces the complexity of merging events and keeps code current by having fewer development lines and by doing small and frequent merges.

![alt text](http://qszhuan.github.io/assets/images/trunk_based_development.png)

Learn why [this](https://www.atlassian.com/continuous-delivery/continuous-integration/trunk-based-development) version control management practice is common practice among DevOps teams.

### CI-friendly repositories

*Google Cloud. 2022. DevOps tech: Continuous integration  |  DevOps capabilities  |  Google Cloud. [online] Available at: <https://cloud.google.com/architecture/devops/devops-tech-continuous-integration> [Accessed 7 October 2022].*

#### Intro

Software systems are complex, and an apparently simple, self-contained change to a single file can have unintended side effects on the overall system. When a large number of developers work on related systems, coordinating code updates is a hard problem, and changes from different developers can be incompatible.

The practice of continuous integration (CI) was created to address these problems. CI follows the principle that if something takes a lot of time and energy, you should do it more often, forcing you to make it less painful. By creating rapid feedback loops and ensuring that developers work in small batches, CI enables teams to produce high quality software, to reduce the cost of ongoing software development and maintenance, and to increase the productivity of the teams.

How to implement CI
When your organization practices CI, your developers integrate all their work into the main version of the code base (known as trunk, main, or mainline) on a regular basis. DevOps Research and Assessment (DORA) research (PDF) shows that teams perform better when developers merge their work into trunk at least daily. A set of automated tests is run both before and after the merge in order to validate that the changes don't introduce regression bugs. If these automated tests fail, the team stops what they are doing to fix the problem immediately.

CI ensures that the software is always in a working state, and that developer branches don't diverge significantly from trunk. The benefits of CI are significant: research (PDF) shows that it leads to higher deployment frequency, more stable systems, and higher quality software.

The key elements in successfully implementing continuous integration are:

Each commit should trigger a build of the software.
Each commit should trigger a series of automated tests that provide feedback in a few minutes.
To implement these elements, you need the following:

An automated build process. The first step in CI is having an automated script that creates packages that can be deployed to any environment. The packages created by the CI build should be authoritative and used by all downstream processes. These builds should be numbered and repeatable. You should run your build process successfully at least once a day.
A suite of automated tests. If you don't have any, start by writing a handful of unit and acceptance tests (PDF) that cover the high-value functionality of your system. Make sure that the tests are reliable. That way, when they fail, you know there's a real problem, and when they pass, you're confident there are no serious problems with the system. Then ensure that all new functionality is covered by tests. Those tests should run quickly, to give developers feedback as soon as possible. Your tests should run successfully at least once a day. Ultimately, if you have performance and acceptance tests, the developers should get feedback from them daily.
A CI system that runs the build and automated tests on every check-in. The system should also make the status visible to the team. You can have some fun with this—for example, you can use klaxons or traffic lights to indicate when the build is broken. Don't use email notifications; many people ignore email notifications or create a filter that hides notifications. Notifications in a chat system is a better and more popular way of achieving this.
Continuous integration, as defined by Kent Beck and the Extreme Programming community where the term originated, also includes two further practices, which are also predictive of higher software delivery performance:

The practice of trunk-based development in which developers work off trunk/mainline in small batches. They merge their work into a shared trunk/mainline at least daily, rather than working on long-lived feature branches.
An agreement that when the build breaks, fixing it should take priority over any other work.
CI requires automated unit tests. These tests should be comprehensive enough to give you confidence that the software works as expected. The tests must also run in a few minutes or less. If the automated unit tests take longer to run, developers won't want to run them frequently. If the tests are run infrequently, then a test failure can originate from many different changes, making it hard to debug. Tests that are run infrequently are hard to maintain.

Creating maintainable suites of automated unit tests is complex. A good way to solve this problem is to practice test-driven development (TDD), in which developers write automated tests that initially fail, before they implement the code that makes the tests pass. TDD has several benefits, one of which is that it ensures developers write code that's modular and easy to test, which reduces the maintenance cost of the resulting automated test suites. Many organizations don't have maintainable suites of automated unit tests and, despite that, still don't practice TDD.

#### Store large files outside the repository

GitHub limits the size of files you can track in regular Git repositories. Learn how to track or remove files that are beyond the limit. To find out more please see [here](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github).

##### About Git Large File Storage
Git LFS handles large files by storing references to the file in the repository, but not the actual file itself. To work around Git's architecture, Git LFS creates a pointer file which acts as a reference to the actual file (which is stored somewhere else). GitHub manages this pointer file in your repository. When you clone the repository down, GitHub uses the pointer file as a map to go and find the large file for you.

Using Git LFS, you can store files up to:

- GitHub Free	2 GB
- GitHub Pro	2 GB
- GitHub Team	4 GB
- GitHub Enterprise Cloud	5 GB

#### Use shallow clones for CI
*Stolee, D., 2022. Get up to speed with partial clone and shallow clone | The GitHub Blog. [online] The GitHub Blog. Available at: <https://github.blog/2020-12-21-get-up-to-speed-with-partial-clone-and-shallow-clone/> [Accessed 7 October 2022].*

As your Git repositories grow, it becomes harder and harder for new developers to clone and start working on them. Git is designed as a distributed version control system. This means that you can work on your machine without needing a connection to a central server that controls how you interact with the repository. This is only fully realizable if you have all reachable data in your local repository.

What if there was a better way? Could you get started working in the repository without downloading every version of every file in the entire Git history? Git’s [partial clone and shallow clone](https://github.blog/2020-12-21-get-up-to-speed-with-partial-clone-and-shallow-clone/) features are options that can help here, but they come with their own tradeoffs. Each option breaks at least one expectation from the normal distributed nature of Git, and you might not be willing to make those tradeoffs.

##### Shallow clones

Partial clones are relatively new to Git, but there is an older feature that does something very similar to a treeless clone: shallow clones. Shallow clones use the --depth=<N> parameter in git clone to truncate the commit history. Typically, --depth=1 signifies that we only care about the most recent commits. Shallow clones are best combined with the --single-branch --branch=<branch> options as well, to ensure we only download the data for the commit we plan to use immediately.

The object model for a shallow clone is shown in this diagram:
    
![alt text](https://github.blog/wp-content/uploads/2020/12/object-model-shallow.png?resize=800%2C414?w=800)
    
Here, the commit at HEAD exists, but its connection to its parents and the rest of the history is severed. The commits whose parents are removed are called shallow commits and together form the shallow boundary. The commit objects themselves have not changed, but there is some metadata in the client repository directing the Git client to ignore those parent connections. All trees and blobs are downloaded for any commit that exists on the client.

Since the commit history is truncated, commands such as git merge-base or git log show different results than they would in a full clone! In general, you cannot count on them to work as expected. Recall that these commands work as expectedly in partial clones. Even in blobless clones, commands like git blame -- <path> will work correctly, if only a little slower than in full clones. Shallow clones don’t even make that a possibility!

The other major difference is how git fetch behaves in a shallow clone. When fetching new commits, the server must provide every tree and blob that is “new” to these commits, relative to the shallow commits. This computation can be more expensive than a typical fetch, partly because a well-maintained server can make use of reachability bitmaps. Depending on how others are contributing to your remote repository, a git fetch operation in a shallow clone might end up downloading an almost-full commit history!

Here are some descriptions of things that can go wrong with shallow clones that negate the supposed values. For these reasons we do not recommend shallow clones except for builds that delete the repository immediately afterwards. Fetching from shallow clones can cause more harm than good!

Remember the “shallow boundary” mentioned earlier? The client sends that boundary to the server during a git fetch command, telling the server that it doesn’t have all of the reachable commits behind that boundary. The client then asks for the latest commits and everything reachable from those until hitting a shallow commit in the boundary. If another user starts a topic branch below that boundary and then the shallow client fetches that topic (or worse, the topic is merged into the default branch), then the server needs to walk the full history and serve the client what amounts to almost a full clone! Further, the server needs to calculate that data without the advantage of performance features like reachability bitmaps.
    
![alt text](https://github.blog/wp-content/uploads/2020/12/shallow-fetch-boundary.png?resize=650%2C248?w=650)

#### Cache the repository on build agents
    
*Google Cloud. 2022. DevOps tech: Continuous integration  |  DevOps capabilities  |  Google Cloud. [online] Available at: <https://cloud.google.com/architecture/devops/devops-tech-continuous-integration> [Accessed 7 October 2022].*
    
Use case example:
    
We have Bitbucket connected with Bamboo. We are planning to set up another Bamboo instance in our European office (We are in the US) but our Stash (Git) server is also located in the US. Doing Git clones or pulls from Europe to the US will take an exponential amount of time. If the repository is cached on the Bamboo server or Agents, builds would become faster because the Git/Bitbucket repository lives in a different part of the world. Where does Bamboo store the repository cache? If we are running elastic agents is the code still cached on the server somewhere after the agent expires?
    
[Repository caching](https://confluence.atlassian.com/bamkb/how-stored-git-caches-speed-up-builds-690848923.html) means that code is first fetched from the repository to a local cache and then another fetch is made from this cache to your plan's workspace that is located under the plan's working directory. Repository caching happens automatically on the Bamboo Server for its internal operations and its Local Agents and is enabled by default on Remote and Elastic Agents (it can be disabled). When using a repository cache, on the first run of a plan, Bamboo performs a full clone and stores the data in a local cache directory and completes the build. On subsequent builds, Bamboo does a git fetch from the remote repository to see if there are additional changes and if so, updates the local cache. Similar to the first run, the data for the plan is then checked out from the local cache. Hence, a faster checkout. To get a better understanding, you can enable "verbose logs" located under the advanced settings of the repository, trigger a build, and follow the sequence of events.

Depending on the type of workload such as in large repositories; multiple plans using the local cache and producing a disk bottleneck, or also on very active repositories whose Build plans have a requirement to be linked to the latest changes, etc, it may be necessary to not use any caching and instead use the latest version from the repository. You can disable the repository caching on agents by unsetting the "Enable repository caching on agents" option on the Repository configuration.

The git cache is used even when different plans checkout the same repository to prevent duplicate and unnecessary checkouts of the same repository between plans. 
    
#### Choose triggers carefully

##### Skipping a build trigger
In some cases, you may want to make a change to your source code but you don't want to invoke a build. For example, you might not want to invoke a build when you update documentation or configuration files.

In such scenarios, you can include [skip ci] or [ci skip] in the commit message, and a build will not be invoked.

If you want to run a build on that commit later, use the Run trigger button in the Triggers page.
    
#### Favour hooking over polling
    
![alt text](https://dz2cdn1.dzone.com/storage/temp/5679158-youre-better-than-this-polling-short.gif)
    
*dzone.com. 2022. Webhooks vs. Polling: You're Better Than This - DZone Integration. [online] Available at: <https://dzone.com/articles/webhooks-vs-polling-youre-better-than-this-1> [Accessed 7 October 2022].*
    
##### Be Nice…to Your Servers
While polling and webhooks both accomplish the same task, webhooks are far more efficient. Zapier found that over 98.5% of polls are wasted. In contrast, webhooks only transfer data when there is new data to send, making them 100% efficient. That means that polling creates, on average, 66x more server load than webhooks. That’s a lot of wasted time, and if you’re paying per API call, a whole lot of wasted money.
    
    
#### Be observant / sensitive to the build process
    
Attentiveness to the build process will enable optimisation of build-times. The virtue of this is that cummulatively much time will be saved, it could also be financially beneficial in terms of cloud or server billing and resources. This can be acheived in certain instances via caching files, analysing slow downloads or dependencies, looking for possibilities to parallelize and/or concurrently run elements of the build, time slow areas of builds and deduce the root causes and whether they can be improved upon.
    
See [this](https://jcdan3.medium.com/4-ways-to-speed-up-your-github-action-workflows-a0b08067a6c6) post for some introductory information on enhancing your next Github Actions build for example.  


## Dependency versions
    
### LTS

*En.wikipedia.org. 2022. Long-term support - Wikipedia. [online] Available at: <https://en.wikipedia.org/wiki/Long-term_support> [Accessed 7 October 2022].*
    
Long-term support (LTS) is a product lifecycle management policy in which a stable release of computer software is maintained for a longer period of time than the standard edition. The term is typically reserved for open-source software, where it describes a software edition that is supported for months or years longer than the software's standard edition.

Short term support (STS) is a term that distinguishes the support policy for the software's standard edition. STS software has a comparatively short life cycle, and may be afforded new features that are omitted from the LTS edition to avoid potentially compromising the stability or compatibility of the LTS release
    
LTS applies the tenets of reliability engineering to the software development process and software release life cycle. Long-term support extends the period of software maintenance; it also alters the type and frequency of software updates (patches) to reduce the risk, expense, and disruption of software deployment, while promoting the dependability of the software. It does not necessarily imply technical support.
    
### Bleeding-edge
    
*Investopedia. 2022. Bleeding Edge Technology. [online] Available at: <https://www.investopedia.com/terms/b/bleeding-edge-technology.asp#:~:text=our%20editorial%20policies-,What%20Is%20Bleeding%20Edge%20Technology%3F,in%20most%20cases%2C%20the%20consumer.> [Accessed 7 October 2022].*

[Bleeding-edge technology](https://en.wikipedia.org/wiki/Emerging_technologies#In_the_media) refers to a type of technology released to the public even though it has not been thoroughly tested and may be unreliable. Bleeding edge technology usually comes with a degree of risk and expense for the end-user—in most cases, the consumer. 

Bleeding edge technology has a certain amount of risk, with early adopters facing a significant downside if the technology misses the mark.
Consumers may not be that familiar with the product, it may not be thoroughly tested and it may have glitches that can't be quickly or easily fixed.
Consumers that become early adopters could lose money, time, or sensitive information if the technology fails to deliver on its promises.
    
### Stable

*En.wikipedia.org. 2022. Software release life cycle - Wikipedia. [online] Available at: <https://en.wikipedia.org/wiki/Software_release_life_cycle#:~:text=Also%20called%20production%20release%2C%20the,This%20release%20goes%20to%20production.> [Accessed 7 October 2022].*
    
#### Stable release
 
Also called production release, the stable release is the last release candidate (RC) which has passed all stages of verification and tests. The remaining bugs are considered as acceptable. This release goes to production.
    
Always favour stable releases when using third party libraries, dependencies, drivers, or other software of any kind.

Some software products (e.g. Linux distributions) also have long term support (LTS) releases which are based on full releases that have already been tried and tested, and receive only security updates. This allows developers to allocate more time toward product development instead of updating code or finding and fixing newly introduced bugs due to outdated assumptions about the used system, language or underlying libraries.

### Pulse
    
Github [pulse](https://github.blog/2013-04-18-get-up-to-speed-with-pulse/) provides a great way to check the current or historical activity on a particular project or piece of software. This can be a good indicator of how well supported or maintained it is. A worthy consideration when establishing a preferable choice from a selection of competitors for a particular task, is how actively maintained that choice of software is.

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
### Docker
### Python

#### Python Environment Management Best Practices
*Perlton, C., 2022. Python Environment Management Best Practices. [online] Blog.inedo.com. Available at: <https://blog.inedo.com/python-environment-management-best-practices> [Accessed 12 October 2022].*

When you need to deploy and run Python scripts that others have written, it's important to run those in a well-managed Python environment. Otherwise, you run the risk of dependency conflicts, disorganization, and once-working scripts suddenly failing.

There are several choices to make when managing environments for your Python projects, this article will explain best practices to follow and common mistakes to avoid when doing so.

##### What is a Python Environment?
By default, pip installs packages onto a global Python environment with a Python interpreter, a standard library, and pre-installed packages. Functionally this means that all projects on a system will use the same directories to store and retrieve packages.

Virtual environments are often preferred due to their ability to keep projects separate. Global environments are best used when using Python for server management, running a quick Python script, or automating a server. Meanwhile, virtual environments are more appropriate for package management and complex Python projects. 

##### Virtual Environments
In the Python world, a virtual environment is a folder containing packages and other dependencies that a Python project needs. Contrary to a global environment, virtual environments are isolated coding spaces where Python packages can be installed, upgraded, and used. When you install or upgrade a package, the old versions stay installed in your directory, so different virtual environments can utilize different package versions. You can also specify the specific version of Python you want for your project. You have free choice between starting Python 2.7, Python 3.6, Python 3.7, Anaconda 4.4.0, and so on.

###### Why the need for virtual environments?

Virtual environments prevent dependency, version, and permission conflicts by keeping Python projects separate. Global environments run the risk of causing a dependency conflict that may prevent your application from building due to packages being dependent on specific versions of other packages.

Consider two Python projects in a global environment that require NumPy 1.10 and NumPy 1.20 respectively. Python can’t differentiate between versions in the “site-packages” directory. So, both version 1.10 and version 1.20 would reside in the same directory with the same name.

Global environments often get cluttered with dozens of different packages that were installed for various projects. There is no great way to organize or manage these in a global environment, making it difficult to thoroughly test your application against a specific set of packages with known versions.

##### Best Practices for Managing Python Environments
✔ Use a Virtual Environment
Virtual environments should always be used unless Python is being utilized for server management or running simple scripts. There are many different Python package managers and virtual environments to choose from that come with a variety of different features. It’s important to carefully consider the best virtual environment for your Python project.

Virtualenv is arguably the most popular and beginner-friendly Python virtual environment. It comes preinstalled with Python 2 as virtualenv and Python 3 as venv. The popular virtualenvwrapper extension adds additional features like tab completion and a single command to switch between environments.

Pipenv is a package and virtual environment management tool that aims to integrate the functionality of Pip and virtualenv into a single tool. It’s a great tool with helpful features but it’s more complex to learn than virtualenv.

Poetry is a feature-rich Python tool for project dependency management. It’s faster than most virtual environment tools and comes with a powerful CLI for managing Python projects.

Conda is a multi-purpose package and environment management system that supports both Python and other languages like Ruby, Scala, R, and C/C++. It’s used to create, save, load, and switch between environments in your local machine. Conda is favored by data scientists and comes pre-installed in both anaconda and miniconda.

##### ✔ Use Requirement.txt Files
The best way to make your work reproducible and keep your environment consistent is to include a requirments.txt file in your project’s root directory. A requirements.txt file contains a list of all the packages present in a project. Utilizing requirements.txt files can be done in two simple steps:

Use pip freeze to output installed packages suitable for a requirements file:
C:\> py -m pip freeze
docutils==0.11
Jinja2==2.7.2
MarkupSafe==0.19
Pygments==1.6
Sphinx==1.2.2
Generate a requirements.txt file and then install it into another environment:
env1\bin\python -m pip freeze > requirements.txt
env2\bin\python -m pip install -r requirements.txt
Requirements.txt files help ensure consistency across installations, deployments, and developers. They also help manage Python dependencies!

##### ✔ Use a Separate Virtual Environment for Each Project
Ideally, you should have one new virtual environment for every Python-based project you work on. The main purpose of this is to keep the dependencies of every project isolated from both the system and each other.

If you have multiple projects that have roughly the same requirements, it might seem like a good idea to create a single virtual environment that both projects can share. The problem with this is that one of the projects could suddenly have requirements that break another project. The whole point of virtual environments is to isolate each project from other projects and their quirks.

The disk space and convenience saved is marginal and simply not worth it. Furthermore, using requirements.txt files makes it easy to set up a virtual environment for a project and install what it needs with a couple of commands.

##### X Don’t Forget to Activate Your Python virtual Environment
Before a virtual environment can be used in a particular shell session, it has to be activated. Forgetting to active a virtual environment or activating the wrong one is an all too common mistake.

Once activated, virtual environments are treated as the default Python instance until it’s deactivated by running the deactivate command. Keep in mind that activating a virtual environment is for a specific session and not for the system as a whole.

##### X Don’t Use >= for Package Versioning in a Python Virtual Environment
When utilizing requirements.txt files, you should specify packages with exact version numbers. For example, use mypackage==3.2, not mypackage>=3.2.

If you don’t use specific versions of packages it will prevent one of the main benefits of using virtual environments: predictable builds. If you use >= instead of ==, there is no guarantee you, or someone else, will end up with the same version when the environment needs to be recreated.



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
