# Intro to Git



## Background info

- Git was written to allow developers work on the source code of the Linux kernel (text files)
  - One kernel release they got in a terrible mess
  - This provoked Linus Torvalds into action
  - For an excellent insight into his thinking watch this talk he gave at Google [here](https://youtu.be/4XpnKHJAok8)  
  - (Especially if used at the command line) Git can be intimidating to use and we can get Git errors (which like LaTeX and R errors can be quite cryptic)  
    <img src="https://imgs.xkcd.com/comics/git.png" width="50%" />
- A Git repository is a folder/directory on your computer which has been Git initialised 
  - Using either the command line  
    ```
    git init mynewfolder
    ```  
  - Or GitHub Desktop  
    <img src="img/ghd-new-repo.png" width="50%" />
  - Repos on GitHub are already Git initialised 
    - When you clone them down to your computer they work in GitHub Desktop
- Git is commonly referred to as version control software
- Git is better described as a *content addressable filesystem* which translates to *Git tracks the contents of the files in your repo*
  - Git creates a little database of the contents of your files - snapshots (commits) are taken when you tell it to
  - Git looks for changes in your files when you save them, so when you have unsaved changes in a file/s Git shows no changes until you save  
    <img src="img/no-local-changes.png" width="1123" />
  - Git takes snapshots of your files - when you tell it to - *commits* - I saved my file from above, enter a commit message and click "Commit to master"
    <img src="img/stashed-changes.png" width="1482" />
  - Commits are identified by the 40-character checksum SHA-1 hash of the contents of your files at that time  
    <img src="img/git-commit-hash-1.png" width="714" />
    
    <img src="img/git-commit-hash-2.png" width="1355" />
    
    <img src="img/git-commit-hash-3.png" width="1401" />
  - Git knows the state of your files at every commit
    - You can easily restore your files to a previous state
  - For Git the state of your files only changes when their contents change
    - If you reopen a file, make no changes, then close it, Git will show no changes in your repo
    - If you add an empty folder/directory to your repo Git will show no changes in your repo
    - This differs to OneDrive/SharePoint/Google Drive which are file synchronisation systems
  - I recommend not to place your Git repos in a location that is sync'd by either OneDrive or Google Drive

## The `.git` folder

- When you initialise a directory the `.git` folder is created
- This contains all of the files Git uses to track the contents of your files
- Here is the `.git` folder of a repo on my computer (I have selected to View hidden files in Windows Explorer)  
<img src="img/windows-explorer-repo.png" width="50%" />
- Confusingly GitHub hides the `.git` folder from view  
<img src="img/repo-github-view.png" width="730" />
- Here are its contents - don't edit these manually  
<img src="img/dot-git-folder-contents.png" width="50%" />
- Explanation of these is (from [here](https://www.tutorialspoint.com/what-is-git-folder-and-why-is-it-hidden))  
<img src="img/dot-git-folder-explanation.png" width="734" />

## Common Git commands

- I recommend you use GitHub Desktop instead of these commands
- These commands are what GitHub Desktop is using behind the scenes
- Git is the name of the program, `git` is the name of the executable available at your command line  

    ```
    git init 
    git add <filename>
    git status
    git commit -m "Your commit message"
    git commit --amend -m "Your amended commit message"
    git push 
    git pull 
    git clone
    git branch
    git checkout
    git merge
    git fetch 
    ```  