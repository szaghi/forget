<a name="top"></a>

# forget [![GitHub tag](https://img.shields.io/github/tag/szaghi/forget.svg)]() [![Join the chat at https://gitter.im/szaghi/forget](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/szaghi/forget?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

[![License](https://img.shields.io/badge/license-GNU%20GeneraL%20Public%20License%20v3,%20GPLv3-blue.svg)]()
[![License](https://img.shields.io/badge/license-BSD2-red.svg)]()
[![License](https://img.shields.io/badge/license-BSD3-red.svg)]()
[![License](https://img.shields.io/badge/license-MIT-red.svg)]()

[![Status](https://img.shields.io/badge/status-unstable-red.svg)]()
[![Build Status](https://travis-ci.org/szaghi/forget.svg?branch=master)](https://travis-ci.org/szaghi/forget)
[![Coverage Status](https://img.shields.io/codecov/c/github/szaghi/forget.svg)](http://codecov.io/github/szaghi/forget?branch=master)

### forget, FORtran Git Template

A template/skeleton for starting new free Fortran projects handled by git with the exploitation of GitHub, Travis, Codecov & Co.

#### A taste of forget

```shell
git clone https://github.com/szaghi/forget free_fortran_project
cd free_fortran_project
rm -rf .git
sed 's/forget/free_fortran_project/g'
git init
git add .
git commit -m "init versioning"
```

#### Issues

[![GitHub issues](https://img.shields.io/github/issues/szaghi/forget.svg)]()
[![Ready in backlog](https://badge.waffle.io/szaghi/forget.png?label=ready&title=Ready)](https://waffle.io/szaghi/forget)
[![In Progress](https://badge.waffle.io/szaghi/forget.png?label=in%20progress&title=In%20Progress)](https://waffle.io/szaghi/forget)
[![Open bugs](https://badge.waffle.io/szaghi/forget.png?label=bug&title=Open%20Bugs)](https://waffle.io/szaghi/forget)

#### Compiler Support

[![Compiler](https://img.shields.io/badge/GNU-v6.1.1+-brightgreen.svg)]()
[![Compiler](https://img.shields.io/badge/Intel-v16.1+-brightgreen.svg)]()
[![Compiler](https://img.shields.io/badge/IBM%20XL-not%20tested-yellow.svg)]()
[![Compiler](https://img.shields.io/badge/g95-not%20tested-yellow.svg)]()
[![Compiler](https://img.shields.io/badge/NAG-not%20tested-yellow.svg)]()
[![Compiler](https://img.shields.io/badge/PGI-not%20tested-yellow.svg)]()

---

[What is forget?](#what-is-forget) | [Main features](#main-features) | [Copyrights](#copyrights) | [Download](#download) | [Compilation](#compilation) | [Documentation](#documentation) | [References](#references)

---

## What is forget?

> **forget** to repeat the same commands everytime your new Fortran project born: do it one-time and make **git** do it for you the next times :smile:

> forget is a remote-hosted (on GitHub) git-repository template/skeleton that provides a bunch of (ready to use) files for handling modern Fortran projects exploiting the best helpers available on web. In particular the template offers:

### How to use

1. clone the forget repository, `git clone https://github.com/szaghi/forget new_fortran_project`
1. to be continued...

To be completed.

Go to [Top](#top)

## Main features

> forget is just template providing

+ [ ] semi-sane project template:
  + [ ] CLI bash script for configuring the template;
  + [x] semi-sane, almost-cluttered, but aesthetically nice, project README.md;
  + [ ] Travis CI configuration file exploiting [Travis CI](https://travis-ci.org) for:
    + [ ] building and testing your Fortran project;
    + [ ] making coverage analysis;
    + [ ] making API documentation (by means of the great [FORD](https://github.com/cmacmackin/ford)) and deploying it on GitHub pages;
  + [ ] Codecov configuration file exploiting [Codecov](https://codecov.io) analyzer;
  + [ ] fully-inclusive, semi-crazy set of FOSS licenses covering almost all scenario definable as *do wathever you want with this project*;
  + [ ] opinionated CONTRIBUTING.md guidelines;
  + [ ] ready to use FORD configuration file;
  + [ ] semi-sane, ready to use .gitingore;
  + [ ] semi-sane tree-sources structure;
  + [ ] agnostic `fobos` file to auto-magically build your Fortran project with the coolest Fortran building tool... [FoBiS.py](https://github.com/szaghi/FoBiS)
  + [ ] agnostic bash script to automatically run all your tests;
* [x] Test Driven Developed (TDD);
* [x] collaborative developed;
* [x] well documented;
* [x] free!

Any feature request is welcome.

Go to [Top](#top)

## Copyrights

forget is an open source project, it is distributed under a multi-licensing system:

+ for FOSS projects:
  - [GPL v3](http://www.gnu.org/licenses/gpl-3.0.html);
+ for closed source/commercial projects:
  - [BSD 2-Clause](http://opensource.org/licenses/BSD-2-Clause);
  - [BSD 3-Clause](http://opensource.org/licenses/BSD-3-Clause);
  - [MIT](http://opensource.org/licenses/MIT).

Anyone is interest to use, to develop or to contribute to forget is welcome, feel free to select the license that best matches your soul!

More details can be found on [wiki](https://github.com/szaghi/forget/wiki/Copyrights).

Go to [Top](#top)

## Download

forget home is at [https://github.com/szaghi/forget](https://github.com/szaghi/forget). To download all the source files you can:

+ clone recursively this repository: `git clone --recursive https://github.com/szaghi/forget`
+ download the latest master-branch archive at [https://github.com/szaghi/forget/archive/master.zip](https://github.com/szaghi/forget/archive/master.zip)
+ download a release archive at [https://github.com/szaghi/forget/releases](https://github.com/szaghi/forget/releases)

Go to [Top](#top)

## Compilation

forget is a modern Fortran project thus a modern Fortran compiler is need to compile the project. The project is modular, namely it exploits Fortran modules. As a consequence, there is compilation-cascade hierarchy to build the project. To correctly build the project the following approaches are supported

+ [Build by means of FoBiS](#build-by-means-of-fobis): full support;
+ [Build by means of GNU Make](#build-by-means-of-gnu-make): to be implemented.
+ [Build by means of CMake](#build-by-means-of-cmake): to be implemented.

The FoBiS building support is the most complete, as it is the one used for the developing forget.

### Build by means of FoBiS

A `fobos` file is provided to build the project by means of the Fortran Building System [FoBiS.py](https://github.com/szaghi/FoBiS).

#### Build all programs

Type

```shell
FoBiS.py build
```

After (a successful) building a directory `./exe` is created containing all the compiled programs found recursively in the tree project.

### Build by means of GNU Make

To be implemented.

### Build by means of CMake

To be implemented.

Go to [Top](#top)

---

## Documentation

Besides this README file the forget documentation is contained into its own [wiki](https://github.com/szaghi/forget/wiki). Detailed documentation of the API is contained into the [GitHub Pages](http://szaghi.github.io/forget/index.html) that can also be created locally by means of [ford tool](https://github.com/cmacmackin/ford).

Go to [Top](#top)
