# DevOps Foundation Training 

## DAY - 1

---

# 1️⃣ SDLC Models – Agile vs Waterfall

## What is SDLC?

SDLC (Software Development Life Cycle) is the structured process used to design, develop, test, and deploy software.

---

## 🔵 Waterfall Model

### Definition
Waterfall is a linear and sequential development model where each phase must be completed before moving to the next.

### Flow
Requirement → Design → Development → Testing → Deployment → Maintenance

### Key Characteristics
- Fixed scope
- Heavy documentation
- Late testing
- Difficult to accommodate changes
- Suitable for stable requirements

### Real-World Use Cases
- Government projects
- Banking systems
- Regulatory systems

### Why Not Ideal for DevOps?
- No continuous feedback
- Testing happens late
- Deployment only at end
- No CI/CD integration

---

## 🟢 Agile Model

### Definition
Agile is an iterative and incremental methodology that delivers software in small, usable pieces.

### Core Principles
- Frequent delivery of working software
- Continuous feedback
- Collaboration
- Adaptability to change

### Sprint Duration
Typically:
- 2 weeks
- 3 weeks
- 4 weeks

### Why Agile Fits DevOps?
- Supports Continuous Integration
- Supports Continuous Deployment
- Enables faster feedback loops
- Small incremental releases

---

# 2️⃣ Agile Terminologies

---

## 📘 Epic

A large feature that cannot be completed in one sprint.

Example:
> User Management System

---

## 📗 User Story

A small requirement written from the user's perspective.

### Format:
> As a <role>, I want <feature>, so that <benefit>

Example:
> As an admin, I want to create users so that I can manage access.

### INVEST Criteria
- Independent
- Negotiable
- Valuable
- Estimable
- Small
- Testable

---

## 📙 Task

Technical work required to complete a story.

Example:

Story: Create user

Tasks:
- Create API
- Create DB schema
- Write unit test
- Configure CI pipeline

---

## 🏃 Sprint

A fixed time-boxed iteration where selected stories are completed.

### Sprint Activities:
- Sprint Planning
- Daily Standup
- Development
- Testing
- Sprint Review
- Retrospective

---

# 3️⃣ Git & GitHub for DevOps Engineers

---

## What is Git?

Git is a distributed version control system used to track changes in:
- Application code
- Infrastructure as Code (Terraform)
- Kubernetes manifests
- CI/CD pipelines
- Configuration files

---

## What is GitHub?

GitHub is a cloud platform for hosting Git repositories.

### Features:
- Remote repositories
- Pull Requests
- Code reviews
- Branch protection
- CI/CD integration (GitHub Actions)

---

# 4️⃣ Core Git Concepts

---

## Repository
A project folder tracked by Git.

---

## Commit
A snapshot of changes.

---

## Branch
An independent line of development.

Common branches:
- main
- master
- feature/*
- bugfix/*

---

## Merge
Combines changes from one branch into another.

---

## Pull Request (PR)
A request to merge code into the main branch.

---

# 5️⃣ Git Commands Required for DevOps Engineers

---

## 🔹 Setup

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

---

## 🔹 Initialize Repository

```bash
git init
```

---

## 🔹 Clone Repository

```bash
git clone <repo-url>
```

---

## 🔹 Check Status

```bash
git status
```

---

## 🔹 Add Files

Add single file:

```bash
git add file.txt
```

Add all files:

```bash
git add .
```

---

## 🔹 Commit

```bash
git commit -m "Added Dockerfile"
```

---

## 🔹 View History

```bash
git log
git log --oneline
```

---

## 🔹 Branching

Create branch:

```bash
git checkout -b feature/docker-setup
```

Switch branch:

```bash
git checkout main
```

---

## 🔹 Push Changes

```bash
git push origin main
```

Push new branch:

```bash
git push origin feature/docker-setup
```

---

## 🔹 Pull Changes

```bash
git pull origin main
```

---

## 🔹 Fetch

```bash
git fetch
```

(Fetch downloads changes but does NOT merge automatically.)

---

## 🔹 Merge

```bash
git merge feature/docker-setup
```

---

## 🔹 Rebase (Advanced)

```bash
git rebase main
```

---

## 🔹 Stash

```bash
git stash
git stash pop
```

---

## 🔹 View Differences

```bash
git diff
```

---

## 🔹 Delete Branch

```bash
git branch -d feature/docker-setup
```

---

## 🔹 Tagging Releases

```bash
git tag v1.0
git push origin v1.0
```

---

# 6️⃣ Git Workflow in DevOps Projects

---

## Feature Branch Workflow

1. Pull latest main branch
2. Create feature branch
3. Make changes
4. Commit changes
5. Push branch
6. Create Pull Request
7. Code review
8. Merge to main
9. CI/CD triggers deployment

---

# 7️⃣ Real DevOps Use Cases of Git

---

## Infrastructure as Code
Terraform files stored and version controlled in Git.

## Kubernetes Deployments
deployment.yaml, service.yaml tracked in Git.

## GitOps
Tools like ArgoCD pull manifests from Git and deploy automatically.

## CI/CD
GitHub Actions triggers on:
- push
- pull_request

---

# 8️⃣ Important Interview Topics

Make sure you understand:

- git fetch vs git pull
- merge vs rebase
- conflict resolution
- squash commits
- branching strategies (GitFlow vs Trunk-Based)
- .gitignore usage
- release tagging

---

# 9️⃣ Practice Exercise

1. Create a GitHub repository
2. Add:
   - Dockerfile
   - README.md
   - Kubernetes deployment.yaml
3. Create a feature branch
4. Raise a Pull Request
5. Merge into main
6. Setup simple GitHub Action workflow

---


