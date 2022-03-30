# Making a pull request



- Let's start by creating a new branch  
![](img/pr-new-branch.png)<!-- -->
- We do some work (in VSCode/text editor/RStudio) which creates a markdown file with a title and some text. We then make a new commit which adds this new file to the repo  
![](img/pr-commit-new-file.png)<!-- -->
- Next publish the new branch to GitHub  
![](img/pr-publish-branch.png)<!-- -->
- Now initiate the creation of the PR by either clicking in GitHub Desktop "Create Pull Request" 
![](img/pr-create-pr-01.png)<!-- -->
- or clicking on the button on the repo webpage "Compare & pull request"  
![](img/pr-create-pr-02.png)<!-- -->
- Edit the title box, add some extra text in the comment box, select a reviewer, and then click "Create pull request"  
![](img/pr-create-pr-and-reviewers.png)<!-- -->
- You can amend/edit pull requests by modifying/adding commits to the branch from which you sent the PR
- See more about pull request reviews [here](https://docs.github.com/en/github/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/about-pull-request-reviews)
- (The reviewer) will then merge your PR  
![](img/pr-merge-pr.png)<!-- -->
- (The reviewer) will then confirm the merge  
![](img/pr-confirm-merge.png)<!-- -->
- (Optional) Delete the branch the PR came from  
![](img/pr-delete-branch.png)<!-- -->
- The PR is now finished and we can see the merge commit in the default (`main`/`master`) branch
![](img/pr-finished.png)<!-- -->
- In GitHub Desktop click "Fetch origin"/"Pull origin" to pull the updated `main`/`master` branch down to your local machine ... and the process begins again ...
