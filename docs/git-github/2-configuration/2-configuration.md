[<-- Back](../1-fundamentals.md)

Git Bash
==============

When you download Git you'll get the Git Bash app, Bash is an acronym for "Bourne Again Shell.

Shells are terminal apps used as interfaces in operational systems with registered commands. Shell is the popular standard on Linux and macOS. Git Bash is the package that installs Bash, some common bash utilities, and Git on Windows operating systems.

Initializing Git
==================

For starters, when you open Git Bash for the first time you gonna need to put your username and e-mail so when you finally make a commit it will know whos the autor.

So use those commands:

```
git config --global user.email "your-email@email.com"
```
```
git config --global user.nickname 
```

If you have something you wanna share/add to your github account inside an repository _like this one_ you should create a new repository. You can do it looking at the left side in the main page on GitHub:

![New repository screenshot](https://i.imgur.com/15XkbkI.png)

Or you can click on your profile dropdown at the upperside in the right, and select "Your repositories":

![A diff new repository screenshot](https://i.imgur.com/Pxz9FZe.png)

After that you can click the "New" button:

![A diff diff new repository screenshot](https://i.imgur.com/Yt3NVgJ.png)

Inside your code folder you can start git bash app directly (and I would suggest doing that) like this:

![GitBash Screenshot](https://i.imgur.com/ow9EDCl.png)

With all of that set and ready you can go back to the Git Bash window that you opened, and initialize a local repository in your folder with this command:

```
git init
```

Now you should have in your folder a hidden folder with the name ".git".

Going on with the configuration of your repository, now you should add the repository that you created ate GitHub on your local one, you can do it with this command:

```
git remote add origin www.github.com/your-git-username/your-git-repository-name
```
At this point you are all set.

To know if you have something to commit in your folder, an code file, markdown documentation or anything you put in your local folder and need to be commited you will use:

```
git status
```
It will show you the files that you didn't commit yet or the ones read to be pushed.

When you have files to be commited you can add them choosing one of the next commands:
```
git add fileName

git add .

git add *
```
The first one adds only one at a time and the other two will add all the files to be commited.

You'll have to prepare then doing the next command, normally the message shows what you are adding with this new file or the changes on your files.

```
git commit -m "your commit message"
```
The next step is sending it to the remote repository at github and you'll do it with this:

```
git push origin main
```
If theres no conflict of files this is the finish line, but if theres a conflict you will have to solve it before you push your file/changes.

Usually the conflicts are because theres a difference between what you are pushing and the files already at the github repository and normally this happens only when you are working with someone. You're both changing and improving the code but your collegue pushed their changes first and you have to pull them so you can solve the conflict.

The pull command is this one:

```
git pull origin main
```

[Next page -->](3-commands.md)