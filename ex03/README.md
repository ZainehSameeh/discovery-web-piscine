# Git Workflow & Secure Authentication

## Overview

This exercise introduces the basic Git workflow used to manage, track, and share changes in a project.

The main workflow is:

```text
Edit → Add → Commit → Push
```

The exercise also covers secure authentication with an Ed25519 SSH key pair as a bonus requirement.

## Why Git Makes Development Easier

Git makes development easier by keeping track of changes to a project over time. Instead of manually creating different copies of files, Git allows developers to save specific versions of their work through commits.

Version control helps safeguard code because previous versions are preserved in the project's history. If a change causes a problem, developers can review earlier commits and return to a previous working version.

Git also makes it easier to track the development of a project. Commands such as `git log` provide a history of commits, making it possible to see what changes were made and when they were made.

Git is also useful for collaboration. Developers can work on the same project, record their changes, and share them through a remote repository such as GitHub. This provides a clear history of changes and makes it easier for team members to work together.

## Git Workflow

The workflow used in this exercise consists of four main steps.

### 1. Edit

Create or modify files in the project.

### 2. Add

Stage the changes that should be included in the next commit:

```bash
git add .
```

### 3. Commit

Save the staged changes in the Git history with a descriptive message:

```bash
git commit -m "Describe the changes"
```

### 4. Push

Send the local commits to the remote GitHub repository:

```bash
git push
```

The complete workflow can be summarized as:

```text
Edit
 ↓
git add
 ↓
git commit
 ↓
git push
```

This cycle can be repeated whenever changes are made to the project.

## Git History

Git keeps a record of previous commits. The project's commit history can be viewed using:

```bash
git log
```

This makes it possible to review how the project has changed over time.

## Secure Authentication with SSH

As part of the bonus requirement, an Ed25519 SSH key pair can be used to authenticate with GitHub.

The key pair consists of:

* **Private key:** Kept secret on the local machine and never committed or submitted.
* **Public key:** Added to GitHub for authentication and submitted as `id_ed25519_pub.txt`.

The repository remote can be configured to use SSH:

```text
git@github.com:username/repository.git
```

With SSH authentication configured, Git operations such as `git push` can be performed securely without entering a GitHub password.

## Security

Private credentials should never be committed to a repository. The private SSH key must remain on the local machine and must not be uploaded to GitHub or submitted for this exercise.

Only the public SSH key should be shared or submitted.

