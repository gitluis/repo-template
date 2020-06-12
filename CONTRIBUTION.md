# Contribution

For those team members willing to contribute to the toolbox make sure you understand the content hereby explained before doing anything.

* [Contribution](#contribution)
    * [Branch Naming Convention](#branch-naming-convention)
    * [How-to Contribute](#how-to-contribute)
    * [Pull Requests](#pull-requests)


## Branch Naming Convention

All development branches are to be named after `dev-*` where `*` shall be replaced by the branch name. The branch name shall reflect what the branch was created for or intended to be worked on (defect/bug fix, addition, enhancement, etc.).

Examples:
| Branch Purpose                        | Bad Name         | Good Name                |
|:--------------------------------------|:-----------------|:-------------------------|
| Create a new LASSO module             | `dev-add-module` | `dev-add-lasso-module`   |
| Fix bug in P-values module's function | `dev-fix-bug`    | `dev-fix-pvalues-bug`    |
| Refactor Logistic Regression module   | `dev-change-lr`  | `dev-refactor-lr-module` |

Remember, **explicit is better than implicit** (add, fix, refactor, bug/defect, improve/enhance).


## How-to Contribute

1. Create a local branch
2. Create/modify unit test cases
3. Add/commit software changes
4. Run unit test cases
    * Back to step 2 upon failures
5. Push local branch to remote repository
    * `git push origin dev-*`
6. Create a pull-request against `qa` branch
7. Request feedback from peers or reviewers

## Pull Requests

1. Implement changes requested
   * As agreed on per team discussions
2. Run unit test cases
   * Back to step 1 upon failures
3. Push new changes implemented
4. Repeat steps 1-3 until team agreement
5. Run unit test suite from `qa` branch
   * All tests must pass
6. If test suite passes, approve review changes
   * Back to step 1 upon failures
7. Merge changes in `qa` to `master` branch
