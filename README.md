# git-task

⚠️ DO NOT SUBMIT PULL REQUESTS TO THIS REPO ⚠️

---

## Prerequisites
1. Fork this repository: https://github.com/ThorsAngerVaNeT/git-task
2. Clone your newly created repo: https://github.com/<%your_github_username%>/git-task/  
3. Go to folder `git-task`

---

## Submit to [RS App](https://app.rs.school)
1. Create PR from **your** `develop` branch to **your** `main` branch, ignore message `Can’t automatically merge`
2. Describe PR like [here](https://docs.app.rs.school/#/platform/pull-request-review-process?id=description-example)
2. Open [RS App](https://app.rs.school) and login
3. Go to submit task page
4. Select your task (Git Task)
5. Input link to your PR
6. Press the submit button and enjoy

---

## General Task Description
You have repository with multiple branches:  
  - `develop` - branch that holds actual state of our main page  
  - `main-page-base` - branch that holds initial design of main page and already have been merged to `develop` branch  
  - multiple feature branches:
    - `bullseye-game` - branch with 4 commits of Bullseye Game by Elliot Geno
    - `cub-n-pup-game` - branch with 6 commits of Cub n Pup Game by Dave DeSandro
    - `menja` - branch with 4 commits of Menja Game by Caleb Miller
    - `link-new-style` - branch with 4 commits of new style of main page

You task is to manipulate branches and commits like it described in [Task](#task) and if task will be implemented correctly you will have page like in [demo](https://rss-git-task.netlify.app) and all games will work correctly too.

## Task 
1) `bullseye-game` branch  
  1.1) Rephrase `6nca2b12` commit, replace `feat` with `docs`.  
  1.2) Split `acd5804b` commit to 3 commits for each file (`index.html`, `style.css`, `script.js`). They should be in place of `acd5804b` commit.
  1.3) Merge `bullseye-game` branch to `develop` branch with creation of a merge commit.

2) `cub-n-pup-game` branch  
  2.1) Merge 3 commits (`3cba260d`, `e4630d3d`, `1870aa2d`) into 1 commit in place of them.  
  2.2) Merge **squashed** `cub-n-pup-game` branch to `develop` branch.

3) `menja` branch  
  3.1) Reorder commits of branch to reverse order.  
  3.2) Rebase `menja` branch into `develop`.
  
4) `link-new-style` branch  
  4.1) Cherry-pick all commits from `link-new-style` branch with references to original commits to `develop` branch.

5) `develop` branch  
  5.1) Setting up deployment to GH Pages from `develop` branch.

## Scoring
Maximum - 45 points

### Basic Scope
- `bullseye-game` branch - total 15 points
  - there is no `feat(bullseye): add license and readme` commit and there is `docs(bullseye): add license and readme` - +5 points
  - there is no `feat(bullseye): add game` (`acd5804b`) and there are 3 new commits in place of it for each file (`index.html`, `style.css`, `script.js`) - +5 points
  - `bullseye-game` branch merged to `develop` branch with created merge commit - +5 points
- `cub-n-pup-game` branch - total 10 points
  - there are no `3cba260d`, `e4630d3d`, `1870aa2d` commits and there is a new commit contains them and placed in place of them - +5 points
  - **squashed** `cub-n-pup-game` branch merged to `develop` branch, there is a squashed commit - +5 points
- `menja` branch - total 10 points
  - there are 4 commits in following order (from oldest to newest) - +5 points:
    1) `docs(menja): add license and readme`
    2) `feat(menja): add game files`
    3) `feat(menja): add link to game in main page`
    4) `feat(menja): update main page style - add text-align center`
  - `menja` branch rebased into `develop` branch - +5 points
- `link-new-style` branch - total 5 points
  - all commits cherry-picked to `develop` branch with references to original commits - + 5 points
- there is a deployment at GH Pages - + 5 points

### Penalties
- there is a PR to [original repository](https://github.com/ThorsAngerVaNeT/git-task) - -20 points
