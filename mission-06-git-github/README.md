# Mission 6 - Git and GitHub

## 1. Task / objective

Check Git status and history, stage and commit a selected README, create an `update-about` branch, add a My Learning section and open a Pull Request.

## 2. Work completed

Before editing, `git status` showed that `main` was up to date with `origin/main`. `git log --oneline` showed the completed mission commits in order. I created `update-about` from `main`, added three things I had learned to the root README, committed the README change and pushed the branch.

I opened [Pull Request #1](https://github.com/krishnachandanofficial-PRO/digital-detective-8516/pull/1) from `update-about` into `main`. The PR shows one commit and one changed file, the root `README.md`. Its current status is **open and not merged**. The `update-about` branch and My Learning section are visible on GitHub.

For the mission documentation, I staged this specific README, made a separate Mission 6 commit on `main` and checked the recent history.

### Git command glossary

| Operation | Command | What it does |
| --- | --- | --- |
| Initialise a repository | `git init` | Starts Git history in a local folder. |
| Check status | `git status` | Shows my branch and which files have changed or are staged. |
| Stage selected changes | `git add path/to/file` | Chooses a file change for the next commit. |
| Commit changes | `git commit -m "message"` | Saves the staged changes in local history with a message. |
| View history | `git log --oneline` | Shows recent commits in a short list. |
| Create or list branches | `git switch -c update-about` or `git branch` | Creates a branch or lists the branches. |
| Switch branches | `git switch main` | Changes the branch I am working on. |
| Publish changes | `git push` | Sends local commits or a branch to GitHub. |
| Retrieve remote changes | `git pull` | Brings remote commits into the current local branch. I did not need it because this PR remains open. |

## 3. Commands / tools used

I used `git status` to check the repository, `git add` to stage a selected README, `git commit` to save changes, and `git log` to check history. I used `git switch -c`, `git branch`, `git switch` and `git push` for the branch workflow. I used GitHub in Safari to compare the branches and create the Pull Request. `git pull` is listed in the glossary, but was not run in this mission.

## 4. My understanding

`git add` and `git commit` are different. Add puts the changes I choose in a staging area, and commit saves those staged changes as one point in the local history. Push then sends the commit to GitHub so it is visible online.

A branch lets me work on a README change separately from `main`. The Pull Request shows the difference between the branch and `main` and gives a place to review it before merging. This is useful when people work together because they can see the change before it becomes part of the main branch.

## 5. Difficulties faced

No major difficulty.

## 6. How I resolved them

Not applicable.

## 7. Evidence / files

The root `README.md` on `update-about` has the My Learning section. [Pull Request #1](https://github.com/krishnachandanofficial-PRO/digital-detective-8516/pull/1) shows the branch comparison. This README has the command glossary and workflow notes.

## 8. Commit details

Branch commit: `Add my learning notes to project README` on `update-about`.

Mission commit: `Complete Git and GitHub collaboration mission` on `main`. Both branches were pushed to GitHub.
