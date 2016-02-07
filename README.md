# Intro to Git
## What is Git 

## The Workshop
### Installing Git
- Windows: Download from https://git-scm.com/download/win
- OS X: Download from https://git-scm.com/download/mac OR
 install Homebrew http://brew.sh/ and run `$ brew install git` OR
 simply run `$ git` and you will be prompted to install Xcode Command Line Tools,
 which includes Git.
- Linux: `$ yum install git` on Fedora or `$ apt-get install git` on Debian-based distributions.

### Configuration
You need to introduce yourself to Git so that it can attribute code contributions to you. Run

`$ git config --global user.name "Your Name"`

and

`$ git config --global user.email your@email.com`

Doing this doesn't sign you up for anything and you won't get emails because of it.
It simply sets two variables in a global configuration file on your computer for later use.

### Making a Repository
Login at https://github.com/ and make a new repository with the button on the rightmost column.
Make sure to *check the box for initializing the repository with a README*.
Right now the repository only lives on GitHub's remote servers. To get it onto your local machine,
go to the directory you would like the project to be placed in and run
```
$ git clone <url of your github repository>
```
This will make a new directory that contains the project you have just cloned. Go into that directory
and run
```
$ git status
```
which should print
```
On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working directory clean
```
Congratulations, you've just created and cloned your first Git repository.

### Making Changes and Staging Files
Let's give Git some changes to track.
Using your favorite editor, write `Hello World` in the next empty line of the README file.

If you run `$ git status` you will see something like
```
On branch master
Your branch is up-to-date with 'origin/master'.
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
```
Run
```
$ git add README.md
```
to stage the README file.

### Committing and Pushing
Once changes have been staged, we can commit them to the local repository with 
```
$ git commit -m "Initial commit."
```
The `-m` flag signals that the string in double quotes following it is the *commit message*,
a short description of the changes in the commit.

Finally, to get your changes back onto GitHub, simply run
```
$ git push
```
You've made it through your first iteration of the edit-stage-commit-push cycle that is core to Git!

## Best Practices
### Commit Messages
