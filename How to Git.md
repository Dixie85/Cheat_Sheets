# In the world of GIT

### Concepts
- Version control
- Git
- Github


## Version control

> Version control is a tool that lets us keep track of different versions of a file.

 - the files would not only have a name but also a version number, throu witch the version control system will keep track, for us.
 - it keeps track of versions of all files so that we can know which version of one file works together with which version of other files.
 - allows us to browse through the version history, see who did what change.


## Git

> "Git" is a super fast, distributed version control system.

 - why _super fast_ - since everyone has a copy of the entire history, all actions happen on your computer (aka locally), making most actions very fast.
 - git can be used to track huge code bases with no problems.


### Terminology

**"Repository"** - A location where code is stored, either on your computer or somewhere else. Also called a ‘repo’.

**"Local Repository"** - A git repository on your machine (stored in a folder called .git).

**"Remote Repository"** - A git repository somewhere else, typically online. Maybe GitHub or similar.

**"Clone"** - A copy of a repository and all its history so that you can work on it on your local machine.

**"Working Directory"** - The folder where your current .git folder is located for this repository.

**"Staging Area"** - Where files being prepared to commit.

**"Committed Files"** - Files stored in git (locally .git).

**"Pull"** - Get current git state from another repository.

**"Push"** - 	Move current git state to another repository.

**"Branch"** - A parallel copy of the original repository at a certain point in time. Gives the opportunity to track the same files at different points in the time.

**"Add"** - Adding changes to the Staging Area.

**"Commit"** - Storesing a version of a file in history.


### The staging process

Git saves things into the repository in two steps.

When we want "git" to know about something/some changes on our computer we will need to **add** it to what is known as the **staging area**. This is how we tell git about the created/changed file/s. Before we **_git add_** a file, git will not know/care about the file.

 - **Steps 1** 
    - An _unstaged_ file is a file that we have on our computer (in the folder with the repository) that we haven't told git about. Git won't track the file unless we explicitly tell it to. (Unstaged changes are changes that are not tracked by the Git).
    - A _staged_ file is a file that we have **_git add_** to our local git repository. We can remove a staged file from the staging area, and then the file becomes unstaged again.
 - **Steps 2**
    - Once we have staged a file, now we can save a certain version of the file to the repository. This is called to **_commit_** a file to git. Once you have _git commit_ a file, git stores a version of that file in our history(in the repo).


### Few git commands to start with

**git help** - Prints out useful commands and theirs descriptions.

**git init** - To create a repository.

   > git init {location}


**git clone** - Clone a remote repository. Make a local copy of a repository on another computer. _git clone_ needs a URL and takes an optional location.

   > git clone {url} {location}


**git status** - Which shows the current status of the files in our local repository; what is staged, what is committed, how is our repository doing compared to a remote repository, etc.

   > git status


**git add** - Is used to add files to the staging area. You know what that means.

   > git add


**git rm** - Is used to remove files from the staging area.

   > git rm


**git commit** - _Git commit_ commits/saves staged files into the git repository. It needs a message which is set with the _-m_ flag, making the full command...

   > git commit -m "Final update"



**git log** - Shows the log in the console.

   > git log


**git pull** - If we want to get the changes from someone else repository, we do _git pull_. This will bring down(pull) all the changes that we don't have and merge them into our repository.

   > git pull 


**git push** - If you want to send our changes to another repository - we do _git push_.

   > git push


### A few words on branches

A branch is a way to make a parallel copy of the current state of the files in your repository. That branch can then evolve separately from the original. This is very useful if you want to work undisturbed for a while.
Once your work is done you can **_merge_** the state of your branch into another branch. Because merge means that you will put two versions of the file(s) that have evolved independently of each other together in one. This might result in problems - that are called merge conflicts.
All repositories have at least one branch main (used to be called master). There's nothing special about that name, other than it is by convention the first branch.

 - **git branch** - create a new branch if a name is added, like this...

   > git branch {branch-name},

   ...and shows all existing branches if used without any name, like this... 

   > git branch

   and then can we switch over to that branch new created branch i.e. view the repository as it looks in the branch) using... 

 - **git checkout** 
 
    > git checkout {branch-name}.

    ...and all together...

    > › git branch testing-dangerous-stuff-by-myself
      › git checkout testing-dangerous-stuff-by-myself
      Switched to branch 'testing-dangerous-stuff-by-myself'

    ...or do both at the same with... 

    > git checkout -b testing-dangerous-stuff-by-myself

    ...to delite a branch, we use the flag _-D_, something like...

    > git branch -D {branch name}

 - **git merge**
  Finally, merge the state of one branch into another by _git merge {branch name_ to merge into your current branch}. If we are on the _main_ branch and want to merge the changes made in _testing-dangerous-stuff-by-myself branch_ into main...

    > - git checkout main 
    > - git merge testing-dangerous-stuff-by-myself


## GitHub

GitHub is the world's largest site for sharing code among developers. At GitHub.com developers can upload their git repositories and then let other people clone them to work on the code on their computers.

GitHub and git are, in other words, two very different things. git is a tool to create repositories on your computer, GitHub is a website that facilitates collaborating on code (and other things where keeping track of versions is important - law-texts has been managed on GitHub).

GitHub has a few key concepts that their site revolves around and that are useful to facilitate working together on code. But at its core, GitHub is built around git.

### GitHub concepts

**Repo** - A git repository pushed to GitHub. This is the starting point for everything you do with code on GitHub. A repository can be public so that everyone can see (and use) it. Or private when only people you let in can use it.

**User** - Each user has an account, and each user have a public homepage (https://github.com/Dixie85 for example). This is a place where you can show off your skills and your work.

**Organization** - Organizations can also be created in GitHub and is a way for companies to share their code amongst themselves and others. Organizations also have a homepage.

**Fork** - Make a clone of a repository from one user to another. It's a real git clone which means that we can then do git push to send changes to the original from our forked repository. Or git pull to get changes into our repository from the original.

**Pull Request (Pr)** - If you git push to a repository that you don't own, it will not be automatically merged into the repository. Instead, you can create a pull request.


## Additional reading and video materials

[Git and GitHub for Beginners] (https://product.hubspot.com/blog/git-and-github-tutorial-for-beginners)

[Git Staging Area - simple explanation] (https://dev.to/sublimegeek/git-staging-area-explained-like-im-five-1anh)

[Introduction to branches] (https://www.atlassian.com/git/tutorials/using-branches)

[How to Fork a GitHub Repository] (https://www.youtube.com/watch?v=XTolZqmZq6s)