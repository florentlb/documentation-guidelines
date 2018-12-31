---
id: contributing_doc_guidelines
title: Contributing to guidelines
sidebar_label: Contributing to guidelines
---

There are two ways for contributing to this documentation:

* On each page, an **Edit** button allows to create a Pull Request with suggested changes.
* Setup Docusaurus on your machine. See <a href="#cloning">Cloning the repository</a>.

## <a name="cloning"></a>Cloning the repository

To be able to clone the repository, you need to have a GitHub account.

1. Access [the repository](https://github.com/florentlb/documentation-guidelines) on GitHub.
2. Select **Clone or download** to download a local copy of the project onto your machine.

> **Note**: You can also fork the project.

You can now edit the files or create pull requests, at your convenience.

## Running a local version of the site

Before being able to generate a local version of the site, you need to install **node** and **yarn** on your local machine.


1. Open your command line tool and browse to your local copy of the repository. For example: ``cd C:\git\documentation-guidelines``.
2. Run ``yarn`` to load the needed dependencies.
3. Go to the website directory using ``cd website``.
4. Run the site locally by using ``yarn start``.

The website is then built locally. Pages that are already created are reloaded when a modification is made. For new files or some specific assets, you need to rebuild the site to see the changes.
