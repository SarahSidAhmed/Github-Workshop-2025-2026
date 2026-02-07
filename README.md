# GitHub Workshop 

Welcome to the GitHub Hands-on Workshop!

## Objectives
By the end of this workshop, you will be able to:
- Use Git locally
- Work with branches
- Commit changes
- Open Pull Requests
- Review code
- Understand GitHub Actions (CI)

---

## Tasks

### 1. Clone the repository
```bash
git clone <repo-url>
cd github-workshop
```

### 2. Create a new branch
```bash
git checkout -b feature/<your-name>
```

### 3. Create your profile
```bash
students/<yourname>.md
```

Exmaple content:
```bash
# Your Name

- University:
- Level:
- Favorite Programming Language:
```

### 4. Commit your changes
```bash
git add .
git commit -m "Add my profile"
```

### 5. Push your branch
```bash
git push origin feature/<your-name>
```

### 6. Open a Pull Request on GitHub
### 7. Review another student's Pull Request
### 8. Resolve conflicts if they appear
### 9. Check GitHub Actions status
```bash

---

## ⚙️ GitHub Actions – `.github/workflows/ci.yml`

```yaml
name: Simple CI

on: [push, pull_request]

jobs:
  check:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4

      - name: Check students folder exists
        run: |
          test -d students

      - name: List students
        run: |
          ls students
```
### 10. Create a conflict
Try editing line 1 of the file conflicts.txt by writing your name in it and commit with another student.
Resolve the conflit before merging.

