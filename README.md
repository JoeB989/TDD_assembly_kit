# TDD_assembly_kit
Assembly kit content for [The Dawnless Days (TDD)](https://discord.com/channels/328911806372511744/811928236752896020), a mod for Total War Attila.

### Contents
- [Setting up the environment](#Setting_up_the_environment)
- [Folder structure](#Folder_structure)
- [Workflow](#Workflow)

## Setting up the environment
Get the assembly_kit DLC (discord instructions link)
- you won't need to get the "old binaries" - they're all in this github repo
- you won't need to get the raw_data zip - the portions needed for battle tilemaps are in this github repo, and we may add more over time
- you won't need to get all the rules.bob files - they're in this github repo in the proper places

Github & github account
- You can browse the online repository in a browser: https://github.com/JoeB989/TDD_assembly_kit
- To contribute files, you'll need to create a [github](github.com) account if you don't have one
- The first time you connect to github from VS Code it will launch you into a browser window and ask for your github account and password.  This should only be needed once

Git
- Install [git](https://git-scm.com/downloads) - or update if you have git but it's old
- Because some of our large files are larger than github's limit (100mb), we use Git Large File Storage (LFS).
-  Install [git LFS](https://docs.github.com/en/repositories/working-with-files/managing-large-files/installing-git-large-file-storage)
- [configure git LFS](https://docs.github.com/en/repositories/working-with-files/managing-large-files/configuring-git-large-file-storage), using Git Bash (from start menu), for these file types
  - .tif
  - .dds
  - .tiles
  - .dll

VS Code & cloning a local copy of the github repository
- Install [VS code](https://code.visualstudio.com/download).  Or you can substitute your favorite git-compatible editor or client if you want
- In VS Code, Open Folder and select the `Total War Attila` install folder
- On the Source Control tab, click Clone Repository
- Paste in `https://github.com/JoeB989/TDD_assembly_kit.git` and hit Enter
- Or, if you don't have the Clone option
  - Open Visual Studio Code terminal (Ctrl + `)
  - Paste and execute this Git clone command

    ``` git clone https://github.com/JoeB989/TDD_assembly_kit.git ```
  - Open the folder (File - Open Folder) you have just cloned, TDD_assembly_kit
- This will create and populate a `TDD_assembly_kit` folder in Total War Attila, right next to `assembly-kit`.  Be patient: there are many files, some very large.

WinMerge
- We use WinMerge to update files between the TDD and attila assembly kits
  - `assembly_kit` is the TW Attila DLC
  - `TDD_assembly_kit` is replicated to github and shared with others, and is a partial mirror of `assembly_kit`
- Install [WinMerge](https://winmerge.org/)
- There is a starting `tdd.WinMerge` project that compares TDD_assembly_kit and assembly_kit
  - **Important** it has relative pathing in it; if you modify it (resulting in full paths) and plan to publish it to others, you should re-edit the file to make the paths relative again.  The paths should look like `..\assembly_kit` and `..\TDD_assembly_kit` because the current-directory is TDD_assembly_kit
  - You can also create your own `.WinMerge` projects for your own use, but don't push them to the shared repository.  You can save them somewhere else to avoid confusion.

Explore WinMerge
- open `tdd.WinMerge` and explore the UI
- what you see
- what's in and what's out

Assembly_Kit (AK) tools
- You should only run AK tools from assembly_kit, not from TDD_assembly_kit
- In AK tools you should load/save data only from assembly_kit folders, not from TDD_assembly_kit
- there are two AK binaries folders
  - binaries_terry - for running Terry (via TWeak).  This is the 'old' binaries
  - binaries (or binaries_bob or binaries_non_terry if you renamed yours) - for running BOB and Ted etc.

Other tools
- rpfm

Resources
- [The Dawnless Days (TDD) discord](https://discord.com/channels/328911806372511744/811928236752896020)
- [Working with GitHub in VS Code](https://code.visualstudio.com/docs/sourcecontrol/github)
- [Managing large files with Git Large File Storage](https://docs.github.com/en/repositories/working-with-files/managing-large-files)

Troubleshooting
- https://stackoverflow.com/questions/59282476/error-rpc-failed-curl-92-http-2-stream-0-was-not-closed-cleanly-protocol-erro `git config --global http.postBuffer 524288000`


## Folder structure
assembly_kit structure, how each piece is used

a picture that shows where files live in the Code/git/WinMerge universe
- tdd_assmebly_kit vs assembly_kit
- local changes
- staged changes
- commited changes on your pc
- github repository

## Workflow
file management between tdd_assembly_kit and assembly_kit
WinMerge
- how to update files
- how to add more content to TDD_assmebly_kit

The editing lifecycle
- edit, stage, commit, publish, sync

tool workflows
- terry, bob, rpfm, ...