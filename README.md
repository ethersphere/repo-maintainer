# Repo Maintainer Role

## Motivation

As the number of GitHub repositories increases, users might find themselves harder to navigate and understand who is maintaining them. When they need to either better understand the code’s functionality, patch a bug or a security issue, it might be unclear who is responsible for the codebase, who can release a new version of the package, who has access rights, and so on. Most probably they have to start a detective work using the GitHub’s Contributors overview and contacting the most promising people, or finding out this information through other channels.
Also, for the contributors or collaborators to the repo, it might be helpful to have clearly defined roles and responsibilities for the repo’s lifecycle.

## The role

Repo Maintainer (RM) is a role linked to a specific repo. This person is responsible for this repository from a technical perspective, ensuring code quality, robustness, and functionality of the repo’s code. They do not handle the product that this repository is part of and hence is not in conflict with Product Owner (PO). Instead, it is expected that these two people will closely collaborate. While most of the requests might flow from the PO, the Repo Maintainer might raise needs, as well (for example dedicated time for refactors, test improvements, and so on). Repo Maintainer also has to coordinate with Tech Lead to ensure that the repo is following team wide standards and directions he sets.

### Responsibilities

The main Repo Maintainer’s responsibility is to **ensure a clean, healty and maintainable code base that can be built upon in the future**.

This includes the following tasks:

1. PRs management
   1. Main PR reviewer
   2. Merging of approved PRs
   3. Request splitting PRs when they are too big or tackle multiple issues
2. Dependency management
   1. Merge dependabot PRs and fix potential issues
3. Documentation
   1. Ensuring/enforcing up to date README and the related documentation if applicable
4. Release new versions of packages
5. Changelog
   1. Correctly follow SemVer
   2. Indicate Breaking Changes
   3. Clean Git history (related to 1.2)
6. Enforcing the “definition of done” that the team agreed on
7. Communication with
   1. PO
   2. Tech Lead
   3. other teams that need technical support for the repo, such as security, DevOps,…

### Access rights

As some of the Repo Maintainer’s tasks require proper access rights he should be given rights like:

- NPM write right
- GitHub Admin role for the repo

## Implementation

Repos that implement this role should clearly indicate the Repo Maintainer in its README. This should include some contact information and a link to this document (which explains the role).

### Two Maintainers per repo

There should be two Repo Maintainers defined for each repo - **main** and **backup** maintainers. 

The main maintainer has the ownership over the repo and the main responsobility. Backup maintainer is there to review the main maintainer's work and to step in if the main maintainer is not available. Backup maintainer should have good knowledge of the repo and the project to efficiently step in as well as all the access rights. 

The order of the maintainers should reflect the main and backup roles, where the main maintainer should be first.

### GitHub workflow

There are some features of the GitHub workflow that should be properly used for good and clear communication amongst the contributors, collaborators, and the RM. This document is not meant to define the GitHub workflow, however, the following points are important for correct and painless execution of duties of the Maintainer:

 - Correct usage of Draft PRs - WIP PRs should be Draft ones and only correctly marked PRs will be reviewed and merged.
 - If a PR is ready for review, but should not be merged yet because of some other dependencies it should have the “Do not merge” label.
 - Once PR is reviewed and changes are requested, the author of the PR should avoid force-push to the branch as it makes it harder to track the incremental changes.

### CODEOWNERS

Very helpful feature of GitHub to support this workflow is [Code Owners](https://docs.github.com/en/free-pro-team@latest/github/creating-cloning-and-archiving-repositories/about-code-owners). It is highly preferable to use it and define the Repo Maintainers as Code Owners as well. Optinally the maintainers can enable the feature of protected branch "Require Code Owner approval before merging PR".

## Maintainer

 - [AuHau](https://github.com/auhau/)
