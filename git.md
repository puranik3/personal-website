# Git and GitHub

## Create GitHub repository
- Login to GitHub
- Create new repository
- Add collborators

## Cloning a repository
```
git clone https://github.com/puranik3/personal-website.git
```

## Commiting files and pushing it
- Add a file git.md to the repository folder. Now commit and push it to GitHub.
```
git add .
git commit -m "first commit - added a file for documenting Git usage"
git push
```

## Working with a feature branch
- Create `feature/my-feature` from develop locally and switch to the feature branch
- Code and commit the feature.
- When you are ready to share your work, switch to local `develop` and pull all changes from `origin/develop`
```
git checkout develop
git pull
```
- Switch to your feature branch. Get all commits from develop to the feature branch. This makes sure you do not face merge issues when you raise the Pull Request (PR). Finally pull (with rebase as commit ids change during `git rebase develop`) and push `origin/feature/my-feature`.
```
git checkout feature/my-feature
git rebase develop
git pull --rebase
git push
```
- Now raise the PR to merge from feature branch to develop branch on GitHub.