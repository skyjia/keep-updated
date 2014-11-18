keep-updated
============

Collections and tips on how to keep your development environment updated.

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](http://doctoc.herokuapp.com/)*

- [Update Development Environment](#update-development-environment)
  - [OS X](#os-x)
    - [Homebrew & Cask](#homebrew-&-cask)
  - [Languages](#languages)
    - [go-lang](#go-lang)
  - [Package Managers](#package-managers)
    - [NPM](#npm)
    - [go packages](#go-packages)
- [Common Issues](#common-issues)
  - [Git](#git)
    - [Why does github keep asking me for repo credentials?](#why-does-github-keep-asking-me-for-repo-credentials)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->



## Update Development Environment

### OS X

#### Homebrew & Cask

- Update all Homebrew and cask packages:
```shell
$ brew doctor
$ brew update && brew upgrade brew-cask && brew cleanup && brew cask cleanup
```

### Languages

#### go-lang

- Update go from source:
```shell
$ cd go/src
$ hg pull
$ hg update release
$ ./all.bash
```
Refer to: http://golang.org/doc/install/source


### Package Managers

#### NPM

- To check if any module in global is 'old':
```shell
$ npm outdated -g
```

- Update all packages in global:
```shell
$ sudo npm update -g
```

#### go packages

- Update all go packages:
```shell
$ go get -u all
```

## Common Issues

### Git

#### Why does github keep asking me for repo credentials?

- http://olivierlacan.com/posts/why-is-git-https-not-working-on-github/
- http://stackoverflow.com/questions/10126381/why-does-github-keep-asking-me-for-repo-credentials
