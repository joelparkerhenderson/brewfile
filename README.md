# Brewfile for macOS Homebrew software management

<img src="README.png" alt="Brewfile" style="width: 100%;"/>

We use Homebrew a.k.a. Brew to install software on our macOS computers.

See http://brew.sh/ and http://homebrew-file.readthedocs.io/

This repository has our Brewfile, which has everything we use in all our projects.

This includes plenty of desktop applications, system tools, programming languages, and more.

Using a Brewfile helps us with our Infrastructure as Code (IaC) initiatives.

Feedback welcome. Pull requests welcome.

To install brew-file and use this Brewfile:

```sh
$ brew install rcmdnk/file/brew-file
$ brew file init
Do you want to set a repository (y)? ((n) for local Brewfile). [y/n]: y
Set repository, "non" for local Brewfile,
<user>/<repo> for github repository,
or full path for the repository: joelparkerhenderson/Brewfile
```
