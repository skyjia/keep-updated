keep-updated
============

Collections and tips on how to keep your development environment updated

# Update Development Environment

## OS X

### Homebrew & Cask

- Update all Homebrew and cask packages:
```shell
$ brew doctor
$ brew update && brew upgrade brew-cask && brew cleanup && brew cask cleanup
```

## Languages


## Package Managers

### NPM

- To check if any module in global is 'old':
```shell
$ npm outdated -g
```

- Update all packages in global:
```shell
$ sudo npm update -g
```

### go packages

- Update all go packages:
```shell
$ go get -u all
```

# Common Issues

## Git

### Why does github keep asking me for repo credentials?

- http://olivierlacan.com/posts/why-is-git-https-not-working-on-github/
- http://stackoverflow.com/questions/10126381/why-does-github-keep-asking-me-for-repo-credentials
