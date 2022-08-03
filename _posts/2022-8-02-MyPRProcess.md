---
layout: post
title: My Pull Request Process
---

Putting this here so I can refer myself and others back to this in the future.

## Creating a Pull Request ##

> :warning: **We treat  the master / main branch as our source of truth and it reflects what is running 'live' within environments**

A pull request should only be created when the feature branch, etc intended for merging is deemed ready for use.

### Pre-requisites ###

> ⚠️ **A PR should not be used just to compare between your branch etc as that can be achieved via your git WEB/UI of choice or via vimdiff or similar in the CLI**

The following should be done as a minimum prior to the creation of a pull request to reduce the likelihood of any issues at merge time:
* Implementation of feature/fix.
* Testing with evidence to prove it works.
* Does not introduce bugs or regressions.

Once the above is complete, a rebase should then be performed against the upstream branch (master/main), to ensure that the branch is up to date with any changes that have happened since you branched off.

### Process ###

One the pre-requisites above have been completed, a PR can then be created either from the WEB/UI of choice or the CLI.
A PR should contain the following information as a minimum:
* **A Title** - Would be useful to include the relevant ticket ID if appropriate.
* **A Description** - What has changed?

> ❕ **Optional** - test results attached or some other form of evidence that the change works as intended and does not regress existing functionality.

When the PR is created the link should be provided to whoever is going to review it.

### Reviewing a Pull Request ###
If you are reviewing a PR, it is prudent to do the following:
* Review the diff, raise any questions to the PR author, including anything you might not understand about the change.
* Look at the diff to ensure best practice is being followed (will differ between teams, companies, and languages).
* Review any associated tickets.
* Review any test data or evidence if applicable.
* Add comments if there are items to discuss.
* Mark the PR as approved only when it is ready, or any comments have been addressed.
* Discuss the outcome with the PR creator:
- Please see my comments etc. I have marked your PR as having work that needs addressing.
- I have approved your PR, it is ready to merge.

### Merging a Pull Request ###
When a PR has been reviewed and approved, it can be then be merged by the PR creator. Anyone who needs to be aware of the change should then be notified.
Following the merge of the PR, relevant artefacts should be built and deployed where applicable.
