# Git policy

# Gitflow strategy

It is defined that all commits, pull requests and merges must follow the Gitflow strategy described in this documents

# Default branches

Default branches is protect and have a extra layer of security, be for make a pull request or approve a merge it need a permission and authentication to do it. This branches is never closed. All repositories must have at least this branches.

The default branches is:

1. `main` > a reflection of production code, and triggers deployment;
2. `staging` > pre-deployment branch, that triggers homologation deployment;
3. `develop` > concentrates development PRs waiting approvals and tests;

# Support branches

In addition to the main branches, we will use auxiliary branches to manage the lifecycle of features, releases and hotfixes. Different from default, those braches can be deleted.

1. **Release branches:**
    
    Used to prepare a new version, such as final adjustments, corrections, or small refinements. It will be the grouping of packages that will be submitted for testing approval and, once approved, will be taken to production without any new changes.
    
    - **Origin:** `develop`
    - **Merge to:** `main`, `develop`, `staging`, `release/*`, `feature/*`
    - **Naming:** `release/<semVer>` , e.g. `release/1.2.34` ****
2. **Feature branches:**
    
    Used to develop new features or significant changes.
    
    - **Origin:** `develop`
    - **Merge to:**  `release/*`
    - **Naming:** `feature/<task_id-feature_name>` , e.g. `feature/EG047-new_product_page`
3. **HotFix braches**
    
    Used for quick fixes in production without going through the full development cycle.
    
    - **Origin:** `main`
    - **Merge to:** `main`, `develop`, `staging`, `release/*`, `feature/*`
    - **Naming:** `hotfix/<issue_id-bug_name>` , e.g. `hotfix/EG084-new_customer_error`

# Workflow

For each type of task you gonna follow the correct GitFlow. We gonna describe the entire process, since receive the task, to merge in the main.

## Feature development

1. From the `develop` branch, create a new branch `feature/*`;
2. All commits in the development of this new feature gonna be in the `feature/*`;
3. When all development is finished, you create a Pull Request, and a colleague gonna review the code, and merge it into `develop` branch, then delete the `feature/*` branch you just created;
4. Then, after all colleagues finished their tasks, and merged in the `develop` branch, it’s created a new PR to `release/*`, and then after aproval it’s merged;