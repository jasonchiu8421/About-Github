# 💼 How GitHub Is Used in Professional Software Engineering

GitHub is **not just a place to store code**.  
In real companies it becomes the **central hub for collaboration**, **version control**, **code review**, **automation**, and **project management**.

Think of GitHub as the engineering team’s:

*   **Source of truth for code**
*   **Collaboration platform**
*   **Documentation library**
*   **Automation engine**
*   **Audit and security system**

Let’s go step-by-step.

***

# 1. 🔐 GitHub as the Source of Truth (Version Control)

Professionally, every change to the codebase must be:

*   tracked
*   reviewable
*   reversible
*   documented

Teams use **Git** and GitHub together.

### What this looks like in practice:

*   You **clone** the repo → `git clone`
*   You create a **branch** → `git checkout -b feature/login-page`
*   You write code
*   You **push** your branch to GitHub → `git push`
*   You create a **Pull Request (PR)**

Every change goes through GitHub—no exceptions.

***

# 2. 🌿 Branching Strategy (Team Workflow)

Companies follow branching models so multiple developers can work safely in parallel.

Common strategies:

### **GitFlow**

*   `main` → production-ready
*   `develop` → next release
*   `feature/*` → features
*   `hotfix/*` → emergency fixes

### **Trunk-based development**

*   Developers branch off `main`
*   Merge small PRs multiple times a day

### What fresh grads need to know:

You **never** commit directly to `main`.  
You **always** create a branch and submit a PR.

***

# 3. 📝 Pull Requests (The Heart of Collaboration)

Pull Requests (PRs) are how code gets merged professionally.

A good PR includes:

✔ Small change set (easy to review)  
✔ Clear description (what/why)  
✔ Linked tasks/issues  
✔ Unit tests  
✔ Screenshots (for UI changes)

### Example PR description:

    Title: Add login page UI

    - Added LoginPage.vue component
    - Implemented basic form validation
    - Added unit tests (Jest)
    - Linked to ISSUE-124: User Authentication

    Tested on Chrome + Safari

***

# 4. 👀 Code Review (Quality + Knowledge Sharing)

Every PR must be reviewed by another engineers.

Reviewers check for:

*   Correctness
*   Code quality & readability
*   Security vulnerabilities
*   Performance issues
*   Test coverage
*   Architectural alignment

You’ll often see comments like:

> “Can we extract this into a helper function?”  
> “This variable name is unclear.”  
> “What happens if the API returns null?”

New engineers learn *a ton* from code reviews.

***

# 5. 🤖 GitHub Actions (Automation in Real Projects)

Companies automate tasks on GitHub using **GitHub Actions**, such as:

*   Running automated tests
*   Running linting & formatting
*   Building the application
*   Deploying to QA/staging environments
*   Security scanning
*   Tagging releases

Typical workflow:

    on: pull_request
    jobs:
      test:
        runs-on: ubuntu-latest
        steps:
          - run: npm install
          - run: npm test

If tests fail → the PR cannot be merged.

***

# 6. 🎯 Project Management (GitHub Issues & Projects)

Product managers, engineers, and designers use GitHub for:

*   Tracking features
*   Logging bugs
*   Maintaining roadmaps
*   Sprint planning (Agile)

### GitHub Issues are used for:

*   Bug reports
*   Feature requests
*   Documentation tasks
*   Security vulnerabilities

### GitHub Projects:

*   Kanban boards (To Do → In Progress → Done)
*   Sprint cycles
*   Progress tracking

***

# 7. 📚 Documentation (README, Wikis, ADRs)

Professional teams use GitHub to store documentation such as:

*   **README.md** for setup instructions
*   **Architecture Decision Records (ADRs)** for design decisions
*   **API docs**
*   **Runbooks for on-call engineers**

Good documentation is expected—not optional.

***

# 8. 🔒 Security & Permissions

In real companies:

*   Access is controlled (least privilege principle)
*   Secrets are stored in GitHub Secrets (never in code)
*   Dependabot alerts security vulnerabilities
*   Protected branches prevent direct pushes

You’ll often see:

✔ Required PR approvals  
✔ Required test checks  
✔ No force-push to main  
✔ Mandatory reviews on sensitive code

***

# 9. 🧪 Environments & Releases

GitHub integrates with CI/CD pipelines to handle deployments.

Common environments:

*   Development
*   QA
*   Staging
*   Production

Teams use Release Tags, e.g.:

`v1.0.5` — hotfix  
`v2.1.0` — new features  
`v3.0.0` — breaking changes

Release notes are auto‑generated.

***

# 10. 🧘 Professional Practices

*   Commit small, meaningful changes
*   Write good PR descriptions
*   Follow the branching strategy
*   Pass test/lint pipelines
*   Respond to code review feedback
*   Keep your branch up to date
*   Never push directly to main

Also…

If something breaks, GitHub has a full history so the team can investigate.
