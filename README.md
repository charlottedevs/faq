# faq
frequently asked question
## How to fork a repo

1. Create a GitHub account
2. Navigate to the repository you'd like to fork.
3. In the top right corner of the page click Fork.

This will give you a fork of the orginial code to edit.


GitHub's documentation on how to fork a repo: https://help.github.com/articles/fork-a-repo/

## How to submit a pull request from your forked repo?

1. After you've forked the repo you want to contribute to, clone the repo locally.


2. Make your changes.


3. When you're done, commit and push the changes you've made to the your forked repo.
_(Note: When you commit, don't forget to include details about the changes you've made in the commit message.)_


4. Visit your forked repo on Github. You should see a banner suggesting you submit a pull request to the original repo. 
If you don't see this, choose the **Pull Request** tab from the ribbon of options at the top of the page and click the 
**New Pull Request** button.
    
    
5. Type in a title and description for your pull request.

   In the description of your pull request be sure to reference the issue you are fixing by simply typing
   `#` followed by the issue number.


6. Click **Create pull request**.

#### Github guides
More detailed instructions on creating a pull request and autolinked references to urls, issues, etc, can be 
found at the following links:

+ https://help.github.com/articles/creating-a-pull-request/ 
+ https://help.github.com/articles/autolinked-references-and-url

## How to rebase to forked origin

### Step 1 (Add the original repo as a git remote):

```
git remote add upstream https://github.com/charlottejuniordevs/client
```

### Step 2 (update git with latest in original repo):
    
```
git fetch upstream
```

### Step 3 (update your branch to what's latest in original repo):
    
```
git rebase upstream/master
```

To do an interactive rebase, add the `-i` flag to your command

```
git rebase -i upstream/master
```

Follow this link to the official Git documentation for more information on git-rebase:
https://git-scm.com/docs/git-rebase