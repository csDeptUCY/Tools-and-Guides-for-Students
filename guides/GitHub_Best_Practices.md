# GitHub Best Practices

This guide presents the essential best practices for using GitHub effectively during your Computer Science studies and beyond. By following these practices, you will be able to keep your project history organized, collaborate effectively with your fellow students on group assignments, and apply professional software development methods.

GitHub is not simply a backup tool; it is a collaboration platform that allows you to work effectively as a team and track the progress of your work.

## Table of Contents

- [1. Commit Best Practices](#commit-best-practices)
  - [1.1 Write Descriptive Commit Messages](#write-descriptive-commit-messages)
  - [1.2 Commit Frequently and Logically](#commit-frequently-and-logically)
  - [1.3 Review Before Committing](#review-before-committing)
  - [1.4 What NOT to Commit](#what-not-to-commit)
- [2. Branching Strategies](#branching-strategies)
  - [2.1 Understanding Branches](#understanding-branches)
  - [2.2 When to Use Branches](#when-to-use-branches)
  - [2.3 Branch Naming](#branch-naming)
  - [2.4 Branch Workflow](#branch-workflow)
  - [2.5 Managing and Preventing Merge Conflicts](#managing-and-preventing-merge-conflicts)
- [3. Repository Organization](#repository-organization)
  - [3.1 Required Files](#required-files)
  - [3.2 Creating .gitignore Files](#creating-gitignore-files)
  - [3.3 Naming Conventions](#naming-conventions)
- [4. Collaboration Guidelines](#collaboration-guidelines)
  - [4.1 Team Communication](#team-communication)
  - [4.2 Work Allocation](#work-allocation)
  - [4.3 The Golden Rule of Collaboration](#the-golden-rule-of-collaboration)
- [5. Code Review Practices](#code-review-practices)
  - [5.1 Creating Pull Requests](#creating-pull-requests)
  - [5.2 Reviewing Pull Requests](#reviewing-pull-requests)
  - [5.3 Responding to Review Feedback](#responding-to-review-feedback)
  - [5.4 Pre-Review Checklist](#pre-review-checklist)
- [6. GitHub Usage Assessment Criteria](#github-usage-assessment-criteria)
  - [6.1 General Principles](#general-principles)
  - [6.2 Criteria for Individual Assignments](#criteria-for-individual-assignments)
  - [6.3 Criteria for Group Assignments](#criteria-for-group-assignments)
  - [6.4 Indicative Elements Assessed](#indicative-elements-assessed)
- [7. Conclusion](#conclusion)

# Commit Best Practices

Commits are the fundamental building blocks of your project history. Well-structured commits make it easier to understand what changes were made, when they were made, and why.

## Write Descriptive Commit Messages

**Examples of good commit messages:** `Implement binary search tree insertion method`, `Fix null pointer exception in calculateAverage()`, `Update README with installation instructions`

**Examples of bad commit messages:** `fixed stuff`, `update`, `asdf`, `done`, `changes`

Guidelines for commit messages:

- Use the imperative mood: `Add feature`, not `Added feature`

- Start with a capital letter and do not end with a period

- Be specific about what changed

- Explain the “why” behind non-obvious changes

## Commit Frequently and Logically

Commit after completing one logical unit of work, such as a new method or a fix, rather than waiting until dozens of changes have accumulated. Avoid very small or very large commits containing unrelated changes. A good commit:

- Implements one specific feature or fixes one specific bug

- Represents a complete, working state of the code

- Includes only the relevant files

## Review Before Committing

Before committing, use `git diff` or VS Code to see what you are about to submit. Make sure that you have removed any debug code and commented-out code, have not included files you added accidentally, and that the code compiles without errors.

## What NOT to Commit

Never commit:

- Compiled files (`.class`, `.o`, `.exe`, `.jar`, `.war`)

- Build directories (`target/`, `bin/`, `build/`)

- IDE-specific files (`.idea/`, `.vscode/settings.json`, `*.iml`)

- System files (`.DS_Store`, `Thumbs.db`)

- Temporary files (`*~`, `*.swp`, `*.tmp`) and log files (`*.log`)

- Environment information (`.env`)

- Sensitive information (passwords, API keys, tokens)

Use `.gitignore` to exclude these files or directories automatically.

**IMPORTANT:** If you accidentally commit sensitive data, immediately stop tracking the file with `git rm --cached <file>`, create a new commit, and immediately change the exposed credentials. The data remains visible in the history even after deletion—contact your instructor if you need help.

# Branching Strategies

Branches allow you to work on independent parts of the code without affecting the “official” version of your project. Keep your branching approach simple but structured.

## Understanding Branches

The main branch is the default branch (usually `main` or `master`). It should always contain working, stable code—it is the “official” version of the project from which assignments are usually submitted.

You can create new branches to develop new features or fixes. They are isolated from `main` and merged back into it when they are complete.

## When to Use Branches

**For individual projects:** Use branches when working on a challenging component that may take considerable time, when experimenting with different approaches, or when making significant changes to your code (code refactoring).

**For group projects (IMPORTANT):** Each member works on their assigned task in a separate branch. This prevents merge conflicts caused by simultaneous editing and allows code review before merging.

## Branch Naming

Use descriptive names with hyphens:

- Good names: `feature/user-authentication`, `feature/add-search-function`, `fix/null-pointer-bug`, `refactor/database-layer`

- Bad names: `test`, `new`, `mybranch`, `fix`

## Branch Workflow

1. Create and switch to a new branch

2. Work on the branch and commit as usual

3. Push the branch to GitHub

4. Switch to `main` and merge. For group assignments, this is usually done through a pull request (see Chapter 5)

5. Delete the branch after merging

## Managing and Preventing Merge Conflicts

Merge conflicts occur when the same lines are modified in different branches. To avoid them, work on different files or modules whenever possible, tell the team which files you will modify, run `git pull` from `main` frequently before starting work, and keep branches short-lived—merge them promptly.

**When VS Code displays merge conflicts:**

1. Open the file containing the conflict

2. VS Code highlights the conflict markers

3. Select “Accept Current Change,” “Accept Incoming Change,” or “Accept Both Changes”—or edit the code yourself

4. Save the file

5. Stage and commit the resolved file

# Repository Organization

Well-organized repositories are easier to navigate, understand, and maintain. Organize files logically by type and purpose (e.g., `src/`, `tests/`, `docs/`, `.gitignore`, `README.md`).

## Required Files

**`README.md`** (required for all assignments). It must include:

- The project title and description

- Installation/setup and execution instructions

- Requirements and dependencies

- Author information (for group assignments: a description of each member’s contribution)

**`.gitignore`** (required for all assignments) automatically excludes files that do not belong in version control.

**`Changelog.md`** (required for group assignments). It records noteworthy changes by version/date, with the most recent entry at the top.

## Creating .gitignore Files

GitHub provides ready-made templates for common programming languages. Examples of files that should be excluded:

- Compiled and executable files (`*.class`, `*.jar`, `*.war`, `*.o`, `*.exe`, `*.out`)

- Build directories (`target/`, `bin/`, `build/`, `__pycache__/`)

- IDE files (`.idea/`, `*.iml`, `.vscode/`)

- System files (`.DS_Store`, `Thumbs.db`)

- Virtual environments (`venv/`, `env/`)

- Jupyter checkpoints (`.ipynb_checkpoints/`)

## Naming Conventions

Repository names: use lowercase letters, separate words with hyphens, and keep names short and descriptive. Examples: `data-structures-project`, `web-shop-application`.

File and folder names should follow the conventions of the language (e.g., CamelCase for Java classes, snake_case for Python), be descriptive, avoid spaces, and remain consistent throughout the project.

# Collaboration Guidelines

Effective collaboration requires clear communication and agreed-upon processes. This section is critical to the success of group assignments.

## Team Communication

Before starting work: Discuss and agree on the project structure, identify the modules/building blocks and allocate responsibilities to team members accordingly, establish coding standards, and define communication channels.

During development: Announce which files/modules you are working on, update the team on progress and problems, and share discoveries and solutions.

## Work Allocation

**By feature/module (RECOMMENDED):**

- Each member implements complete features (e.g., Person A: user authentication, Person B: data processing)

- Minimizes merge conflicts

- Gives each person ownership of their area

**By layer:**

- Divide work by technical responsibility (e.g., Person A: UI, Person B: business logic, Person C: database)

- Requires careful interface design

- Makes merge conflicts more likely

## The Golden Rule of Collaboration

Pull → Work → Commit → Push

1. Pull the latest changes before you begin

2. Work on your assigned tasks

3. Commit frequently with descriptive messages

4. Push after completing a logical unit of work

# Code Review Practices

Code review improves code quality and helps team members learn from one another.

## Creating Pull Requests

When creating a pull request (PR):

- Write a clear title that describes the change

- Complete the description using the template below

- Link relevant issues, if any

- Assign reviewers from your team

PR description template:

1. What this PR does: Brief description of the changes

2. Why it is needed: Explanation of the problem being solved

3. How it was implemented: Brief technical overview

4. Testing: How was it tested? Which scenarios were covered?

## Reviewing Pull Requests

When reviewing code:

- Read the description first to understand the context

- Check that the code follows the project conventions

- Look for potential bugs or edge cases

- Confirm that the logic is correct and efficient

Good review comments: “The logic looks correct, but we could simplify it by using the built-in `sort()` instead of implementing our own.”

Bad review comments: “This is wrong.”, “Bad code.”

## Responding to Review Feedback

When receiving feedback:

- Do not take it personally—focus on improving the code

- Ask questions if the feedback is unclear

- Discuss alternatives if you disagree

- Make the requested changes in new commits

## Pre-Review Checklist

Before requesting a review, check that:

1. The code compiles without errors

2. All tests pass (if any)

3. There is no debug code or commented-out sections

4. Variables and functions have meaningful names

# GitHub Usage Assessment Criteria

The best practices presented in the preceding chapters are not merely recommendations; they form part of the assessment of assignments. The assessment considers not only the final result but also the development process, as it reflects your working methods and consistency in using the tool.

Using GitHub supports the learning process and helps improve the organization, documentation, and assessment of your work. You are expected to make the consistent application of the best practices in this guide a standard part of your working methodology in both individual and group projects.

## General Principles

The assessment takes into account the consistent use of GitHub throughout the assignment, the cleanliness and organization of the repository, and the ability to document progress through the change history.

The commit history is key evidence of the work performed. For this reason, each student must use only their personal GitHub account so that their contribution can be attributed correctly.

## Criteria for Individual Assignments

Individual assignments are assessed on the extent to which the student follows fundamental version control best practices:

- **Commit consistency:** regular commits at significant achievements/milestones that demonstrate the gradual development of the work, rather than the submission of a large amount of content shortly before the deadline

- **Commit message quality:** self-explanatory, descriptive messages that explain the nature of the change

- **Repository organization:** logical folder structure, correct file naming, and avoidance of unnecessary or sensitive files

- **Documentation:** presence and quality of `README.md` and `.gitignore`

- **Use of branches** (where applicable): viewed positively in more complex assignments

## Criteria for Group Assignments

All the individual criteria above apply to each member of a group assignment. The following are also assessed:

- **Use of branches:** correct use of feature branches for separate development work

- **Pull requests and code review:** controlled integration of changes with documentation of the process

- **Coordination:** minimal merge conflicts as an indication of good planning and communication

- **Balanced participation:** meaningful and sustained contributions from all members. Work concentrated in one person does not meet the expectations for group work

- **Work allocation documentation:** clear description of roles in the `README` and `Changelog`

- **Evidence of communication:** issues, comments, or other evidence of collaboration within GitHub

## Indicative Elements Assessed

| Assessment Criterion                | Individual Assignments | Group Assignments |
|-------------------------------------|:----------------------:|:-----------------:|
| Commit frequency and distribution   |          Yes           |        Yes        |
| Commit message quality              |          Yes           |        Yes        |
| Repository organization and hygiene |          Yes           |        Yes        |
| Presence and quality of `README.md` |          Yes           |        Yes        |
| Correct use of `.gitignore`         |          Yes           |        Yes        |
| Use of branches                     |        Optional        |        Yes        |
| Pull requests and code review       |           No           |        Yes        |
| Issues / comments / communication   |           No           |        Yes        |
| Balance of member contributions     |           No           |        Yes        |
| Changelog and role allocation       |           No           |        Yes        |

# Conclusion

GitHub is a powerful tool that, when used effectively, enhances your learning experience, improves collaboration with your fellow students, and develops professional skills. The practices described in this guide represent industry-standard approaches used by professional software development teams worldwide.

Remember:

1. Start with the basics and gradually adopt more advanced practices

2. Consistency is more important than perfection

3. Learn from mistakes—they are part of the learning process

4. Help your fellow students learn best practices

5. Continue improving your skills as you progress

Useful links:

- Official Git documentation: <https://git-scm.com/doc>

- GitHub Guides: <https://guides.github.com>

- Pro Git book: <https://git-scm.com/book/en/v2>

Good luck with your projects!
