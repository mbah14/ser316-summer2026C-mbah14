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
