# Tutorial Steps Completed (plus notes)

Full details: [Tutorial](https://git-scm.com/book/en/v2)

## Frequently used Git commands

Also see: [more commands](https://git-scm.com/docs/gittutorial)

$ cd [file path for repository] # command to enter a given repository (e.g., cd C:/Users/edens1/Git_ETSmith/)
$ git status # command to check the status of repository (of whichever branch is being worked on)
$ git init # command to initialise an empty Git repository (or re-initialise an existing repository)
$ git clone [file path of the repository to be cloned] # command to clone an existing repository, e.g., $ git clone [url of repository](https://github.com/tariq-eden/RAT)
$ git remote add shortname url # e.g., git remote add github-rat [url of repository](https://github.com/tariq-eden/RAT)
$ git branch [name of branch] # command to create a branch of the repository
$ git checkout [name of branch] # command to switch to an existing branch (this moves HEAD to point to the new branch) - note 'checkout' sometimes is 'switch'.
$ git checkout main # command to return to main branch
$ git checkout [name of branch] # command to switch back to an existing branch
$ git merge [branch name] # command to use when in the main branch merge a given working branch into the main branch. (Note, if there are conflicts, markers will be left in the files (type $ git diff to show what the differences are). After resolving conflicts, type $ git commit -a (to commit the results of the merge). $ gitk will show a graphical representation of the resulting history. Note, when commiting, in vim, you'll be asked to 'type a commit message' to do this  press i to start entering text and save by pressing esc and :wq which would commit the message you entered. To quit without committing, you can do :q instead of the :wq as mentioned above.
$ git add [filename] # A multipurpose command to “add precisely this content to the next commit”
$ git add . # command to take a snapshot of the contents of all files under the current directory (note the .)
$ git commit -m 'commit message for staged changes' # command to commit staged changed
$ git commit -a -m 'commit message for all changes' # command to commit ALL changes, regardless of if staged or not.
$ git rm [filename] # command to stage files for removal from the repository
$ git rm --cached [filename] # command to remove files from the staging while keeping it in the working tree (i.e., so the file reamins on your hard drive but Git doesn't try to track it)
$ git mv [old-filename] [new-filename] # command to rename a file, e.g., $ git mv Draft1.md Draft2.md
$ git log # command to view the commit history (lists the commits made in that repository in reverse chronological order) - note that there are a bunch of variations on this command see:[Tutorial section](https://git-scm.com/book/en/v2/Git-Basics-Viewing-the-Commit-History).
$ git remote # command to view list of remote servers
$ git pull name (Note: The git pull command is essentially a git fetch immediately followed by a git merge in most cases. If you have a tracking branch set up as demonstrated in the last section, either by explicitly setting it or by having it created for you by the clone or checkout commands, git pull will look up what server and branch your current branch is tracking, fetch from that server and then try to merge in that remote branch. Generally it’s better to simply use the fetch and merge commands explicitly as the magic of git pull can often be confusing. The git fetch command will fetch all the changes on the server that you don’t have yet, it will not modify your working directory at all. It will simply get the data for you and let you merge it yourself. .)

## Ch 1

- Read background concepts
- Installed git on work computer

## Ch 2.1 Git Basics

### Configure git (only need to once per computer)

$ git config --list --show-origin
$ git config --global user.name "E.T.Smith"
$ git config --global user.email teq.etsmith@protonmail.com
$ git config --global init.defaultBranch main
$ git config global core.editor “C:/Users/edens1/AppData/Local/Programs/Microsoft VS Code/Code.exe”
$ git config --list
$ git help config file:///C:/Users/edens1/AppData/Local/Programs/Git/mingw64/share/doc/git-doc/git-config.html

### Local Repository set up

$ cd C:/Users/edens1/Git_ETSmith/
$ git init # reinitialised existing git repository in C:/Users/edens1/Git_ETSmith/.git/
$ cd C:/Users/edens1/Git_ETSmith/Git_RAT
$ git init # reinitialised existing git repository in C:/Users/edens1/Git_ETSmith/Git_RAT/.git/
$ git add .
$ git commit -m 'Initial project version'

### Remote Repository Clone

$ git clone [url of repository](https://github.com/tariq-eden/RAT)
$ git add C:/Users/edens1/RAT
$ git status
$ git commit -m ‘Initial project version update’

## Ch 2.2 Recording Changes to the Repository

List of commands used
 Full deatails: [Tutorial Section](https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository)

### The 'add' command

$ git add [filename] # e.g. C:/Users/edens1/Git_ETSmith/git_tutorial_notes.md
The git add is a multipurpose command — you use it to begin tracking new files, to stage files, and to do other things like marking merge-conflicted files as resolved. It may be helpful to think of it more as “add precisely this content to the next commit” rather than “add this file to the project”).

#### Tracking new files

$ git add [filename] # e.g. C:/Users/edens1/Git_ETSmith/git_tutorial_notes.md
$ git status
$ git commit -m ‘commit message’ # e.g., git commit - m 'track git_tutorial_notes file'

#### Staging Modified Files

When a file appears under a section named “Changes not staged for commit” it means it is tracked, and was modified in the working directory, but is not staged. To stage it, you also run the git add command.
$ git add [filename] # e.g. C:/Users/edens1/Git_ETSmith/git_tutorial_notes.md
$ git status
$ git commit -m 'commit message' # e.g., git commit -m 'changes to git_tutorial_notes'

### Viewing Your Staged and Unstaged Changes

Outlines commands for more detailed status, return to this section later.

### Committing Your Changes

$ git commit -m 'commit note' # e.g., git commit -m 'update index document'
"let’s say that the last time you ran git status, you saw that everything was staged, so you’re ready to commit your changes. The simplest way to commit is to type $ git commit - doing so will launch the editor of your choice which will display text asking you to enter the commit message (note, lines starting with # will be ignored, and an empty message aborts the commit). To see changes to be made, you can pass the -v option to git commit to put the diff of your changes into the editor. When you exit the editor, Git creates your commit with that commit message (with the comments and diff stripped out). Alternatively, you can type your commit message inline with the commit command by specifying it after a -m flag (i.e., $ git commit -m 'commit message'). Note that anything you didn’t stage is still sitting there modified; you can do another commit to add it to your history. Every time you perform a commit, you’re recording a snapshot of your project that you can revert to or compare to later.

#### Skipping the Staging Area

The -a flag (which means 'include all changed files') can be added to a git commit command to make Git automatically stage every file that is already tracked before doing the commit, letting you skip the git add part used to explicitly stage selected files prior to a commit. To do this, be sure you want to commit ALL changes and check the status of changes ($ git status) to be sure, then use the command: $ git commit -a -m 'commit message'
$ git commit -a -m 'commit message' # e.g., git commit -a -m 'changes all recent changes'

### Removing Files

$ git rm [filename] # command to stage files for removal from the repository
$ git rm --cached [filename] # command to remove files from the staging while keeping it in the working tree (i.e., so the file reamins on your hard drive but Git doesn't try to track it)
To remove a file from Git, you have to remove it from your tracked files (more accurately, remove it from your staging area) and then commit. The git rm command does that, and also removes the file from your working directory so you don’t see it as an untracked file the next time around. Then, if you run git rm, it stages the file’s removal. The next time you commit, the file will be gone and no longer tracked. If you modified the file or had already added it to the staging area, you must force the removal with the -f option. This is a safety feature to prevent accidental removal of data that hasn’t yet been recorded in a snapshot and that can’t be recovered from Git.
If you just want remove a file from your staging area but keep the file in your working tree (so that the file reamins on your hard drive but Git doesn't try to track it) then use $ git rm --cached [file name], e.g., $ git rm --cashed local-noted_untracked.md

### Moving Files

$ git mv [old-filename] [new-filename] # command to rename a file, e.g., $ git mv Draft1.md Draft2.md
Note that this is a convenience command and is the same as running the following three commands:
$ mv Draft1.md Draft2.md
$ git rm Draft1.md
$ git add Draft2.md

### Ignoring Files

FOLLOW UP: *using VisualStudio* I created a .gitignore file and added the example ignore commands - not sure if this works, but the instructions for git aren't clear ($ cat .gitignore # This results cat: .gitignore: No such file or directory). *Follow-up later*

## Ch2.3 Viewing the Commit History

$ git log # command to view the commit history (lists the commits made in that repository in reverse chronological order) - note that there are a bunch of variations on this command (see [tutorial](https://git-scm.com/book/en/v2/Git-Basics-Viewing-the-Commit-History).

## Ch 2.4 Undoing Things

$ git commit --amend
Only amend commits that are still local and have not been pushed somewhere. Amending previously pushed commits and force pushing the branch will cause problems for your collaborators. Also, it’s important to understand that when you’re amending your last commit, you’re not so much fixing it as replacing it entirely with a new, improved commit that pushes the old commit out of the way and puts the new commit in its place. Effectively, it’s as if the previous commit never happened, and it won’t show up in your repository history.
See chapter for commands for: unstaging a staged file; unmodifing a modifed file; using git restore (It’s important to understand that git restore [file] is a dangerous command. Any local changes you made to that file are gone — Git just replaced that file with the most recently-committed version. Don’t ever use this command unless you absolutely know that you don’t want those unsaved local changes).

## Ch 2.5 Working with Remotes

$ git remote add shortname url # This add the remote repository and links it to a short name that can be mentioned in leu of the url.
For example, $ git remote add github-rat [url of repository](https://github.com/tariq-eden/RAT)

$ git remote # this command will list the shortnames of each remote handle you’ve specified.
$ git fetch shortname # This command will fetch all the information from the repository linked to that shortname.
For example, $ git fetch github-rat should fetch anything not already locally stored from the github repository for RAT.
$ git merge branch-name # merges into the current branch.
$ git push remotename branchname # This will push to the remote repository (on the branch named) - note, fetch an update prior to pushing.
Note that if there the remote branch isn't able to be committed, check that may be un-committed changes within it. Changes to a submodule will need to be staged and committed in the integrated terminal (accessed by right-clicking on the submodule in the explorer)
$ git status
$ git add (file names)
$ git commit -m (message)
THEN, the commits can be made in the main folder (i.e., GIT_ETSMITH using the shortcuts or command line)
