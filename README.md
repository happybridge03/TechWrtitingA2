# Using and Navigating a Git Repository

Technical Writing 

Assignment 2 - Instructions

Sean Bridge

## Introduction

This repository is a hands on instructional demonstration on how to use the `git` version control system and the `git-bash` terminal on a Windows device. 

After following these instructions, you will be able to understand the basic `git` commands as well as the typical workflow someone who uses `git` regularly would go through on a daily basis. 

### What is Git?
> "Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency." 
>
> *git-scm.com*

Git is the most used version control system in the world. A version control system is a piece of software which is used to track, manage, and combine changes in a set of files over time. Git is especially popular due to its high speeds and the ability to synch changes between one central remote repository and a lot of local ones.   

It is mainly used by computer programmers and software developers to track their code changes and collaborate with other developers. `Git` forms the backbone of the open-source community.

### Why use Git?

The main reason to use `git` is to track and make changes in a way that is completely reversible. With every commit which is made to a repository the state of the repository is saved and able to be revisited at a later date.

Multiple different versions of the same set of files can be worked on at the same time with branches. Each branch can be used to workshop or experiment with different features or changes which may have adverse affects on the rest of the code. If an experiment is successful and a developer would want to integrate it with the rest of their code, they can then merge those changes into the main or official code branch.  

> ![Diagram of a typical git repository with a master branch, develop branch, and topic branch.](./Photos/git%20branches%20diagram.png)
> 

When this is integrated with a service such as `GitHub` multiple developers can work on the same code in different branches at the same time. Allowing two developers to develope two different features at the same time, which can then be integrated together at a later date.

This allows for a workflow which is experimentative, iterative, and collaborative. 

