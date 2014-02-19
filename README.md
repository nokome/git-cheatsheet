# git-cheatsheet

A personal cheatsheet for Git

## Installation

Install [git](http://git-scm.com/)

```sh
sudo apt-get install git
```

Install [Legit](http://www.git-legit.org/).
Legit provides a git shortcuts for a simple branching workflow. 
An alternative is [git-flow](https://github.com/nvie/gitflow) based on [Vincent Driessen's branching model](http://nvie.com/git-model) but I find that somewhat convoluted for my needs.

```sh
sudo pip install legit
install legit
```

## Creating

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

## Branching

`git sprout [<branch>] <new-branch>`
    Creates a new branch off of the specified branch.
    Swiches to it immediately.

`git publish <branch>`
    Publishes specified branch to the remote.

`git branches`
    Get a nice pretty list of available branches.

`git sync [<branch>]`
    Syncronizes the given branch. Defaults to current branch.
    Stash, Fetch, Auto-Merge/Rebase, Push, and Unstash.
    You can only sync published branches.

`git switch <branch>`
    Switches to specified branch.
    Defaults to current branch.
    Automatically stashes and unstashes any changes.

`git harvest [<branch>] <into-branch>`
    Auto-Merge/Rebase of specified branch changes into the second branch.

`git graft <branch> <into-branch>`
    Auto-Merge/Rebase of specified branch into the second branch.
    Immediately removes specified branch. You can only graft unpublished branches.

`git unpublish <branch>`
    Removes specified branch from the remote.


## Tagging

```
git tag -a '0.x' -m '0.x'
git push --tags
```