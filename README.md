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

### Initialization
Make a new directory that will contain your practice Git project, and `cd` into that new directory.
```
$ mkdir practice-git
$ cd practice-git
```
To have Git start tracking the contents of the directory, run

```
$ git init
Initialized empty Git repository in /path/to/your/practice-git/.git
```

Congratulations, you have just created your first Git repository!

### Staging Files
Let's give Git some files to track. Create a new text file
`$ touch README.md`
and, using your favorite editor, write `Hello World` in the first line.

If you run `$ git status` you will see something like
```
$ git status
On branch master

Initial commit

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	README.md

nothing added to commit but untracked files present (use "git add" to track)
```
Run `$ git add README.md` to stage the readme file.

### Committing Changes
Once changes have been staged, we can commit them to the local repository with 
```
$ git commit -m "Initial commit."
```
The `-m` flag signals that the string in double quotes following it is the *commit message*,
a short description of the changes in the commit.

### Remotes

## Best Practices
### Commit Messages