### Further Readings
| Reading                                        | Description                                                          |
| ---------------------------------------------- | -------------------------------------------------------------------- |
| [Git About Website](https://git-scm.com/about) | A more thorough description of the features of `git` source control. |
| [GitHub About](https://github.com/about)       | A full description of what `GitHub` is.                              |

## Assumptions

These instructions make some assumptions about the user of this guide as well as the materials that the user has access to. 

### Audience Assumptions

This instructional guide assumes that a user understands the basics of using their computer. 

These skills include navigating the internet, installing programs, opening programs, and typing.   

### Material Assumptions

This guide assumes a user has access to a computer with either Windows 10 or 11 and the user has the necessary permissions to install programs on that computer.  

## Instructions

### Install `Git` & `Git-Bash`

By default `Git` is not included on most Windows computers and must be downloaded from `Git`'s official website. Additionally, the default Windows terminal is not great for using and navigating `Git`. Therefore, the makers of `Git` have created `Git Bash`, a terminal created specifically to interact with `Git` and other command-line tools on Windows devices. 

#### 1. Downloading the Installer   

Navigate to the windows installation page of the [git website](https://git-scm.com/download/win). You will know you are on the correct page if it says `Download for Windows` at the top of the page (Fig 1).

> ![The Git installation website for windows systems. The installation link is highlighted.](./Photos/Git%20Installer%20Website.png) 
> *Figure 1*: The Git installation website for windows systems. The installation link is highlighted.

Once you are on the page, click on the text in the first paragraph which reads `Click here to download`. The download for the installer should begin immediately.

#### 2. Run the Installer

Once the installer is downloaded navigate to where the executable downloaded to. By default this will be your `Downloads` folder, however, most browsers have a button on the top right of their window to see recently downloaded files.

Run the executable, allow the executable to make changes on your device, and follow the instructions on screen. 

The executable should be configured to install and configure the needed components correctly, however make sure that at a minimum the boxes next to `Git Bash Here` and `Associate .sh files to be run with Bash` are checked (Fig 2).

> ![The component selection window of the Git installer with the default installation options that are expected by this guide](./Photos/Git%20Bash%20Install%20Config.png)
> *Figure 2*: The component selection window of the Git installer with the default installation options that are expected by this guide. 

Continue to hit the next button on the bottom right of the installer window, leaving all settings as their default. Upon reaching the final window hit `Finish` in the bottom right corner.

#### 3. Open Git-Bash

Once the executable has finished installing, click on your windows search bar and search for the application titled `Git Bash`.

Opening this application should open a `Git Bash` terminal window. The terminal window displays the current user and device names and should have a flashing cursor in front of a `$` sign (Fig 3).

> ![A freshly opened Git Bash terminal. The terminal reads "bridg@XPSWinBri MINGW64 ~".](/Photos/Git%20Bash%20Terminal%20Window.png)
> *Figure 3*: A freshly opened `Git Bash` terminal window. This terminal shows that the current user is `bridg` and the device is named `XPSWinBri`. `MINGW64` refers to a library of windows coding utilities that `Git Bash` is built off of. The `$` is the current terminal line.

To ensure that the terminal is working correctly, click on the terminal and type the command: 

```sh
echo "Hello World"
``` 

Then hit enter. The terminal should then display the text `Hello World` below your typed command.

> **Note**:
> If this application is not visible in the windows search bar, fails to run, or throws an error when you attempt to run the test command, then return to the previous step and ensure that the application was installed with the default installation settings. 
> 
> A  fresh install can be completed with the same installer so long as the `Only show new options` box at the bottom of the install window is not checked (Fig 2).


#### 4. Verify Git is installed correctly

In order to verify that Git was installed correctly type the command:

```
git version
```

The hit enter. The terminal should then display the version of Git that was installed on your system (Fig 4). This version should match the version listed on the installation website (Fig 1).

> ![A Git Bash terminal where the command `echo "Hello World"` was ran and returned "Hello World", and the command "git version" was ran and returned "git version 2.40.0.windows.1".](./Photos/Verifying%20Git%20Installation.png)
> *Figure 3*: A git bash terminal where both the `Git Bash` installation test from the previous step, the the `Git` installation test from this step has been run. Notice how the version `2.40.0` matches the version from Figure 1.

### Preparing a folder

`Git` repositories are based out of a single parent folder. All of the files within that folder (and any sub-folders) are then tracked by `git`. So for neatness, we will be making a folder to contain all of the code that will be track by this `git` repository so if you wish to delete all of the files created by these instructions, you will only need to delete a single folder. 

#### 5. Create a Folder for the `Git` Repository

Open the Window's File Explorer and navigate to where you wish to create the folder which will hold your `git` repository. It is recommended that you create this folder on your `Desktop` or in your `Documents` folder.

#### 6. Open the Folder in `Git-Bash`

Once that folder is created, right click in that folder and then `Git Bash Here`. 

> **Note**: 
> If your computer is running Windows 11, you may need to click `Show more Options` before the `Git Bash Here` options will be displayed.

This will open a `Git Bash` terminal based in that folder and any commands which are run in that terminal will be based out of that folder (Fig 4).

> ![a Windows File Explorer window and a Git-Bash terminal. Both the Git-Bash terminal and the Windows File Explorer window are open to the same folder.](./Photos/Git%20Bash%20In%20Folder.png)
> *Figure 4*: This image is what the `Git-Bash` terminal should look like when opened in the folder correctly. Notice how the folder's path is displayed in the terminal, make sure this matches what you expect. 

### Cloning a Repository

Now that we have a folder set up and a terminal window open to that folder we can create a repository into this folder.

There are two main ways to create a repository on your local computer. You can either initialize a clean repository in a local folder using `git initialize` , or you can clone an already existing repository from a remote repository using `git clone`. 

> **Warning**: 
> It is important that `git` repositories are kept to a local folder and not the entire file system. If a `git initialize`  is run in a folder with many files or many sub-folders (such as at the root of a computer's `C Drive`) then this can cause `git` to slow to a crawl or even crash. 

We will be using the second method of cloning from a remote repository. 

#### 7. Copy the `Git` repo's `HTTP` address

Navigate to the top of this repository's [GitHub page](https://github.com/happybridge03/TechWrtitingA2) (which you should be reading this off of) and click on the <font color=lime>`<> Code`</font> button (Fig 5). 

Select the `Local` and `HTTP` tabs. Then copy the address from the text box there.

> ![The GitHub page for this repository with the HTTPS URL highlighted in yellow.](./Photos/Github%20HTTP%20Address.png)
> *Figure 5*: The GitHub page for this repository with the HTTPS URL highlighted in yellow.

#### 8. Use the address to clone the repository

To clone the repository from GitHub, type the following command into the terminal you opened in step #6 and replace `<address>` with the `HTTP` address from the previous step:

```
git clone <address>
```

> **Note**: `Git-Bash` does not support the default copy & past keyboard shortcuts. If you want to copy and paste the `HTTP` address directly from GitHub into the `Git-Bash` terminal you will need to right click in the terminal and select the `Paste` option or use the `Shift + Ins` shortcut.

After you run this command there should be a new folder called `TechWritingA2` in your original folder. The contents of this repository has now been downloaded into this folder.

> ![A terminal displaying the expected execution of the `git clone` command.](./Photos/Git%20Repository%20Cloned.png)
> **Figure 6**: A terminal displaying the expected execution of the `git clone` command.   


#### 9. Inspect information about the repository

Now that we have a cloned repository let's inspect its contents. Move the terminal into the `TechWritingA2`. Do this either by opening an entirely new terminal like in step #6, or, in the terminal which is already open, type and run the command:

```sh
cd TechWritingA2
```

Now run the command:
```
git log
```

The `log` command displays a list of commit, in chronological order, along their author, when they were made, and the message that was given for each commit. This is the quickest way to see the change history of the repository.

Next, run the command:
```
git branch
```

The `branch` command displays a list of branches in the repository (Fig 7). The branch which you are currently located on will have an astrict next to it. 

> ![The expected execution of the `git branch` command.](./Photos/Git%20Branch%20Command.png)
> Figure 7: The expected execution of the `git branch` command. Notice how the `main` branch is both highlighted in green and has an astrict next to it.

To see a visual representation of how the different branches relate to one another run the command:
```
git log --graph --all --oneline
``` 
This will show the same information as the `log` command, except it will graphically display that information, with lines showing the relationship between each commit and the different branches those commits rest on. 

> **Note**: Take note of where the `HEAD` label is. This label is what commit you are currently located at. 

### Branch Management

Now that we have a functioning repository, and understand what branches and commits the repository has, lets navigate through those commits and branches. 

#### 10. Checkout a new branch

In order to switch to another branch run the command:
```
git checkout <branch name>
```

Now if you run 
```
git branch
```
you will see that the astrict has moved to a different branch name, signifying that you have switched branches. 

You can also see this with the graphical visualization by running the command:
```
git log --graph --all --online
```
Notice how the `HEAD` label has moved to a different location than it was in step #9.

#### 11. Create a new branch

To create and switch to a new branch you can run the command:
```
git checkout -b <New Branch Name>
```

You can verify this worked by running the command:
```
git branch
```

### Commits

To actually populate your new branch with commits, you need to be able to make a new commit. Commits are an essential part of tracking changes within the repository. 

#### 12. Set up personal details

With very commit, `git` tracks who made it. This means that before you can make a commit you need to tell `git` who you are. To do this, run the commands:
```
git config --global user.name <NAME>
git config --global user.email <EMAIL>
``` 
Where `<NAME>` is your name and `<EMAIL>` is your email. No neither need to be your real name or email. 

#### 13. Modify a file

The first step in making a commit, is to actually modify a file within the repository. If you were to run the command `git commit` without making any file changes, you will receive an error which reads: `no changes added to commit`.

So let's modify a file. 

Open the repository folder in Windows File Explorer. There should now be a file called `Modify_Me.txt`. Open this file in a text editor of your choice (double clicking on the file will open it in your default text editor) and add a line of text to it. Make sure to save the file before closing it again.

#### 14. Stage your changes

In order to create a commit you must first "stage" the changes you just made. This is basically just selecting what changes you want to be apart of the commit that you make. This allows you to modify multiple files at once, and then separate the different changes across multiple commits.

To stage the change you just made, run the command:
```
git add Modify_Me.txt
```

You can check if this was successful by running the command:
```
git status
```

#### 15. Make the commit

To make the commit, run the command:
```
git commit
```
This will prompt you to type a message to describe the commit you just made. This description will be displayed when the command `git log` is run.

You can also run the command:
```
git commit -m <Description>
``` 
And whatever text you replace `<Description>` with will be automatically assigned to the description and the prompt will be skipped.

Make sure to verify that your commit was successful by running:
```
git log
``` 

#### 16. Do it again

Repeat steps 13-15 to add another commit to your branch. 

#### 17. Revert your previous commit

Now lets pretend that you didn't mean to make that most recent change. In order to fix that change you would run the command:
```
git revert HEAD~1
```

This command means revert the current branch backwards one commit -- signified by `~1` -- from the current `HEAD`.

Running this command will prompt you to enter a description for **why** you are reverting the commit. This is an essential feature of `git`, every single change, even undoing previous changes, is tracked by the repository.

See how this is tracked by running the command:
```
git log
```

#### 18. Merge changes into the `main` branch

The final basic feature of `git` is merging changes from one branch into another. In order to merge your new branch back into the `main` branch run the command:
```
git merge main <New Branch>
```

This will take the commits from your new branch and add them to the `main` branch creating a single branch which has all of the changes from both. 

You can verify that this worked by running the command: 
```
git log --graph --all --oneline
```

## Glossary

| Term           | Definition                                                                                                                                                                                                                                                                 |
| -------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Git            | Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.                                                                                                                |
| Git-Bash       | A BASH emulation used to run Git from the command line. *NIX users should feel right at home, as the BASH emulation behaves just like the "git" command in LINUX and UNIX environments.                                                                                    |
| Repository     | Tracks all changes made to files in your project, building a history over time.                                                                                                                                                                                            |
| HTTP           | The Hypertext Transfer Protocol is an application layer protocol in the Internet protocol suite model for distributed, collaborative, hypermedia information systems.                                                                                                      |
| Github         | An Internet hosting service for software development and version control using Git. It provides the distributed version control of Git plus access control, bug tracking, software feature requests, task management, continuous integration, and wikis for every project. |
| Source Control | A class of programs responsible for managing changes to computer programs, documents, large web sites, or other collections of information                                                                                                                                 |
| Branch         | Represents an independent line of development. Branches serve as an abstraction for the edit/stage/commit process. You can think of them as a way to request a brand new working directory, staging area, and project history.                                             |
| Commit         | A snapshot of your repo at a specific point in time                                                                                                                                                                                                                        |
| Terminal       | A text-based interface to the computer                                                                                                                                                                                                                                     |
