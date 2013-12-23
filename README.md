# git-cheatsheet

A personal cheatsheet for Git

## Installation

Install git

```sh
sudo apt-get install git
```

## New repo

Create a new git repository

```sh
# Creat a new repo called 'foo'
git init foo

# Change into it
cd foo
```

Add a `[user]` section to `.git/config` with the email address to be used for this repo rather than the global git config email
```
[user]
	name = Nokome Bentley
	email = nokome.bentley@example.com
```

Add Github as a remote

```sh
git remote add origin git@github.com:nokome/foo.git
```

## git-flow

`git-flow` is a "collection of Git extensions to provide high-level repository operations for Vincent Driessen's branching model". It can be useful for projects which have distinct release cycles. It may not be so useful for projects with continuous deployment.

* [Vincent Driessen's branching model](http://nvie.com/git-model)
* [Why aren't you using git-flow?](http://jeffkreeftmeijer.com/2010/why-arent-you-using-git-flow/)
* [Atlassian's guide](https://www.atlassian.com/git/workflows#!workflow-gitflow)
* [Daniel Kummer's Gitflow cheatsheet](http://danielkummer.github.io/git-flow-cheatsheet/)

Install [git-flow](https://github.com/nvie/gitflow)

```sh
sudo apt-get install git-flow
```

Initialise git-flow for this repo with the default values

```sh
git flow init -d
```
