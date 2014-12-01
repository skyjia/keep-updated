keep-updated
============

Collections and tips on how to keep your development environment updated.

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](http://doctoc.herokuapp.com/)*

- [Update Development Environment](#update-development-environment)
  - [OS X](#os-x)
    - [Homebrew & Cask](#homebrew-&-cask)
    - [CocoaPods](#CocoaPods)
  - [Languages](#languages)
    - [go-lang](#go-lang)
  - [Development Tools](#development-tools)
    - [Vim](#vim)
    - [GUN Emacs](#gun-emacs)
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

#### CocoaPods
CocoaPods is the dependency manager for Objective-C projects:

- Intall:
```shell
$ sudo gem install cocoapods
```

- Create a Podfile in your project folder:
```shell
$ touch Podfile
```
One Simple Podfile example:
```shell
source 'https://github.com/CocoaPods/Specs.git'
pod 'AFNetworking', '~> 1.0'
```

- Using CocoaPods:
```shell
$ pod install
```
After CocoaPods download the dependent libraries, will create a new xcode workspace for you. You will see " From now on use `xxx.xcworkspace`. Your original target will add a lib called libPods.a.

- Update dependencies:
```shell
$ pod update
```
>For more usage, read cocoapods website.
>Refer to: http://cocoapods.org

### Languages

#### go-lang

- Update go from source:
```shell
$ cd go/src
$ hg pull
$ hg update release
$ ./all.bash
```
> Refer to: http://golang.org/doc/install/source

### Development Tools

#### Vim

- Update plugins managed by [pathogen](https://github.com/tpope/vim-pathogen) with shell script:
```shell
#!/bin/bash
cd ~/.vim/bundle
for i in `ls`; do
  cd "$i"
  git pull
cd ..
done
```

#### GUN Emacs

- Update GUN Emacs packages managed by [Prelude](https://github.com/bbatsov/prelude):  
  Just run `M-x package-list-packages RET U x` in Emacs

> Refere to https://github.com/bbatsov/prelude#updating-prelude

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
