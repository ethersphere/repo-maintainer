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

### Backup Repo Maintainer

It is possible that the RM can not be reachable for a longer time period. It is then recommended to define a Backup RM who then takes over the tasks when the main RM is not available. He should have all the necessary access rights that the main RM has.
In best-case scenarios, Backup RM should be informed upfront about planned unavailability and be prepared for the task. Backup RM should not be misused as a go-around of the main RM. Additionally, in RM’s presence, the Backup RM should not be able to assume the role’s abilities and responsibilities

## Implementation

Repos that implement this role should clearly indicate the Repo Maintainer in its README. This should include some contact information and a link to this document (which explains the role).

### GitHub workflow

There are some features of the GitHub workflow that should be properly used for good and clear communication amongst the contributors, collaborators, and the LM. This document is not meant to define the GitHub workflow, however, the following points are important for correct and painless execution of duties of the Maintainer:

 - Correct usage of Draft PRs - WIP PRs should be Draft ones and only correctly marked PRs will be reviewed and merged.
 - If a PR is ready for review, but should not be merged yet because of some other dependencies it should have the “Do not merge” label.
 - Once PR is reviewed and changes are requested, the author of the PR should avoid force-push to the branch as it makes it harder to track the incremental changes.

### CODEOWNERS

It is also possible to use GitHub's [CODEOWNERS](https://docs.github.com/en/free-pro-team@latest/github/creating-cloning-and-archiving-repositories/about-code-owners) feature to support the LM role. Especially together with the feature "Require Code Owner approval before merging PR".

## Maintainer

 - [AuHau](https://github.com/auhau/)
