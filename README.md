# 🚀 DevOps Project with Git

A hands-on project to demonstrate **version control best practices** and **collaborative DevOps workflows** using Git and GitHub.
This repository follows a professional branching model with CI integration and release management.

---

## 📘 Project Overview

This project simulates a real-world DevOps environment where version control and collaboration are essential.
It demonstrates how to:

* Manage multiple branches (`main`, `dev`, and `feature/*`)
* Use Pull Requests for code reviews
* Implement basic CI workflows using **GitHub Actions**
* Maintain clean commit history and documentation
* Tag stable versions for release (`v1.0.0` and beyond)

---

## 🧱 Repository Structure

```
my-devops-project/
│
├── .github/
│   └── workflows/
│       └── ci.yml              # Basic GitHub Actions CI workflow
│
├── docs/
│   └── notes.md                # Additional documentation
│
├── README.md                   # Project overview and instructions
├── TASKS.md                    # Task tracking and progress
├── .gitignore                  # Ignored files and folders
└── ...
```

---

## 🧩 Branching Strategy

| Branch      | Purpose                                             |
| ----------- | --------------------------------------------------- |
| `main`      | Production-ready code (protected branch)            |
| `dev`       | Integration branch for testing and merging features |
| `feature/*` | Individual short-lived feature branches             |

**Flow:**

1. Create a new branch from `dev`

   ```bash
   git checkout dev
   git checkout -b feature/add-new-feature
   ```
2. Commit and push your changes

   ```bash
   git add .
   git commit -m "feat: describe feature"
   git push -u origin feature/add-new-feature
   ```
3. Open a **Pull Request** → `feature/*` → `dev`
4. Once approved and tested, merge `dev` → `main`

---

## ⚙️ Continuous Integration (CI)

A sample **GitHub Actions** workflow (`.github/workflows/ci.yml`) is configured to run on each push and pull request:

```yaml
name: CI
on: [push, pull_request]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Run sample step
        run: echo 'CI workflow running successfully!'
```

This validates basic functionality and ensures all PRs are automatically checked before merging.

---

## 🧾 Versioning and Tags

Semantic versioning is followed:

* `vMAJOR.MINOR.PATCH` (e.g., `v1.0.0`, `v1.1.0`)

Example commands:

```bash
git tag -a v1.0.0 -m "Initial release"
git push origin v1.0.0
```

---

## 🧰 Git Best Practices

* Commit messages follow the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) style:

  ```
  feat(scope): add something new
  fix(scope): correct a bug
  docs: update documentation
  chore: maintenance updates
  ```
* Every feature branch must go through a **Pull Request**
* Use `.gitignore` to keep the repo clean
* Document progress in `TASKS.md`

---

## 🗂️ Documentation

All project updates and goals are tracked in **TASKS.md**.

Example:

```markdown
## ✅ Completed
- Initialized Git repo and pushed to GitHub
- Created main, dev, and feature branches
- Added GitHub Actions CI workflow
- Merged feature to dev, dev to main
- Created tag v1.0.0

## 🔜 Next
- Add Dockerfile and Jenkins CI/CD
- Integrate Terraform for IaC
- Add monitoring with Prometheus & Grafana
```

---

## 🧩 How to Clone and Work on This Project

```bash
# Clone the repository
git clone https://github.com/Yasaswvene/DevOps-Project-with-Git.git

cd DevOps-Project-with-Git

# Create a new branch from dev
git checkout dev
git checkout -b feature/my-feature
```

---


## 🏁 Outcome

✅ You will learn:

* Real-world Git branching & merging workflow
* CI automation setup
* Collaborative development using Pull Requests
* Professional repository organization
* Tagging and release management with GitHub

---

**🎯 Goal:** Build confidence managing production-like DevOps projects with Git best practices.
