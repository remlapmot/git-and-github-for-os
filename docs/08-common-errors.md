# Common errors



## Merge conflicts

* These can happen if e.g., 
  - you forget to pull down the latest changes from GitHub (I find easy to forget in the morning)
  - if you're working on a project with multiple people
    - you both create new branches
    - they send in their PR first and it's merged
    - then you send in your PR which edits some of the same lines
* Let's say I made changes yesterday which I pushed to GitHub
  - The next day I restart work on a different computer, GitHub Desktop will show for example  
    <img src="img/pulling-from-github.png" width="740" />
- But you forget to click "Pull origin"
- If you make commits onto a branch on which there are not yet pulled commits on GitHub you'll get a merge error when you eventually click "Pull origin"  
<img src="img/ghd-resolve-conflicts-before-merge.png" width="510" />
- You could resolve conflict e.g., in VSCode  
<img src="img/vscode-git-merge-resolve.png" width="1120" />
- We can see this can happen when we see both up and down arrows in Pull origin box (but not always)  
<img src="img/ghd-potential-conflict.png" width="1200" />
* Fix
  - Move your changes to a new branch  
    <img src="img/ghd-create-branch-from-commit.png" width="1084" />
  - Move back to `master`/`main` and revert/undo the changes there, then edit the files so they show no changes  
    <img src="img/ghd-revert-changes-in-commit.png" width="1088" />
    
    <img src="img/ghd-undo-commit.png" width="1086" />
  - Pull down the changes from GitHub to the relevant branch  
    <img src="img/ghd-all-is-well.png" width="1083" />
  - Merge changes from your new branch into the `main`/`master`/relevant branch
- See the GitHub documentation for more information about merge conflicts
  - [here](https://docs.github.com/en/github/collaborating-with-pull-requests/addressing-merge-conflicts/about-merge-conflicts)
  - Resolving a merge conflict [here](https://docs.github.com/en/github/collaborating-with-pull-requests/addressing-merge-conflicts/resolving-a-merge-conflict-on-github)

## No content changes found

- If you see the following message from Git that a file has changed but there are *No content changes found*  
    <img src="img/no-content-changes-found.png" width="720" />

- This is most likely caused by working with colleagues using different operating systems, because they save text files with different line ending characters (`CRLF` on Windows, `LF` on macOS/Linux/Unix)

- You can usually simply right click on the offending file in GitHub Desktop and *Discard changes*  
    <img src="img/no-content-changes-found-discard-changes.png" width="722" />
- Additionally you can set the following option at the top of your `.gitattributes` file

    ```  
    # Auto detect text files and perform LF normalization
    * text=auto
    ```  
