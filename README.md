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
Using your favorite editor, write `Hello World` in line 3 of the README file.

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

### Branching and Merging
Find somebody near you and introduce yourselves! We will now simulate collaborating on a project.
First, one person in each pair should add the other as a collaborator to the GitHub repository from earlier.
![Adding collaborators.](assets/add-collaborators.png)
If you were the one added, make sure you clone that repository.

Next, each person should make a branch that is named with your own name in the shared repositories by using
```
$ git branch <your name>
```
That creates the branch, but if you run `$ git branch` you will find that you are still on the master branch.
To move to a different branch, run
```
$ git checkout <branch name>
```
In the future, this can be accomplished in one go with `$ git checkout -b <branch name>`, but it is important
to be aware of Git's branch management commands under `git branch`.

Once you've successfully moved to your new branch, write `contributors: <your name>` in the 4th line of the
README and then add-commit-push your changes to GitHub.

The owner of the repository should then pull the changes (partner, look over their shoulder while they do this)
```
$ git pull
```
You'll notice that your partner's branch have been pulled to your local repository. To finalize these changes,
checkout your partner's branch the master branch, then run
```
$ git merge <branch name>
```
for both you and your partner's branches.

The second time you merge, you will get a *merge conflict* since both you and your partner have edited the same line.
The areas where the two branches conflict are marked out like so:
```
<<<<<<< HEAD
contributors: foo
=======
contributors: bar
>>>>>>> bar
```
You will not be able to merge until all structures like this are resolved in the code. In this case, you're both
collaborators so resolve the merge conflict by listing both of your names in the collaborators lines.

Once you have finished resolving, add-commit-push again. If you were not the one doing the merging, 
you should `$ git pull` to receive the changes in your local repository.

Feel free to spend some extra time making new branches, committing things, and merging back and forth!

## Best Practices
### Branching Structure
### Pull Requests
### Commit Messages

## Tips
### Aliasing
