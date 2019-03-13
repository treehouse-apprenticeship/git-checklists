# Handling GitHub Issues
You'll be assigned issues -- bug fixes, feature requests -- in GitHub. Read the issue in GitHub to figure out what needs to be done. Make a note of the issue number because you'll use that number when creating a branch.

## Get the Code and Fix the Issue Locally
1. **Pull down the latest code**
   
   > ```git pull origin master```

2. **Create and checkout branch to work on issue.** For example if the issue number is 52:

    > ```git checkout -b issue-52```

3. **Make changes required by the issue and commit.** Make sure to commit early and often -- it's good to commit when you've fixed one thing for example. Then, if there's another thing to fix, do that then make a second commit. However, don't commit incomplete work -- for example, if you haven't completely fixed a bug you are working on complete that fix before committing. 

    > ```git add .``` -- stages all changes

    > ```git commit -m "Your commit message"``` -- commit your staged changes using the `-m` option to provide a short commit message (preferred)
   
    > ```git commit``` -- commit your staged changes using the editor so you can provide longer commit messages (if needed)

4. **Update your branch with the latest changes from the remote `master` branch.** Before you push your branch up to GitHub (in the next step), make sure that you have all of the latest updates from the remote `master` branch. When you're working on a team, it's likely that someone else has made changes to the `master` branch while you were working on a fix for your issue.

    > ```git pull origin master```

5. **If there are any merge conflicts, resolve them before moving on to the next step.**

6. **Push your branch up to GitHub.** For example, if the issue # is 52, and the branch is `issue-52`.

    >```git push origin issue-52```

## Create Pull Request on GitHub
1. **Go to the project repo on GitHub**, and click the "Pull requests" tab.
2. **Click the "New pull request" button.**
3. **From the "Compare" drop-down, select the branch you pushed to fix the issue.**
![PR select branch](images/pr1.png "Select Branch")
4. **Click the "Create pull request" button.**
5. **Write a description for the pull request.** Here you can describe the changes you made to fix the issue.
6. **Assign the PR to one of your teammates for code review.**
![PR assignment](images/pr2.png "PR Assignment")
7. **Click the "Create pull request" button.**

If your PR fixes the issue, then the code reviewer will accept the PR and merge your branch into the `master` branch. If not...

## Resolve Any Issues
If the code reviewer found a problem in your code, they'll comment on the PR and you'll need to resolve any problems they found.
![PR rejected](images/pr3.png "PR Rejected")

1. **Make sure you are still on the issue branch you created.**
    >```git checkout issue-52```

2. **Make required changes.**
3. **Stage, commit and push** (as described above)
4. **On GitHub go to the Pull Request you created earlier -- add a note and tag the code reviewer to let them know that you've updated the branch.** They'll review your code again -- repeat these steps until the PR is accepted.

## Close the Pull Request
Once your code is approved by the reviewer it's time to close the PR.

1. **On GitHub go to the Pull Request and click the "Merge pull request" button.**
2. **Click the "Confirm merge" button.** GitHub will merge the branch associated with the PR into the `master` branch and close the PR.
3. **Click the "Delete branch" button to delete the branch that was associated with the PR.** Once your fix has been merged into the `master` branch, it's safe (and a good practice) to delete the branch that you created for the fix.

At this point, you're done, and you can also delete your local branch -- but don't do this until you know the PR's been accepted.

> ```git branch -d issue-52```
