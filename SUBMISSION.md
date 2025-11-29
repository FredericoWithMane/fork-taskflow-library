# Team Collaboration Assignment Submission

## Repository Links
- Original repository: https://github.com/FrodoAK060/taskflow-library
- Fork repository: https://github.com/FredericoWithMane/fork-taskflow-library (fork)
- Feature PR: https://github.com/FrodoAK060/taskflow-library/pull/1
- Release tag: https://github.com/FredericoWithMane/fork-taskflow-library/releases/tag/v1.3.0

## Fork Workflow Evidence
```bash
# Show remotes configuration
$ git remote -v
origin  git@github-frederico:FredericoWithMane/fork-taskflow-library.git (fetch)
origin  git@github-frederico:FredericoWithMane/fork-taskflow-library.git (push)
upstream        git@github.com:FrodoAK060/taskflow-library.git (fetch)
upstream        git@github.com:FrodoAK060/taskflow-library.git (push)

# Show merged PR in history
$ git log --oneline --grep="priority"
777b195 (upstream/main, upstream/HEAD) Merge pull request #1 from FredericoWithMane/feature/task-priority
899175f test: add tests for task priority
f27656a feat: add priority support to Task class
```

## Code Review Participation
1. PR I created: https://github.com/FrodoAK060/taskflow-library/pull/1
   - Review feedback received: ничего, молча принял и смержил)
   - How I addressed it: Adds priority support to tasks as requested in issue #42

2. PR I reviewed: https://github.com/FrodoAK060/taskflow-library/pull/2  
   - Comments I made: requested 3 changes
   - Improvements suggested: - "Consider adding a maximum limit for labels (e.g., 5 per task)"
                             - "Missing tests for the addLabel method"
                             - "Please update the API documentation"

## Release Management
1. Version bump: 1.2.0 → 1.3.0
2. Changelog updated: Yes
3. Tag created: v1.3.0
4. Semantic versioning followed: Yes (minor release for new features)

## Workflow Analysis
Current workflow: GitHub Flow
- Pros experienced: Простая модель ветвления, легко отслеживать изменения и быстрое внедрение новых функций в main через pull request
- Cons experienced: Все изменения сразу влияют на main, риск конфликтов при большом количестве PR
- Recommended improvements: Активнее использовать CI/CD для автоматического тестирования PR

## Verification Commands
```bash
# Verify fork setup
git remote -v | grep upstream
upstream        git@github.com:FrodoAK060/taskflow-library.git (fetch)
upstream        git@github.com:FrodoAK060/taskflow-library.git (push)

# Verify tags
git tag -l "v1.3*"
v1.3.0

# Verify PR was merged
git log --grep="feat:" --oneline
f27656a feat: add priority support to Task class

# Check release tag details
git show v1.3.0

tag v1.3.0
Tagger: Fyodor <chasolist@gmail.com>
Date:   Sat Nov 29 23:20:02 2025 +0500

Release version 1.3.0

Features:
- Task priorities
- Task labels
- Improved validation

commit d3d07c98a17a167aec2c422bdabdc9751e2d148b (tag: v1.3.0, origin/release/1.3.0, origin/main, origin/HEAD, release/1.3.0)
Author: Fyodor <chasolist@gmail.com>
Date:   Sat Nov 29 22:56:24 2025 +0500

    Change package and CHANGELOG

diff --git a/CHANGELOG.md b/CHANGELOG.md
index c1c836d..3f38c3b 100644
--- a/CHANGELOG.md
+++ b/CHANGELOG.md
@@ -1,3 +1,10 @@
-## [Unreleased]
+## [1.3.0] - 2025-29-11
 ### Added
 - Task priority support with setPriority() method
+- Task labels with addLabel() method
+
+### Changed
+- Improved task validation
+
+### Fixed
+- Board filtering by status
diff --git a/package.json b/package.json
index 75f4dff..a91921b 100644
--- a/package.json
+++ b/package.json
@@ -1,5 +1,5 @@
 {
     "name": "taskflow-library",
-    "version": "1.2.0",
+    "version": "1.3.0",
     "description": "Simple task management library"
 }
```

## Self-Assessment Checklist
- [x] Successfully created and configured fork
- [x] Made meaningful contribution via PR
- [x] Participated in code review (both sides)
- [x] Followed project contribution guidelines
- [x] Created proper release with semantic versioning
- [x] Analyzed different workflow strategies
- [x] Documented all processes
