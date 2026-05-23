# Number Guessing Game - Git Workflow Documentation

## Project Overview

This is a simple Java number guessing game built using Gradle. The player tries to
guess a random number within a range, and the program gives feedback until the correct
number is found or the user quits.

The project was developed using multiple Git branches to simulate a real development
workflow.

---

## Branch Structure

### main

This is the stable version of the project. It contains the working baseline code.

---

### dev

This branch is used for integrating features before they are added to main. Most
development work is merged here first.

---

### feature1

This branch improves user interaction. It includes:

- Ability to quit the game using a negative number
- Play again loop after finishing a game
- Small improvements to user messages

---

### feature2

This branch adds extra game rules such as:

- Maximum number of attempts
- Game over condition when attempts run out

---

### feature3

This branch contains experimental features:

- Hint system for helping the user
- Multiple commits were made during development (this branch will be squashed before
  merging)

---

### hotfix

This branch fixes an important bug:

- The random number generator did not include the maximum value
- This fix is applied directly to main before being merged back into dev

---

- Each feature was developed in a separate branch
- Merges were done into dev after testing
- Some conflicts were resolved manually
- hotfix was applied to main first

---

## Git Workflow Summary

### Merge vs Rebase vs Squash vs Cherry-pick

---

**Merge**

- Combines branches and keeps full history
- Used for integrating features into `dev` or `main`

**Rebase**

- Moves commits onto a new base for linear history
- Used to update feature branches before merging

**Squash**

- Combines multiple commits into one clean commit
- Used to clean up feature history (e.g., feature3)

**Cherry-pick**

- Applies a single commit to another branch
- Used for hotfixes without full merges

---

### Project Observations

- **feature1**: Direct merge, includes merge commits
- **feature2**: Required conflict resolution after updates
- **feature3**: Squashed into a single clean commit
- **hotfix**: Cherry-picked into `main`, then merged into `dev`

---

### When to use

- **Merge**: final integration
- **Rebase**: keep history linear
- **Squash**: simplify commits
- **Cherry-pick**: urgent fixes

---

### Summary

- `dev` should stay clean
- Feature branches can be messy internally
- Squash/rebase improve history
- Hotfixes must go to both `main` and `dev`
