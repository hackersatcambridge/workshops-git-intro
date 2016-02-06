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
Let's make a new directory that will contain our practice Git project, and move inside that new directory.
```
$ mkdir practice-git
$ cd practice-git
```
To have Git start tracking the contents of the directory, run

```
$ git init
Initialized empty Git repository in /path/to/your/practice-git/.git
```

### Staging Files

### Commits

### Remotes
