# adebayo-owolabi-w3-version-control
Version Control

Version control is a system that tracks changes to files over time. It allows developers to:

Record Changes: Keep a history of edits to code or documents.
Collaborate: Work together without overwriting each other's changes.
Revert: Roll back to earlier versions if something goes wrong.
Branching and Merging: Create separate "branches" for new features or experiments and merge them back when ready.
Difference Between Git and GitHub
Git: A distributed version control system that runs on your computer. It tracks changes, allows branching/merging, and manages code locally.
GitHub: A cloud-based platform for hosting Git repositories. It provides collaboration tools, issue tracking, and a web interface for Git projects.

Alternatives to GitHub
GitLab: A Git-based platform with built-in CI/CD tools.
Bitbucket: Supports Git and Mercurial repositories, often used with Atlassian tools like Jira.
Azure DevOps: Offers version control and CI/CD features, integrated with Microsoft's ecosystem.
Difference Between git fetch and git pull
git fetch: Downloads changes from a remote repository without merging them into your local branch. It updates only the metadata.
Use it when you want to see what others have done without altering your work.
git pull: Fetches changes and merges them into your current branch in one step.
Use it to update your branch with the latest changes from the remote repository.

Git Rebase (Simple Explanation)
Rebasing re-applies your changes on top of another branch's history, making the commit history linear and cleaner.

Example:
Before rebasing:
mathematica
Copy code
master: A---B---C
feature:       D---E
After git rebase master on the feature branch:
mathematica
Copy code
master: A---B---C
feature:             D'---E'
Command:
bash
Copy code
git checkout feature
git rebase master

Git Cherry-Pick (Simple Explanation)
Cherry-picking takes a specific commit from one branch and applies it to another branch without merging the entire branch.

Example:
If a branch has these commits:
mathematica
Copy code
feature: A---B---C---D
You can pick only commit C and apply it to main.
Command:
bash
Copy code
git checkout main
git cherry-pick <commit-hash>
This is useful when you want to apply a bug fix or feature from one branch to another without merging unrelated changes.
