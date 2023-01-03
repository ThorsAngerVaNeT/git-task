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

## `bullseye-game` branch
1) Rephrase `6nca2b12` commit, replace `feat` with `docs`
2) Split `acd5804b` commit to 3 commits for each file
3) Merge `bullseye-game` branch to `develop` branch

## `cub-n-pup-game` branch
1) Merge 3 commits (`3cba260d`, `e4630d3d`, `1870aa2d`) into 1 commit
2) Merge `cub-n-pup-game` branch to `develop` branch

## `menja` branch
1) Reorder commits of branch to reverse order
2) Rebase `menja` branch to `develop` branch

## `develop` branch
1) Setting up deployment to GH Pages from `develop` branch