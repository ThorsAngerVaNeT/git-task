# git-task

⚠️ DO NOT SUBMIT PULL REQUESTS TO THIS REPO ⚠️

---

## Prerequisites
1. Fork this repository with all branches: https://github.com/ThorsAngerVaNeT/git-task. Don't forget to uncheck `Copy the master branch only` checkbox.
2. Clone your newly created repo: https://github.com/<%your_github_username%>/git-task/  
3. Go to folder `git-task`
4. Suggestion: set up VSCode as your Git editor - `git config --global core.editor "code --wait"`

---

## Submit to [RS App](https://app.rs.school)
1. Create PR from **your** `develop` branch to **your** `main` branch, and ignore the message `Can’t automatically merge`
2. Describe PR like [here](https://docs.app.rs.school/#/platform/pull-request-review-process?id=description-example)
2. Open [RS App](https://app.rs.school) and login
3. Go to `Cross-check: Submit` page
4. Select your task (Git Task)
5. Input link to your PR
6. Press the submit button and enjoy

---

## General Task Description
You have a repository with multiple branches:  
  - `main` - main branch of a repository with task requirements and description
  - `develop` - branch that holds an actual state of our main page  
  - `main-page-base` - branch that holds an initial design of the main page and already has been merged to the `develop` branch  
  - multiple feature branches:
    - `bullseye-game` - branch with 5 commits of Bullseye Game by Elliot Geno
    - `cub-n-pup-game` - branch with 6 commits of Cub n Pup Game by Dave DeSandro
    - `menja` - branch with 4 commits of Menja Game by Caleb Miller
    - `link-new-style` - branch with 4 commits of the new style of the main page

Your task is to manipulate branches and commits like it is described in [Task](#task).  
Resolving conflicts while merging/rebasing is a part of this task.  
**The preferable way** of solving the task is by using Git CLI, but you could also use `Git Graph` and `Git Lense` VSCode extensions to visualize branches and so on.  
The deployed page should be like in [the demo](https://rss-git-task.netlify.app) and all games should work correctly too.

---

## Task 
1) `bullseye-game` branch  
  1.1) Replace commit prefix `feat` with `docs` in `feat(bullseye): add license and readme` commit title.  
  1.2) Split `feat(bullseye): add game` commit to 3 commits for each file (`index.html`, `style.css`, `script.js`). They should be in place of the old commit, which means commits should be in the following order (from the oldest to the newest): 
    ```
    1. docs(bullseye): add license and readme
    2. feat(bullseye): add index.html
    3. feat(bullseye): add style.css
    4. feat(bullseye): add script.js
    5. feat(bullseye): add link to game in main page
    6. feat(bullseye): add external dependencies as local files
    7. feat(bullseye): update main page style
    ```
    The #2-4 commit titles could vary.  
  1.3) Merge the `bullseye-game` branch into the `develop` branch with the creation of a merge commit.

2) `cub-n-pup-game` branch  
  2.1) Merge 3 commits (`feat(cub-n-pup): add index.html`, `feat(cub-n-pup): add script.js`, `feat(cub-n-pup): add style.css`) into 1 commit in place of them, commits should be in the following order (from the oldest to the newest):  
    ```
    1. docs(cub-n-pup): add license and readme
    2. feat(cub-n-pup): add cub-n-pup game sources
    3. feat(cub-n-pup): add link to game in main page
    4. feat(cub-n-pup): update main page style - specify width
    ```
    The #2 commit title could vary.  
  2.2) Merge **squashed** `cub-n-pup-game` branch to `develop` branch.

3) `menja` branch  
  3.1) Reorder commits of the branch to reverse order, commits should be in the following order (from the oldest to the newest):  
    ```
    1. docs(menja): add license and readme
    2. feat(menja): add game files
    3. feat(menja): add link to game in main page
    4. feat(menja): update main page style - add text-align center
    ```
    3.2) Rebase `menja` branch into `develop`.
  
4) `link-new-style` branch  
  4.1) Cherry-pick all commits from the `link-new-style` branch **with references to original commits** to `develop` branch.

5) `develop` branch  
  5.1) Set up deployment to GH Pages from the `develop` branch.

---

## Scoring
Maximum - 45 points

### Basic Scope
- `bullseye-game` branch - **total 15 points**
  - there is no `feat(bullseye): add license and readme` commit and there is `docs(bullseye): add license and readme` commit - **+5 points**
  - there is no `feat(bullseye): add game` and there are 3 new commits in place of it for each file (`index.html`, `style.css`, `script.js`) - **+5 points**
  - `bullseye-game` branch merged to `develop` branch with created merge commit - **+5 points**
- `cub-n-pup-game` branch - **total 10 points**
  - there are no `feat(cub-n-pup): add index.html`, `feat(cub-n-pup): add script.js`, `feat(cub-n-pup): add style.css` commits and there is a new commit contains them and placed in place of them - **+5 points**
  - The **squashed** `cub-n-pup-game` branch was merged with to `develop` branch, there is a squashed commit - **+5 points**
- `menja` branch - **total 10 points**
  - there are 4 commits in the following order (from the oldest to the newest) - **+5 points**:
    ```
    1) `docs(menja): add license and readme`
    2) `feat(menja): add game files`
    3) `feat(menja): add link to game in main page`
    4) `feat(menja): update main page style - add text-align center`
    ```
  - `menja` branch was rebased into `develop` branch - **+5 points**
- `link-new-style` branch - **total 5 points**
  - all commits were cherry-picked to the `develop` branch with references to original commits - **+5 points**
- there is a deployment at GH Pages - **+5 points**

### Penalties
- there is a PR to the [original repository](https://github.com/ThorsAngerVaNeT/git-task) - -20 points
- `bullseye-game` branch commits not in the order specified in Task 1.2 - -15 points
- `cub-n-pup-game` branch commits not in the order specified in Task 2.1 - -10 points
- `menja` branch commits not in the order specified in Task 3.1 - -10 points
