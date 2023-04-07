# Using and Navigating a Git Repository

## Introduction

### What is Git?

### Why use Git?

## Assumptions

### Audience Assumptions

### Material Assumptions

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

> :memo: **Note**:
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

> :memo: **Note**: 
> If your computer is running Windows 11, you may need to click `Show more Options` before the `Git Bash Here` options will be displayed.

This will open a `Git Bash` terminal based in that folder and any commands which are run in that terminal will be based out of that folder (Fig 4).

> ![a Windows File Explorer window and a Git-Bash terminal. Both the Git-Bash terminal and the Windows File Explorer window are open to the same folder.](./Photos/Git%20Bash%20In%20Folder.png)
> *Figure 4*: This image is what the `Git-Bash` terminal should look like when opened in the folder correctly. Notice how the folder's path is displayed in the terminal, make sure this matches what you expect. 

### Cloning a Repository

Now that we have a folder set up and a terminal window open to that folder we can clone a repository into this folder.

#### 7. Copy the `Git` repo's `HTTP` address

#### 8. Use the address to clone the repository

> :warning: **Warning**: 
> It is important that `git` repositories are kept to a local folder and not the entire file system. If a `git` repository is initialized in a folder with many files or many sub-folders (such as at the root of a computer's `C Drive`) then this can cause `git` to slow to a crawl or even crash.  


#### 9. Inspect information about the repository

### Branch Management

#### 10. Visualize the branch relationships

#### 11. Checkout a new branch

#### 12. Create a new branch

### Commits

#### 13. Modify a file

#### 14. Create a new commit

#### 15. Do it again

#### 16. Revert your previous commit

#### 17. Merge changes into the `main` branch

#### 18. Resolve merge conflicts

### Remote Repositories

#### 19. Create a GitHub Account

#### 20. Create a new empty remote repository

#### 21. Register this remote in the local repository

#### 22. Push the local repository to the remote repository

## Glossary

| Term           | Definition |
| -------------- | ---------- |
| Git            |            |
| Git-Bash       |            |
| Repository     |            |
| HTTP           |            |
| Github         |            |
| Source Control |            |
| Branch         |            |
| Commit         |            |
| SSH            |            |
| Terminal       |            |
