This repo is a personal learning log for mastering Git and GitHub Actions, with a focus on applying CI/CD workflows to detection engineering projects and mastering devsecops.

## Code Deployment (CI/CD)
Automate code testing, building and deployment

## Code & Repo Management
Automate code reviews, issue management etc.

## Crash Course in Git
Allows us to manage source code changes:
- Save code snapshots: **commits**
- Work with alternative code versions: **branches**
- Move btwn branches & commits: **checkout**
- Cloud Git repo storage: **push & pull**
- Move between commits: **git checkout <id>**
- Code mgmt & collaborative devpt: issues, projects, PRs
- Automation & CI/CD: GitHub Actions

### Git Workflow
- git add <file(s)> or .
- git commit
- git push

### Common git commit message formats
- feat: a new feature
- fix: a bug fix
- docs: documentation only changes
- style: formatting
- test: add missing tests
- chore: changes to the build process/auxiliary tools

Examples:
```
feat(ci): add initial GitHub Actions workflow for CI

fix(gitignore): exclude .env files from version control

docs(readme): add learning objectives for Git and GitHub Actions

refactor(workflow): rename job steps for clarity
```

Points to note:
- Use imperative mood e.g. add
- Use present tense

### Undo commits
Use git revert \<id>
This is used to revert changes of commit by creating a new commit

### Resetting code
`git reset --hard <id>` is used to undo changes by deleting all commits since \<id>.  
We end up losing history with this

### Ignoring files with .gitignore
Allows us to specify folders and files to ignore
For example, if using MacOS and VS code, the .gitignore would look like:
```
.vscode
.DS_Store
```

### 🪾Branches

```mermaid
gitGraph
   commit id: "Initial Commit"
   branch develop
   checkout develop
   commit id: "Add README"
   branch feature/login
   checkout feature/login
   commit id: "Create login UI"
   checkout develop
   merge feature/login
   commit id: "Release v1.0"
   checkout main
   merge develop id: "Merge develop into main after release"
```

