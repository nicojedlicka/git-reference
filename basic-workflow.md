# Basic GIT workflow

## Setting up a repository

There are two options: create a new repository locally, or clone an
existing remote repository.

### Create a new local repository

```
git init .
```
This will initialise a new repository in the current working directory.

### Clone an existing repository

```
git clone https://github.com/nicojedlicka/git-reference.git
```
This will create a new working directory *git-reference* and clone the
existing remote repository into it.

## Basic snapshotting

```
git add .
```
Adds all files in the current working directory and all subdirectories
to the staging area (or index).

```
git status
```
Show the status of the current working directory and the index. All
files in the index are the ones that can be committed. The files in
the working directory (which weren't added by *git add* to the index)
won't be committed.

```
git diff
```
Shows the changes in files that are on the *WORKING DIRECTORY*
compared to the ones on the repository.

```
git diff HEAD
```
Show the changes in files that are on the *STAGING AREA* compared to
the ones on the repository.

```
git commit -m "message"
```
Commits all changes in the staging area to the repository with a given
message. If the *-m "message"* flag is not given, the default system
editor will be opened in order to type in a message.

```
git log
```
Shows the project history.

```
git checkout
```
* $ git checkout "branch name" => Change to "branch name" branch
* $ git checkout master => Change to master
* $ git checkout -b "branch name" => Create "branch name" branch and change to it
* $ git checkout -d "branch name" => Delete "branch name"

##Group Changes
####Name a series of commits and combine completed efforts  
```
$ git branch  
```
Lists all local branches in the current repository  
```
$ git branch [branch-name]  
```
Creates a new branch
```
$ git checkout [branch-name]
```
Switches to the specified branch and updates the working directory
```
$ git merge [branch]
```
Combines the specified branch’s history into the current branch
```
$ git branch -d [branch-name]
```
Deletes the specified branch

## Glossary
* Working directory :: A local directory containing a git
  repository.

* Staging area or Index :: An intermediate area where all changes to
  be committed are stored. From here, the changes can be either
  permanently committed to the repository or applied back to the
  working directory.
