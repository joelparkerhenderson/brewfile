# Brewfile for macOS Homebrew bundle software management

<img src="README.png" alt="Brewfile" style="width: 100%;"/>

We use Homebrew a.k.a. brew to install software on our macOS computers.


## Introduction

This repository has our Brewfile, which manages much of the software that we use for projects.

This Brewfile helps us install:

  * Hundreds of desktop applications, such as browsers, players, editors, etc.
  * Hundreds of system utilities, such as command line interfaces, sysop helpers, etc.
  * Dozens of programming capabilties, such as languages, toolchains, servers, etc.

To learn about Brewfile capabilties, please see:

  * http://brew.sh/
  * http://homebrew-file.readthedocs.io/
  * https://github.com/Homebrew/homebrew-bundle

Using a Brewfile helps us with our Infrastructure as Code (IaC) initiatives.

Feedback welcome. Pull requests welcome.


## Usage

To use this Brewfile via `brew bundle`:

```sh
$ brew bundle
```

To use this Brewfile via `brew-file`, which has more capabilties than bundle:

```sh
$ brew install rcmdnk/file/brew-file
$ brew file init                    
Do you want to set a repository (y)? ((n) for local Brewfile). [y/n]: y
Set repository, "non" for local Brewfile,
<user>/<repo> for github repository,
or full path for the repository: joelparkerhenderson/brewfile
```
